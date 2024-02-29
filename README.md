# Azuregold242
Tokenization of Azure Group of Companies Ltd to develop the Islands of the Bahamas. 
The AzureGold242 token (ATG20) is an ERC20 token on the Ethereum blockchain. It has a total supply of 1,000,000 ATG20 and a circulating supply of 500,000 ATG20. The token was created on July 28, 2023 by the address 0xe3152d33c08807ba9c301c5110e78b9203137c0c¹. The token has been traded on some decentralized exchanges (DEXs) such as Uniswap and SushiSwap. The current price of ATG20 is $0.0024 USD, based on the last trade on Uniswap on August 4, 2023². The token has a low trading volume and liquidity, which means it may be subject to high price volatility and slippage. You can find more information about the token and its smart contract calls on Bitquery¹³ and Bloxy².

Source: Conversation with Bing, 29/08/2023
(1) AzureGold242 (ATG20) ERC20 Token Analytics | Ethereum Mainnet | Bitquery. https://explorer.bitquery.io/ethereum/token/0xe3152d33c08807ba9c301c5110e78b9203137c0c.
(2) Trades for AzureGold242 token - Bloxy. https://bloxy.info/token_trades/0xe3152d33c08807ba9c301c5110e78b9203137c0c.
(3) AzureGold242 (ATG20) ERC20 Token Smart Contracts calls | Ethereum Mainnet. https://explorer.bitquery.io/ethereum/token/0xe3152d33c08807ba9c301c5110e78b9203137c0c/calls_contracts.
http://www.azuregold242.com

"New Project"

#include <stdio.h>
#include <stdlib.h>

// Define the structure for a node
struct Node {
    int data;
    struct Node* next;
};

// Function to create a new node
struct Node* createNode(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;
    return newNode;
}

// Function to insert a node at the beginning
void insertAtBeginning(struct Node** head, int value) {
    struct Node* newNode = createNode(value);
    newNode->next = *head;
    *head = newNode;
}

// Function to insert a node at the end
void insertAtEnd(struct Node** head, int value) {
    struct Node* newNode = createNode(value);
    if (*head == NULL) {
        *head = newNode;
        return;
    }
    struct Node* temp = *head;
    while (temp->next != NULL) {
        temp = temp->next;
    }
    temp->next = newNode;
}

// Function to delete a node with a given value
void deleteNode(struct Node** head, int value) {
    struct Node* temp = *head;
    struct Node* prev = NULL;
    while (temp != NULL && temp->data != value) {
        prev = temp;
        temp = temp->next;
    }
    if (temp == NULL) {
        printf("Node with value %d not found.\n", value);
        return;
    }
    if (prev == NULL) {
        *head = temp->next;
    } else {
        prev->next = temp->next;
    }
    free(temp);
}

// Function to find a node with a given value
struct Node* findNode(struct Node* head, int value) {
    struct Node* temp = head;
    while (temp != NULL) {
        if (temp->data == value) {
            return temp;
        }
        temp = temp->next;
    }
    return NULL;
}

// Function to display the linked list
void display(struct Node* head) {
    struct Node* temp = head;
    while (temp != NULL) {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    printf("NULL\n");
}

int main() {
    struct Node* head = NULL;

    insertAtBeginning(&head, 3);
    insertAtBeginning(&head, 2);
    insertAtBeginning(&head, 1);

    insertAtEnd(&head, 4);
    insertAtEnd(&head, 5);

    printf("Linked list: ");
    display(head);

    deleteNode(&head, 3);
    printf("After deleting 3: ");
    display(head);

    struct Node* foundNode = findNode(head, 4);
    if (foundNode != NULL) {
        printf("Node with value 4 found.\n");
    } else {
        printf("Node with value 4 not found.\n");
    }

    return 0;
}

"www.azuregold242.com"
