---
layout: post
title: 코딩 인터뷰 완전분석
---
## 연결리스트

*  보관된 원소를 상수 시간에 접근할수 없음
*  재귀 호출 빈번

```java
class Node{
	Node next = null;
	int data;
	
	public Node(int d) {
		data = d;
	}
	
	void appendToTail(int d) {
		Node end = new Node(d);
		Node n = this;
		while(n.next != null) {
			n = n.next;
		}
		n.next = end;
	}
	
}
```

```java
Node deleteNode(Node head, int d) {
	Node n = head;
	
	if(n.data == d){
		return head.next
	}
	
	while(n.next != null) {
		if(n.next.data ==d) {
			n.next = n.next.next;
			return head;
		}
		n = n.next
	}
	return head
}
```

## 트리와 그래프

```java
void search(Node root) {
	if(root == null) return;
	visit(root);
	root.visited = true;
	foreach (Node n in root.adjacent) {
		if(!n.visited){
			search(n)
		}	
	}
}

```