---
layout: examHandoutNoName
num: e01
ready: true
desc: "Midterm Exam E01 Handout"
exam_date: 2017-10-26 09:30:00.00-7
---

## `Dog.java`

{% highlight java linenos %}
public class Dog {

    private static Dog bestInShow = null;
    private String name;

    public static void setBestInShow(Dog b) {
	bestInShow = b;
    }

    public static Dog getBestInShow() {
	return bestInShow;
    }

    public Dog(String name) { this.name = name;}

    public static void main(String [] args) {

	Dog d1 = new Dog("Alf");
	Dog d2 = new Dog("Bella");
	Dog d3 = new Dog("Charlie");
	Dog d4 = new Dog("Davy");
	Dog d5 = d3;
	
	setBestInShow(d1);       gc();    
	d2 = d3;                 gc();                   
	d4 = d5;                 gc();                   
	d1 = null;               gc();                 
	d2 = null;               gc();
 	d3 = null;               gc();
 	d4 = null;               gc();
	setBestInShow(null);	 gc();
    }                              

    public static void gc(int ln) {
      // ... encourage garbage collection
    }     

}
{% endhighlight %}

<div class="page-break-before" style="font-size:90%; font-family: Arial Narrow, sans-serif;" markdown="1">

# class `java.util.ArrayList<E>`

The following excerpts from the javadoc for `java.util.ArrayList<E>` may be
helpful to you in completing this exam. 

## Inheritance Hierarchy (complete)

```
java.lang.Object
  java.util.AbstractCollection<E>
    java.util.AbstractList<E>
      java.util.ArrayList<E>
```

<div markdown="1" style="font-size: 80%; font-family: Arial Narrow, sans-serif;"
   class="hanging-indent-table">

| All Implemented Interfaces: | `Serializable, Cloneable, Iterable<E>, Collection<E>, List<E>, RandomAccess` |
| Direct Known Subclasses: | `AttributeList, RoleList, RoleUnresolvedList` |

</div>

## Constructors (complete)

<div markdown="1" class="hanging-indent-table">

| `ArrayList()` | Constructs an empty list with an initial capacity of ten.
| `ArrayList(Collection<? extends E> c)` | Constructs a list containing the elements of the specified collection, in the order they are returned by the collection's iterator. |
| `ArrayList(int initialCapacity)` |Constructs an empty list with the specified initial capacity. |

</div>

## Most important methods, with brief description

<div markdown="1" class="hanging-indent-table">

| `boolean` | `add(E e)` | Appends the specified element to the end of this list. |
| `void` | `add(int index, E element)` | Inserts the specified element at the specified position in this list. |
| `void` | `clear()` | Removes all of the elements from this list.|
| `E` | `get(int index)` | Returns the element at the specified position in this list. |
| `int` | `indexOf(Object o)` | Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| `boolean` | `isEmpty()` | Returns true if this list contains no elements. |
| `int`	|  `lastIndexOf(Object o)` | Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| `E` | `remove(int index)` | Removes the element at the specified position in this list.|
| `boolean` | `remove(Object o)` | Removes the first occurrence of the specified element from this list, if it is present. |
| `E` | `set(int index, E element)` | Replaces the element at the specified position in this list with the specified element. |
| `int` | `size()` | Returns the number of elements in this list. |

</div>

## Additional methods, listed by method signature only.

<div markdown="1" class="hanging-indent-table">

| `boolean addAll(Collection<? extends E> c)` | `boolean	addAll(int index, Collection<? extends E> c)` |
| `Object   clone()` |  `boolean  contains(Object o)` |
| `void	   ensureCapacity(int minCapacity)` | `void forEach(Consumer<? super E> action)` |
| `Iterator<E> iterator()` | `ListIterator<E>  listIterator()` |
| `ListIterator<E> listIterator(int index)` | `boolean removeAll(Collection<?> c)` |
| `boolean removeIf(Predicate<? super E> filter)` | `protected void removeRange(int fromIndex, int toIndex)` |
| `void replaceAll(UnaryOperator<E> operator)` | `boolean retainAll(Collection<?> c)` |
| `void	sort(Comparator<? super E> c)` | `Spliterator<E>  spliterator()` |
| `List<E> subList(int fromIndex, int toIndex)` | `Object[] toArray()` |
| `<T> T[] toArray(T[] a)` | `void    trimToSize()` |

</div>


<p style="font-size:80%">(The two columns are not signficant; they they are divided into two columns
only for space reasons)</p>

<div markdown="1" >

| Inherited from | methods | more methods |
|----------------|---------|--------------|
| <strong>`class java.util.AbstractList`</strong> | `bool equals(Object o)` | `int hashCode()` |
| <strong>`class java.util.AbstractCollection`</strong> | `boolean containsAll(Collection<?> c)` | `String toString()` |
| <strong>`class java.lang.Object` </strong>| `void finalize() throws Throwable` <br> `final Class<?> getClass()` <br> `final void notify()` <br > `final void notifyAll()` | `final void wait()`<br>&nbsp;&nbsp;`throws InterruptedException` <br > `final void wait(long timeout)`<br>&nbsp;&nbsp;`throws InterruptedException`,<br >`final void wait(long timeout,int nanos)`<br>&nbsp;&nbsp;`throws InterruptedException`|

</div>

</div>

