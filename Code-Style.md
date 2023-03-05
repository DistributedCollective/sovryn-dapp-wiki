# Cleanliness

| Name | Rule |
| ---- | ---- |
| Dead Code | Remove old and unused code. Don't just create the replacement, also cleanup the replaced and check for newly unused assets. If something should specifically not be removed it should be marked with a comment. |
| Out Commented Code | Remove out commented code before merging. If something should be specifically not be removed it should be marked with a comment. |
| ESLint Warnings | Fix ESLint Warnings before merging. If you are sure the warning is wrong you can use eslint-ignore comments, but you need to specify your reasoning with an adjacent comment. Failure to resolve warnings will prevent builds from being deployed to production environments. |
| Comments | Comments should provide value by explaining the reasoning for the code or complex parts. If the comment does not, remove it! <br /><br />JSDoc style comments <code>(/** description */)</code> can be used to add valuable information to functions/classes/types/properties/constants, e.g. the type may be string, but its value is expected to be a wei string. |
| console.log | Remove console.log (warn, info, error) calls, that were intended for development/debugging. console.error calls are acceptable where used in exception handling. |
| Breaking Changes | When you change a component/function/class in a way that changes it's usage, check the whole project for usages and update them. Compile-time warnings will indicate direct violations of this, but diligence is advised when making changes that may have unintended side effects. |
| Inline Hard-Coding | Avoid using inline defined constants. Define a named constant instead. Instead of iterating until you reach 5, iterate until MAX_ENTRY_COUNT. |
| Magic Values | Define Enums for function parameters, instead of defining it as number/string and expecting specific values. <br /><br />Don't use: <br/><code>size: 'sm' \| 'md' \| 'lg' \| 'xl';</code><br /><br />instead use: <br/><code>enum ButtonSize {<br/>sm = 'sm',<br/>  md = 'md',<br/>lg = 'lg',<br/>xl = 'xl',<br/>}<br/>size: ButtonSize;</code> |
| Named Exports | Use named exports. |
| No Wildcard Imports | Never use wildcard imports. <br /><br />Don't use: <br /><code>Import * as Module from '…';</code><br /><br />instead use: <br /><code>Import { a, b, c } from '…';</code> |
| Generalize | Use existing functions and components that fit your use. Extract embedded code to be used in multiple locations. Try to create functions and components in a generalized way, so it can be used in other places. |
| No inline ifs | Do not use inline ifs! <br /><br />Don't use: <br /><code>if(condition) functionCall();</code><br /><br />instead use: <br /><code>if(condition) {<br />functionCall();<br />}</code> |




# Naming
# Typescript
# React
# NPM Packages
# GraphQL Queries
# Styling
# Localisations (Translations)
# Number Localisations
# Formatting
