#### 1.  Data Structures
- express_orders: A list of tuples to store location of express orders.
- assigned: A list of dictionaries for each assignment to delivery agent, includes agent count, priority and express orders.
- agents: An integer counter for delivery agents.

#### 2.  Algorithm Steps
- Add Express Orders: Append the location to the express_orders list.
- Add Priority Orders:
	- No Express Orders: Assign the priority order alone to a new delivery agent.
	- With Express Orders:
		- Calculate Distances: find eucledian distances from the priority order to all express orders.
		- Sort Distances: Sort distances to find the closest express orders.
		- Assign Orders: Assign the closest express orders (up to two) along with the priority order.
		- Remove Assigned Orders: Remove the assigned express orders from the list.
- Display Assignments: Print the assignments for each delivery agent.

#### 3. Time Complexity
- Adding Express Orders: O(1) per order.
- Adding Priority Orders: O(m log m), where m is number of express orders (due to sorting).
- Displaying Assignments: O(n), where n is the number of delivery agents.

#### 4. Space Complexity
- express_orders:  O(m)
- assigned: O(n)
- Overall: O(m + n)

#### 5. Assumptions and Trade-offs
- Assumptions: Correct input format and valid coordinates.
- Trade-offs: Avg case time complexity in sorting O(m log m).
