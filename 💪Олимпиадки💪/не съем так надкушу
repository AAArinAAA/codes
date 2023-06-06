with open('Input.txt', 'r') as Inp:
    N, M = map(int, Inp.readline().split())
    C, S = [0] * M, [0] * M
    tree = [[float('inf') if i != j else 0 for j in range(N+1)] for i in range(N+1)]
    for i in range(N):
        K, L = map(int, Inp.readline().split())
        tree[K][i+1] = tree[i+1][K] = L
    for j in range(M):
        C[j], S[j] = map(int, Inp.readline().split())
    X, Z = map(int, Inp.readline().split())
for k in range(N+1):
    for i in range(N+1):
        for j in range(N+1):
            tree[i][j] = min(tree[i][k] + tree[k][j], tree[i][j])
[C.pop(x) and S.pop(x) for x in range(M) if S[x] < Z]
ans = 0
while C:
    aim = min([(tree[X][c], c) for c in C])
    ans += aim[0]
    X = aim[1]
    C.remove(aim[1])
with open('Output.txt', 'w') as Outp:
    Outp.write(str(ans))
