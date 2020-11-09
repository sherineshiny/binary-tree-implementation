import java.util.Scanner;
class BTNode
{
 BTNode left,right;
 int data;
 public BTNode()
 {
  left=null;
  right=null;
  data=0;
  }
  public BTNode(int n)
  {
   left=null;
   right=null'
   data=n;
   }
   public void setLeft(BTNode n)
   {
    left=n;
    }
    public void setRight(BTNode n)
    {
     right=n;
     }
     public BTNode getLeft()
     {
      return left;
      }
      public BTNode getRight()
      {
       return right;
       }
       public void setData(int d)
       {
         data=d;
         }
       public int getData()
       {
         return data;
         }
        }
        class Bt
        {
         private BTNode root;
          public BT()
          {
           root=null;
           }
          public boolean isEmpty()
          {
           return root==null;
           }
           public void insert(int data)
           {
             root=insert(root,data);
           }
           private BTNode insert(BTNode node,int data)
           {
             if(node==null)
               node=new BTNode(data);
             else
             {
               if(node.getRight()==null)
                  node.right=insert(node.right,data);
                else
                 node.left=insert(node.left,data);
              }
              return node'
            }
            public int countNodes(BTNode r)
            {
              return countNodes(root);
             }
            private int countNodes(BTnode r)
            {
              if(r==null)
                 return 0;
              else
              {
                int l=1;
                l+=countNodes(r.getLeft());
                l+=countNodes(r.getRight());
                return l;
              }
             public boolean search(int val)
             {
               return search(root,val);
             }
             private boolean search(BTNode r,int val)
             {
               if(r.getData()==val)
                  return true;
               if(r.getLeft()!=null)
                 if(search(r.getLeft(),val))
                    return true;
                if(r.getRight()!=null)
                  if(search(r.getRight(),val))
                    return true;
                return false;
               }
             public void inorder()
             {
               inorder(root);
             }
             private void inorder(BTNode r)
             {
               if(r!=null)
               {
                 inorder(r.getLeft());
                 System.out.println(r.getData()+" ");
                 inorder(r.getRight());
               }
              }
            public void preorder()
            {
              preorder(root);
             }
            private void preorder(BTNode r)
            {
              if(r!=null)
               {
                 System.out.println(r.getData()+" ");
                 preorder(r.getLeft());
                 preorder(r.getRight());
               }
             }
             public void postorder()
             {
               postorder(root);
             }
             private void postorder(BTNode r)
             {
               if(r!=null)
               {
                postorder(r.getLeft());
                postorder(r.getRight());
                System.out.println(r.getData()+" ");
               }
              }
             }
             public class BinaryTree
             {
               public static void main(String[]args)
               {
                 Scanner in=new Scanner(System.in);
                 BT bt=new BT();
                 System.out.println("Binary Tree Test \n");
                 char ch;
                 do
                 {
                   System.out.println("Binary Tree operations \n");
                   System.out.println("1.Insert");
                   System.out.println("2.search");
                   System.out.println("3.count nodes");
                   System.out.println("4.check empty");
                   int choice=scan.nextInt();
                   switch(choice)
                   {
                    case 1:
                      System.out.println("\n enter integer element to insert");
                      bt.insert(scan.nextInt());
                      break;
                    case 2:
                      System.out.println("\n enter integer element to search");
                      System.out.println("\n search result:"+bt.search(scan.nextInt()));
                      break;
                    case 3:
                      System.out.println("Nodes="+bt.countNodes());
                      break;
                    case 4:
                      System.out.println("Empty status="+bt.Empty());
                      break;
                    default:
                      System.out.println("Wrong entry\n");
                      break;
                    }
                    System.out.println("\n post order:");
                    bt.postorder();
                    System.out.println("\n pre order:");
                    bt.preorder();
                    System.out.println("\n in order:");
                    bt.inorder();
                    System.out.println("\n Do you want to continue(Type y or n)\n");
                    ch=scan.next().charAt(0);
                    }while(ch=='Y'||ch=='y')
                   }
                  }
                  
                    
                    
                      
                 
