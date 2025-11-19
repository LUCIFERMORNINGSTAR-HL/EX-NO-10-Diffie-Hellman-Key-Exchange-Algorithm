# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1. Diffie-Hellman Key Exchange is used for securely sharing a secret key between two parties over an insecure channel.

2. Initialization: Agree on a large prime number \( p \) and a primitive root \( g \) modulo \( p \) (both are public values).

3. Key Exchange Process: 
   - Each party selects a private key and calculates their public key using the formula \( g^{\text{private key}} \mod p \).
   - Each party then shares their public key with the other.

4. Secret Key Computation: 
   - Each party computes the shared secret key using the received public key and their own private key.

5. Security: The difficulty of computing discrete logarithms ensures that the shared key remains secure even if public values are intercepted.

## Program:
```python
# Diffie-Hellman Key Exchange (Simple Example)

# Public numbers (shared openly)
p = 23     # prime number
g = 5      # primitive root

# --- Person A ---
a = 6                      # A's secret
A_pub = pow(g, a, p)       # g^a mod p

# --- Person B ---
b = 15                     # B's secret
B_pub = pow(g, b, p)       # g^b mod p

# Shared Secret Key (both MUST get same)
A_key = pow(B_pub, a, p)   # (g^b)^a mod p
B_key = pow(A_pub, b, p)   # (g^a)^b mod p

print("Public p:", p)
print("Public g:", g)

print("\nA sends:", A_pub)
print("B sends:", B_pub)

print("\nA's secret key:", A_key)
print("B's secret key:", B_key)
```

## Output:

<img width="401" height="287" alt="Screenshot 2025-11-19 112517" src="https://github.com/user-attachments/assets/461bd7ef-ed0d-48b6-9fc8-297962bc5d1e" />


## Result:
  The program is executed successfully

