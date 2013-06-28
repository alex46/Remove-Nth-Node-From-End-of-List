Remove-Nth-Node-From-End-of-List
================================


/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        // Start typing your Java solution below
        // DO NOT write main() function
        
        if(head == null) return null;
        
        ListNode h1 = head;
        ListNode h2 = head;
        
       for(int i = 0; i < n; i++){
           h1 = h1.next;
           
           if(h1==null) return head.next;
       }
       
       while(h1.next!=null){
           h1 = h1.next;
           h2 = h2.next;
       }
        
      // h2.val = h2.next.val;
       h2.next = h2.next.next;
       
       return head;
    }
}
