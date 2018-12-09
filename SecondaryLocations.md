# Support secondary issue locations for ESLint-based SonarJS rules.

## WHY

As a result of Epic MMF-1409, SonarJS rules will be ESLint-compatible and will be processed by ESLint engine.
However, ESLint, contrary to SonarQube and SonarCloud platforms, doesn't support issue reporting containing secondary locations. Goal of this MMF is to make sure that ESLint-based SonarJS rules that require secondary issue locations can still benefit of the same level of quality in terms of reporting as we have today.

## WHAT

In order to implement this MMF, we will need to firstly:

- Define an interface to communicate secondary issue locations from eslint-bridge to SonarJS sensor
- Allow ESLint-based SonarJS rules to report secondary issue locations
- Migrate the following rules already implemented in eslint-plugin-sonarjs that require secondary issue locations:
  - Cognitive complexity
  - ...

Having that in place, we will need to:
- Ensure that *eslint-plugin-sonarjs* issue reporting remains unchanged and compatible with *ESLint* when used with ESLint tool.
- Verify 

- Replace SonarJS cognitive complexity rule with its corresponding ESLint-based rule
- Verify that message reporting in eslint-plugin-sonarjs is compliant with ESLint usual environment

## HOW
