# fluid-table-react

## Overview

This librairy provides typescript Table component

## System Requirements

- Node version 18 or higher is required.
- React

## Getting Started

Install this package:

```shell
npm install fluid-table-react
```

```shell
pnpm add fluid-table-react
```

Import the Table component:

```js
import { Table, ColumnType } from "fluid-table-react";

<Table dataSource={employees} columns={columns} search />
```

You can then render the `Table` component like any other React component in JSX.
Use `ColumnType` for typing your data.


## Example

```js
interface Employee {
  key: string
  firstName: string
  lastName: string
}

const columns: ColumnType<Employee>[] = [
  {
    key: "firstName",
    title: "First Name",
    dataIndex: "firstName",
  },
  {
    key: "lastName",
    title: "Last Name",
    dataIndex: "lastName",
  },
]

export const EmployeesListPage = (
  props: PropsWithChildren<EmployeesListPageProps>,
) => {
  const employees = [
    {
        key: "1",
        firstName: "John",
        lastName: "Doe"
    },
    {
        key: "1",
        firstName: "Ned",
        lastName: "Stark"
    }
  ]

    return <Table dataSource={employees} columns={columns} search />
}
```

## NPM Package

Visit the NPM package page for installation and usage details:

[NPM Package - fluid-table-react](https://www.npmjs.com/package/fluid-table-react)