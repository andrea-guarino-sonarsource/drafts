# Support secondary locations for ESLint-based SonarJS rules.

## WHY

MMF-1409 enhances SonarJS adoption into the JavaScript community thanks to its integration with ESLint.
However, SonarQube and SonarCloud platforms enhance issues reporting thanks to the presence of secondary locations. Currently ESLint custom rules don't have a concept of secondary locations or data flow reporting.

## WHAT

- Define an interface to send data between eslint-bridge and SonarJS
- Replace SonarJS cognitive complexity rule with its corresponding ESLint-based rule
- Verify that message reporting in eslint-plugin-sonarjs is compliant with ESLint usual environment

## HOW
