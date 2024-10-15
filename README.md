
# DynamicLibrary

**DynamicLibrary** is a React component library that provides customizable UI components: `Dropdown`, `Modal`, `Tabs`, `Datatable`, and `Accordion`. It also includes theme management using `useTheme` and `ThemeProvider` for switching between dark and light themes.

## Installation

Install the library via npm:

```bash
npm install dynamiclibrary
```

## Components

### 1. Datatable

A customizable data table component.

```jsx
import { Datatable } from 'dynamiclibrary';

<Datatable
  userData={data}
  CustomUserDataCard={MyCustomCardComponent}
  CustomDataNavBar={CustomNavBarComponent}
  MainDataNavBarStyle={{ backgroundColor: '#ddd' }}
  UserDataCardsStyle={{ padding: '10px' }}
/>
```

- **Props:**
  - `userData`: Data to display.
  - `CustomUserDataCard`: Component for custom user data card.
  - `CustomDataNavBar`: Component for custom navigation bar.
  - `MainDataNavBarStyle`: Styles for the main navigation bar.
  - `UserDataCardsStyle`: Styles for the user data cards.

### 2. Accordion

A customizable accordion component.

```jsx
import { Accordion } from 'dynamiclibrary';

<Accordion
  accordianQuestions={questions}
  accordianMainStyle={{ margin: '10px' }}
  accordianQuestionStyle={{ fontWeight: 'bold' }}
  accordianQuestionTextStyle={{ color: 'blue' }}
  accordianAnswerStyle={{ color: 'gray' }}
/>
```

- **Props:**
  - `accordianQuestions`: Array of questions and answers.
  - `accordianMainStyle`: Styles for the accordion container.
  - `accordianQuestionStyle`: Styles for each question.
  - `accordianQuestionTextStyle`: Styles for question text.
  - `accordianAnswerStyle`: Styles for the answer.

### 3. Tabs

A customizable tabs component.

```jsx
import { Tabs } from 'dynamiclibrary';

<Tabs
  tabContents={contents}
  CustomTabButtons={MyTabButtonsComponent}
  CustomContentContainer={MyContentContainerComponent}
/>
```

- **Props:**
  - `tabContents`: Array of tab contents.
  - `CustomTabButtons`: Custom component for rendering tab buttons.
  - `CustomContentContainer`: Custom component for content container.

### 4. Dropdown

A customizable dropdown component.

```jsx
import { Dropdown } from 'dynamiclibrary';

<Dropdown
  showDropdown={true}
  links={['Home', 'About', 'Contact']}
  dropDownContainerStyle={{ backgroundColor: 'lightgray' }}
  dropDownListStyle={{ padding: '5px' }}
  dropDownLinkStyle={{ color: 'black' }}
/>
```

- **Props:**
  - `showDropdown`: Boolean to show/hide dropdown.
  - `links`: Array of dropdown links.
  - `dropDownContainerStyle`: Styles for dropdown container.
  - `dropDownListStyle`: Styles for the list.
  - `dropDownLinkStyle`: Styles for individual links.

### 5. Modal

A customizable modal component.

```jsx
import { Modal } from 'dynamiclibrary';

<Modal
  showModal={true}
  setShowModal={setShowModal}
  title="Confirm Action"
  description="Are you sure you want to proceed?"
  onCancelPress={handleCancel}
  onProceedPress={handleProceed}
  TitleStyle={{ fontWeight: 'bold' }}
  DescStyle={{ fontSize: '14px' }}
  CancelButtonStyle={{ backgroundColor: 'red' }}
  ProceedButtonStyle={{ backgroundColor: 'green' }}
/>
```

- **Props:**
  - `showModal`: Boolean to show/hide modal.
  - `setShowModal`: Function to toggle modal visibility.
  - `title`: Modal title.
  - `description`: Modal description.
  - `onCancelPress`: Function for cancel button.
  - `onProceedPress`: Function for proceed button.
  - `TitleStyle`: Styles for the title.
  - `DescStyle`: Styles for the description.
  - `CancelButtonStyle`: Styles for cancel button.
  - `ProceedButtonStyle`: Styles for proceed button.

## Theme Management

Use `useTheme` and `ThemeProvider` to toggle between light and dark themes.

```jsx
import { ThemeProvider, useTheme } from 'dynamiclibrary';

<ThemeProvider>
  <App />
</ThemeProvider>;

const { theme, toggleTheme } = useTheme();

<button onClick={toggleTheme}>
  Switch to {theme === 'dark' ? 'Light' : 'Dark'} Theme
</button>;
```

- `useTheme`: Hook to access and toggle the theme.
- `ThemeProvider`: Wrap your app with this to enable theme functionality.
