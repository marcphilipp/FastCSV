# Open Test Reporting Demo

> FastCSV is just a regular, "random" open source project.

1. Show [Gradle changes](lib/build.gradle.kts)

2. Run tests

```shell
./gradlew test --rerun intTest --rerun --continue
```

3. Open event-based XML reports:
   - [test](lib/build/test-results/test/open-test-report.xml)
   - [intTest](lib/build/test-results/intTest/open-test-report.xml)

4. Convert to HTML report:
```shell
jbang org.opentest4j.reporting:open-test-reporting-cli:0.2.7:standalone \
  html-report \
  --output lib/build/reports/open-test-report.html \
  lib/build/test-results/test/open-test-report.xml \
  lib/build/test-results/intTest/open-test-report.xml \
  --open
```
