# 📊 Response Visualizer

This example demonstrates how to use **Bruno’s Response Visualizer** to transform raw API responses into meaningful visual formats like **tables, dashboards, and charts**.

Using the `bru.visualize('html')` method, you can render custom HTML, including UI cards and charts (such as pie and bar charts using Chart.js), to better understand API data like request distribution, status codes, and performance metrics.

This helps you move beyond raw JSON and build interactive, visual insights directly inside your API workflow.

### Table Visualization 

```js

bru.visualize('table', {
  name: 'usersTable',
  provider: 'ag-grid',
  props: {
    rowData: [],
    columnDefinitions: []
  }
});
```

### HTML Visualization

```js

bru.visualize('html', {
  name: 'htmlView',
  content: `
    <h2>API Report</h2>
    <p>Custom HTML content</p>
  `
});

```

### Handlebar Visualization 

```js

bru.visualize('html', {
  name: 'userCard',
  template: `
    <div>
      <h2>{{name}}</h2>
      <p>{{email}}</p>
    </div>
  `,
  data: {
    name: "Bruno",
    email: "bruno@test.com"
  },
  options: {}
});
```
---

## 🚀 What this example includes

- 📊 Pie chart (API method distribution)
- 📈 Bar chart (status code analysis)
- 🧾 HTML dashboard (API performance summary)
- 🎯 Real-world structured sample data

---

## 📖 Learn More

👉 Read more about Response Visualizer in Bruno docs:  
https://docs.usebruno.com/advanced-guides/visualize
