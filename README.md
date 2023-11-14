# A-B-TESTING-IN-R
# Assume we have two sets of data for version A and version B
group_A <- c(25, 30, 35, 40, 45)
group_B <- c(20, 28, 32, 38, 42)

# Perform a two-sample t-test
t_test_result <- t.test(group_A, group_B)

# Display the results
cat("T-Test Results:\n")
cat("----------------\n")
cat("Test Statistic:", t_test_result$statistic, "\n")
cat("P-value:", t_test_result$p.value, "\n")
cat("Degrees of Freedom:", t_test_result$parameter, "\n")
cat("\n")

# Interpret the results
if (t_test_result$p.value < 0.05) {
  cat("Reject the null hypothesis at the 0.05 significance level.\n")
  cat("There is sufficient evidence to suggest a significant difference between A and B.\n")
} else {
  cat("Fail to reject the null hypothesis at the 0.05 significance level.\n")
  cat("There is not enough evidence to suggest a significant difference between A and B.\n")
}
