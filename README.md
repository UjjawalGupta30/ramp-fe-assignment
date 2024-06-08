## Changelog

### Bug Fixes Details

#### Bug 1: Select dropdown doesn't scroll with rest of the page
- **Fixed:** Updated the dropdown position calculation in the `InputSelect` component to adjust its position based on the scroll position of the window.
- **Impact:** Ensures that the dropdown for selecting employees remains aligned with the select input as the user scrolls, improving the UI experience.

#### Bug 2: Approve checkbox not working
- **Fixed:** Implemented a callback in `TransactionPane` to handle state changes when the checkbox is toggled.
- **Impact:** Users can now toggle the approval state of transactions directly from the UI, and the state is correctly synced with the server.

#### Bug 3: Cannot select _All Employees_ after selecting an employee
- **Fixed:** Corrected the employee selection handling in `App.tsx` to properly reset the transaction list when "All Employees" is selected.
- **Impact:** Enhances stability and functionality of the employee filter, allowing for seamless switching between filters without crashing the page.

#### Bug 4: Clicking on View More button not showing correct data
- **Fixed:** Modified the `loadAllTransactions` function to append new transactions to the existing list instead of replacing them.
- **Impact:** Users can now view a continuous list of transactions without losing earlier data, improving data visibility and user interaction with pagination.

#### Bug 5: Employees filter not available during loading more data
- **Fixed:** Decoupled the loading states of employee data and transaction data in the `useEmployees` hook.
- **Impact:** Provides a smoother user experience by ensuring that the employee filter is available even when transaction data is loading.

#### Bug 6: View more button not working as expected
- **Fixed:** Added conditional rendering for the "View More" button based on whether there are more transactions to load.
- **Impact:** Prevents user confusion and potential errors by only displaying the "View More" button when additional data can be loaded.

#### Bug 7: Approving a transaction won't persist the new value
- **Fixed:** Updated the `setTransactionApproval` function in `requests.ts` to correctly update the transaction's approved state in the mock data.
- **Impact:** Guarantees that changes to the approval state of transactions are persistent and reflect accurately across user sessions.
