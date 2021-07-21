class Node {
  constructor(value, next = null) {
    this.value = value;
    this.next = next;
  }
}

const find_cycle_start = function (head) {
  // find the start of the linked list cycle
  let slow = head,
    fast = head;
  // while loop: end when pointers collide
  while (fast !== null && fast.next !== null) {
    // reassign fast and slow pointers
    fast = fast.next.next;
    slow = slow.next;
    // if the pointers collide, we've know we have a cycle
    if (fast === slow) {
      cycleLength = calculateLength(slow)
      break;
    }
  }
  // start new pointers back at the head
  let pointer1 = head,
    pointer2 = head;
  // move pointer2 cycleLength nodes ahead
  while (cycleLength > 0) {
    pointer2 = pointer2.next;
    cycleLength -= 1;
  }
  // move pointers ahead by 1 until they meet
  while (pointer1 !== pointer2) {
    pointer1 = pointer1.next;
    pointer2 = pointer2.next;
  }
  return pointer1;
};

const calculateLength = (node) => {
  // calculate length of the cycle
  let current = node,
    cycleLength = 0;
  while (true) {
    current = current.next;
    cycleLength += 1;
    if (current === node) {
      break;
    }
  }
  return cycleLength;
}


head = new Node(1)
head.next = new Node(2)
head.next.next = new Node(3)
head.next.next.next = new Node(4)
head.next.next.next.next = new Node(5)
head.next.next.next.next.next = new Node(6)

head.next.next.next.next.next.next = head.next.next
// console.log(`LinkedList cycle start: ${find_cycle_start(head).value}`)

head.next.next.next.next.next.next = head.next.next.next
// console.log(`LinkedList cycle start: ${find_cycle_start(head).value}`)

head.next.next.next.next.next.next = head;
// console.log(`LinkedList cycle start: ${find_cycle_start(head).value}`);

// HAPPY NUMBER - two pointer approach
const find_happy_number = function (num) {
  // init slow and fast pointers
  let slow = num,
    fast = num;
  // use while loop to find cycle
  while (true) {
    // slow pointer will calculate one sum at a time
    slow = findSum(slow);
    // fast pointer will calculate two sums at a time (move forward two spaces)
    fast = findSum(findSum(fast));
    // we will find a cycle once the slow and fast pointers have converged
    if (slow === fast) {
      break;
    }
  }
  return slow === 1;
};

// calculate the sum of the square of all digits
const findSum = (num) => {
  let sum = 0;
  while (num > 0) {
    let digit = num % 10; // first isolate the 1s place
    sum += digit * digit; // add the square of the ones place
    num = Math.floor(num / 10); // move the next place to the left to the 1s place
  }
  return sum;
}


// console.log(`${find_happy_number(23)}`)
// console.log(`${find_happy_number(12)}`)

// DUTCH NATIONAL FLAG PROBLEM
const dutch_flag_sort = function (arr) {
  // init left and right pointers
  // iterate over the input arr: while left !== right
  // if we encounter a 2 place it at the end
  // if we encounter a 0, place at the beginning
};

let arr = [1, 0, 2, 1, 0];
dutch_flag_sort(arr);
console.log(arr);

arr = [2, 2, 0, 1, 2, 0];
dutch_flag_sort(arr);
console.log(arr);