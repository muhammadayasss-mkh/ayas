using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // List
        List<int> list = new List<int>() { 1, 2, 3 };
        Console.WriteLine("List:");
        foreach (var i in list) Console.Write(i + " ");

        // HashSet
        HashSet<int> set = new HashSet<int>() { 1, 2, 2, 3 };
        Console.WriteLine("\nHashSet:");
        foreach (var i in set) Console.Write(i + " ");

        // Stack
        Stack<int> stack = new Stack<int>();
        stack.Push(10);
        stack.Push(20);
        Console.WriteLine("\nStack:");
        foreach (var i in stack) Console.Write(i + " ");

        // Queue
        Queue<int> queue = new Queue<int>();
        queue.Enqueue(100);
        queue.Enqueue(200);
        Console.WriteLine("\nQueue:");
        foreach (var i in queue) Console.Write(i + " ");

        // SortedSet
        SortedSet<int> sortedSet = new SortedSet<int>() { 5, 1, 3 };
        Console.WriteLine("\nSortedSet:");
        foreach (var i in sortedSet) Console.Write(i + " ");

        // LinkedList
        LinkedList<int> linkedList = new LinkedList<int>();
        linkedList.AddLast(7);
        linkedList.AddLast(9);
        Console.WriteLine("\nLinkedList:");
        foreach (var i in linkedList) Console.Write(i + " ");
    }
}



using System;
using System.Collections;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // ArrayList
        ArrayList arrayList = new ArrayList();
        arrayList.Add(1);
        arrayList.Add("Hello");
        Console.WriteLine("ArrayList:");
        foreach (var item in arrayList)
            Console.Write(item + " ");

        // Stack (non-generic)
        System.Collections.Stack stack = new System.Collections.Stack();
        stack.Push(10);
        stack.Push("Hi");
        Console.WriteLine("\nStack:");
        foreach (var item in stack)
            Console.Write(item + " ");

        // Queue (non-generic)
        System.Collections.Queue queue = new System.Collections.Queue();
        queue.Enqueue(100);
        queue.Enqueue("World");
        Console.WriteLine("\nQueue:");
        foreach (var item in queue)
            Console.Write(item + " ");
    }
}


using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        Console.Write("Enter sentence: ");
        string input = Console.ReadLine();

        string[] words = input.Split(' ');

        Dictionary<string, int> wordCount = new Dictionary<string, int>();

        foreach (string word in words)
        {
            if (wordCount.ContainsKey(word))
                wordCount[word]++;
            else
                wordCount[word] = 1;
        }

        Console.WriteLine("\nWord Frequency:");
        foreach (var pair in wordCount)
        {
            Console.WriteLine(pair.Key + " : " + pair.Value);
        }
    }
}
