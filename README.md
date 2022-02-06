# Merge Sort Projesi

## Proje 2

`[16,21,11,8,12,22]` --> Merge Sort

1.  Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
2.  Big-O gösterimini yazınız.

---

1. Aşamaları:

```mermaid
flowchart LR
    subgraph Birinci Adım
        16,21,11,8,12,22
        end
    subgraph İkinci Adım
        16,21,11,8,12,22 --> 16,21,11
        16,21,11,8,12,22 --> 8,12,22
        end
    subgraph Üçüncü Adım
        16,21,11 --> 16
        16,21,11 --> 21,11
        8,12,22 --> 8
        8,12,22 --> 12,22
        end
    subgraph Dördüncü Adım
        21,11 --> 21
        21,11 --> 11
        12,22 --> 12
        12,22 --> 22
        end
    subgraph Beşinci Adım
        16 --> 11,16,21-merged[11,16,21]
        11 --> 11,16,21-merged[11,16,21]
        21 --> 11,16,21-merged[11,16,21]
        12 --> 8,12,22-merged[8,12,22]
        22 --> 8,12,22-merged[8,12,22]
        8 --> 8,12,22-merged[8,12,22]
        end
    subgraph Altıncı Adım
        11,16,21-merged[11,16,21]-->8,11,12,16,21,22
        8,12,22-merged[8,12,22]-->8,11,12,16,21,22
        end

```

2.  Merge Sort Big-O: $O(n*\log n)$
