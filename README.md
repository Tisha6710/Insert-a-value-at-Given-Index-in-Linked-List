# Insert-a-value-at-Given-Index-in-Linked-List
package LinkedListttt;

public class InsertAtGivenNode {
    static class Node{
        int data ;
        Node next;
        Node(int data ){
            this.data=data;
        }
    }

    void insertat(int idx,int val){

        Node temp=new Node(val);
        Node head=null;
        if(idx==0){
            temp.next=head;
            head=temp;
            return;
        }
        Node t=head;

        for(int i=1;i<=idx-1;i++){
            t = t.next;

        }
        temp.next=t.next;
        t.next=temp;
    }
}

