# sort-a-stack
void sortedInsert(stack<int>&s,int x)
{
    if(s.empty())
    {
        s.push(x);
        return;
    }
    else{
        if(s.top()>x)
        {
            int top=s.top();
            s.pop();
            sortedInsert(s,x);
            s.push(top);
        }
        else{
            s.push(x);
            return;
        }
    }
}
void SortedStack :: sort()
{
   //Your code here
 if(s.empty())
 {
     return;
     
 }
 else{
     int top=s.top();
     s.pop();
     sort();
     sortedInsert(s,top);
 }
}
