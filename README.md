# chenpanping.github.io
chenpanping的个人博客
hello world
welcome to the China


![歪歪](https://github.com/chenpanping/chenpanping.github.io/assets/117699013/6b415485-c720-4445-bd29-ab4ab62ac6b8)
初学二叉树，二叉树的建立过程  
#define _CRT_SECURE_NO_WARNINGS  
#include<iostream>  
using namespace std;  
typedef struct Tree  
{  
	int data;  
	struct Tree* left;  
	struct Tree* right;  
}Tree,*BitTree;  

BitTree CreatTree()  
{  
	int x;  
	int temp;  
	BitTree T;  
	scanf("%d", &x);  
	temp = getchar();  
	if (x == -1)  
		return NULL;  
	else  
	{  
		T = new struct Tree;  
		T->data = x;  
		printf("请输入%d的左子树\n", x);  
		T->left = CreatTree();  
		printf("请输入%d的右子树\n", x);  
		T->right = CreatTree();  
		return T;  
	}  

}  

void preorder(BitTree T)  
{  
	if (T == NULL)  
		return;  
	printf("%d ", T->data);  
	preorder(T->left);  
	preorder(T->right);  
}  
int main()  
{  
	BitTree S;  
	printf("请输入根结点\n");  
	S = CreatTree();  
	preorder(S);  
	return 0;  

}  
