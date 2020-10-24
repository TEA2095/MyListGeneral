# MyListGeneral
package mylist;
import java.util.Collection;
import java.util.Iterator;

public class MyList<T> implements Collection {
  class Node<T> {    
        private T value;
        private Node<T> nextNode;
        
        public Node (T value) {
            this.value = value;
            this.nextNode = null;
        }
        
        public T getValue() {
            return value;
        }
        
        public Node<T> getNextNode() {
            return nex
        }
        
        public void setNextNode(Node<T> nextNode) {
            this.nextNode = nextNode;
        }
       
        public boolean hasNextNode() {
            if (this.nextNode != null)
                return true;
            return false;
        }
    }
    
