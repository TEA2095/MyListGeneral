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
    
    private Node<T> root;
    private long length;
    
    public MyList() {
        this.root = null;
        this.length = 0;
    }
    
    @Override
    public int size() {
        return 0;
    }

    @Override
    public boolean isEmpty(Object o) {
        return false;
    }
    
    @Override
    public boolean contains(Object o) {
       return false;
    }


    @Override
    public Iterator<T> iterator() {
        return null;
    }

    @Override
    public Object toArray() {
       return new Object[0];  
    }

    @Override
    public boolean add(Object o) {
        Node<T> node = new Node<>((i) o);
        if (this.root == null) {
            this.root = node;
            this.length++;
            return true;
        }
        
        end().setNextNode(node);
        this.length++;
        return true;
    }
    
    public Node<T> end() {
    Node<T> iter = this.root;
    if (iter ==null)
        return null;
    while (iter.hasNextNode()) {
        iter = iter.getNextNode();
    }
    return iter;
   
}  
    public Node<T> indexAt(long index) {
        Node<T> iter = this.root;
        if (iter == null)
            return null;
        if (index == 0)
            return iter;
        if (index < this.length && index > 0) {
            for (; index >= 0; --index) {
                iter = iter.getNextNode();
            }
            return iter;
        }
        else
            return null;
        }
  public boolean swap (long firstPos, long secondPos) {
        Node<T> node = indexAt(firstPos);
        Node<T> node1 = indexAt(secondPos).getNextNode();
        indexAt(firstPos - 1).setNextNode(indexa(secondPost);
        indexAt(firstPos).setNextNode(node.getNextNode());
        node.getNextNode().setNextNode(node);
        node.getNextNode(node1);
        return true;
    }
 public boolean sort() {
     if (comp.compare(indexAt(1), indexAt(2), > 0)) {
         swap(1,2);
     }
     if (comp.compare(indexAt(3), indexAt(2), > 0)) {
         swap(2,3);
     }
}
    @Override
     public boolean remove(Object o) {
        return false;
    }

    @Override
    public boolean containsAll(Collection<?> c) {
        return false;
    }
    
    @Override
    public boolean addAll(Collection<? extends T> c) {
        return false;
    }

    @Override
    public boolean removeAll(Collection<?> c) {
       return false;
    }

    @Override
    public boolean retainAll(Collection<?> c) {
        return false;
    }

    @Override
    public void clear() {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }
    
    @Override
    public String toString() {
        String result = "[";
        Node<T> iter = this.root;
        if (iter == null) {
            return null;
        }
        while (iter.hasNextNode()) {
            result += iter.toString() + ",";
            iter = iter.getNextNode();
        }
        result += iter.toString() + "]";
        return result;
    }
    
}
  
        
Interface Comparable {
    int compare(MyList.Node a, MyList.Node b);
}
    
