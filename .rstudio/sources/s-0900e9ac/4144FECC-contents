
# ==========================================
# BASIC DATA ANALYSIS USING R
# Dataset: test_dataset.csv
# ==========================================

# 1. Import the CSV dataset
data <- read.csv(file.choose())

# 2. Display the dataset
print(data)

# 3. Display first 6 rows
head(data)

# 4. Display last 6 rows
tail(data)

# 5. Check number of rows and columns
dim(data)

# 6. Display column names
names(data)

# 7. Check data structure and data types
str(data)

# 8. Statistical summary
summary(data)

# 9. Count rows and columns
nrow(data)
ncol(data)

# ==========================================
# SELECT COLUMNS
# ==========================================

# Display employee names
data$Name

# Display Name and City
data[, c("Name", "City")]

# Display Name, Department, and Salary
data[, c("Name", "Department", "Salary_INR")]

# ==========================================
# FILTER DATA
# ==========================================

# Employees from Bengaluru
subset(data, City == "Bengaluru")

# Employees working in QA
subset(data, Department == "QA")

# Employees with salary greater than 60000
subset(data, Salary_INR > 60000)

# Active employees
subset(data, Status == "Active")

# Employees older than 30
subset(data, Age > 30)

# ==========================================
# STATISTICAL CALCULATIONS
# ==========================================

# Average salary
mean(data$Salary_INR)

# Median salary
median(data$Salary_INR)

# Maximum salary
max(data$Salary_INR)

# Minimum salary
min(data$Salary_INR)

# Total salary
sum(data$Salary_INR)

# Average age
mean(data$Age)

# Standard deviation of salary
sd(data$Salary_INR)

# ==========================================
# SORT DATA
# ==========================================

# Sort salary in ascending order
data[order(data$Salary_INR), ]

# Sort salary in descending order
data[order(-data$Salary_INR), ]

# Sort employees by age
data[order(data$Age), ]

# ==========================================
# COUNT RECORDS
# ==========================================

# Employees in each department
table(data$Department)

# Active and Inactive employees
table(data$Status)

# Employees in each city
table(data$City)

# Department-wise employee status
table(data$Department, data$Status)

# ==========================================
# CHECK MISSING VALUES AND DUPLICATES
# ==========================================

# Missing values in each column
colSums(is.na(data))

# Total missing values
sum(is.na(data))

# Identify duplicate rows
duplicated(data)

# Count duplicate rows
sum(duplicated(data))

# Remove duplicate rows
data <- data[!duplicated(data), ]

# ==========================================
# CREATE A NEW COLUMN
# ==========================================

# Classify employees by age
data$Age_Group <- ifelse(
  data$Age >= 30,
  "30 and Above",
  "Below 30"
)

# Display updated dataset
print(data)

# ==========================================
# CREATE CHARTS
# ==========================================

# Bar chart: Employees by department
dept_count <- table(data$Department)

barplot(
  dept_count,
  main = "Employees by Department",
  xlab = "Department",
  ylab = "Number of Employees"
)

# Histogram: Salary distribution
hist(
  data$Salary_INR,
  main = "Salary Distribution",
  xlab = "Salary (INR)",
  ylab = "Frequency"
)

# Scatter plot: Age vs Salary
plot(
  data$Age,
  data$Salary_INR,
  main = "Age vs Salary",
  xlab = "Age",
  ylab = "Salary (INR)",
  pch = 19
)

# ==========================================
# EXPORT UPDATED DATASET
# ==========================================

write.csv(
  data,
  "updated_dataset.csv",
  row.names = FALSE
)

# ==========================================
# DISPLAY WORKING DIRECTORY
# ==========================================

getwd()

# ==========================================
# END OF PROGRAM
# ==========================================
