# SheriffExample

running `sheriff verify apps/sheriff-example/src/main.ts`

results in
```
Verification Report

No issues found. Well done!
```

running `sheriff verify apps/sheriff-example/src/app/non-compliant/ui/ui-violation.component.ts
`

results in
```
Issues found:
  Total Invalid Files: 3
  Total Encapsulation Violations: 1
  Total Dependency Rule Violations: 3
----------------------------------

|-- apps/sheriff-example/src/app/non-compliant/ui/ui-violation.component.ts
|   |-- Dependency Rule Violations
|   |   |-- from tag type:ui to tags type:data-access
|   |   |-- from tag type:ui to tags type:feat
|-- apps/sheriff-example/src/app/non-compliant/types/violation.types.ts
|   |-- Dependency Rule Violations
|   |   |-- from tag type:types to tags type:util
|-- apps/sheriff-example/src/app/non-compliant/feat/feat-violation.component.ts
|   |-- Encapsulation Violations
|   |   |-- ../util/internal/internal-util
```
