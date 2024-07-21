#include <stdio.h>
#include <stdlib.h>
 
// Definition of a node in the binary search tree
typedef struct Node {
    int data;
    struct Node* left;
    struct Node* right;
} Node;
 
// Function to create a new node
Node* createNode(int data) {
    Node* newNode = (Node*)malloc(sizeof(Node));
    newNode->data = data;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}
 
// Function to insert a node into the binary search tree
Node* insert(Node* root, int data) {
    if (root == NULL) {
        return createNode(data);
    }
    if (data < root->data) {
        root->left = insert(root->left, data);
    } else {
        root->right = insert(root->right, data);
    }
    return root;
}
 
// In-order traversal: left-root-right
void inorderTraversal(Node* root) {
    if (root != NULL) {
        inorderTraversal(root->left);
        printf("%d ", root->data);
        inorderTraversal(root->right);
    }
}
 
// Pre-order traversal: root-left-right
void preorderTraversal(Node* root) {
    if (root != NULL) {
        printf("%d ", root->data);
        preorderTraversal(root->left);
        preorderTraversal(root->right);
    }
}
 
// Post-order traversal: left-right-root
void postorderTraversal(Node* root) {
    if (root != NULL) {
        postorderTraversal(root->left);
        postorderTraversal(root->right);
        printf("%d ", root->data);
    }
}
 
int main() {
    Node* root = NULL;
 
    // Inserting nodes into the binary search tree
    int values[] = {45, 15, 79, 90, 10, 55, 12, 20, 50};
    for (int i = 0; i < sizeof(values) / sizeof(values[0]); i++) {
        root = insert(root, values[i]);
    }
 
    // Performing in-order traversal
    printf("In-order traversal of the binary search tree:\n");
    inorderTraversal(root);
    printf("\n");
 
    // Performing pre-order traversal
    printf("Pre-order traversal of the binary search tree:\n");
    preorderTraversal(root);
    printf("\n");
 
    // Performing post-order traversal
    printf("Post-order traversal of the binary search tree:\n");
    postorderTraversal(root);
    printf("\n");
 
    return 0;
}