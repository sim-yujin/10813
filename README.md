# 10813
#include <stdio.h>

int main() {
    int n, m;
    int baskets[101];
    scanf("%d %d", &n, &m);

    // 바구니에 초기값 할당
    for (int i = 1; i <= n; i++) {
        baskets[i] = i;
    }

    // 공 교환
    for (int i = 0; i < m; i++) {
        int a, b;
        scanf("%d %d", &a, &b);
        int temp = baskets[a];
        baskets[a] = baskets[b];
        baskets[b] = temp;
    }

    // 바구니 출력
    for (int i = 1; i <= n; i++) {
        printf("%d ", baskets[i]);
    }
    printf("\n");
    return 0;
}
