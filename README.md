# SimplyFi Assessment

**Assignment 1** -

Design the logo provided as an attachment.

**Solution:**

![img](./assets/img.png)

**Assignment 2** -

Q . Your son took a vacation through Europe without telling you. When the kid returned from the vacation you asked him where did he go. The kid told you: Dad I went to these cities: Amsterdam, Kiev, Zurich, Prague, Berlin, Barcelona.
I used only train as transportation and these were the available tickets:
Paris-Skopje, Zurich-Amsterdam, Prague-Zurich, Barcelona-Berlin, Kiev-Prague, Skopje-Paris, Amsterdam-Barcelona, Berlin-Kiev, Berlin-Amsterdam.
You know that your kid started with Kiev
Write a data structure and algorithm that will give you the route which your son was traveling.

**Answer:** -

```javascript
const tickets = {
  'Paris': 'Skopje',
  'Skopje': 'Paris',
  'Zurich': 'Amsterdam',
  'Amsterdam': 'Barcelona',
  'Barcelona': 'Berlin',
  'Berlin': 'Kiev',
  'Kiev': 'Prague',
  'Prague': 'Zurich'
};


function findRoute(tickets, start, end, path = []) {
  path.push(start);
  if (start == end) {
    return path;
  }
  if (!tickets[start]) {
    return null;
  }
  return findRoute(tickets, tickets[start], end, path);
}
let route = findRoute(tickets, 'Kiev', 'Berlin');
console.log(route);

```

Attachment : [Resume](./assets/Resume.pdf)
