package misc;

public class Stack_min {
	
	public static class Node{
		private int data;
		private Node next;
		
		public Node(int d) {
			data = d;
		}
	}
	
	private Node top;
	private Node min;
	
	public Stack_min(int d) {
		/*top.data = d;
		min.data = d;
		top.next = null;
		min.next = null;*/
		
		Node _top = new Node(d);
		top = _top;
		top.next = null;
		
		
		Node _min = new Node(d);
		min = _min;
		min.next = null;
	}
	
	public int pop() {
		
		if(top == null) {
			System.out.println("Empty Stack");
			return -1;
		}		
		int value = top.data;
		if(top.data == min.data) {
			min = min.next;
		}
		top = top.next;
		return value;
	
	}
	
	public void push(int d) {
		
		Node n = new Node(d);
		n.next = top;
		top = n;
		
		int k = min.data;
		
		/*
		 * Operating the min values "linked list"
		 */
		
		if(min.data > d) {
			min.data = d;
			min.next.data = k;
			return;
		}
		
		if(min.next == null) {
			min.next = new Node(d);
			min.next.next = null;
			return;
		}
		
		k = min.next.data;
		
		if(min.next.data > d) {
			min.next.data = d;
			min.next.next.data = k;
		}
		
		
	}
	
	public int get_min(){
		
		return min.data;
		
	}
	
	public int peek() {
		if(top != null) {
			return top.data;
		}
		return -1;
	}
	

}
