Spec:

TODO:
1. Generate random G1/G2/GT generator. [DONE]
2. Generate deterministic G1/G2/GT from string.
3. pairings(G1,G2) [DONE]
4. Functions for multiplication and exponentiation of G1/G2/GT elememts
5. Generate random field element. [DONE]
6. Addition and multiplication of field elements. [DONE]
7. Exponentiation function that exponentiates a G1/G2/GT element by a field element.



#### Example

```python
In [1]: from pypairing import PyG1, PyG2, PyFq12
In [2]: g1 = PyG1(0x5dbe6259, 0x8d313d76, 0x3237db17, 0xe5bc0654)
In [3]: g2 = PyG2(0x5dbe6259, 0x8d313d76, 0x3237db17, 0xe5bc0654)
In [4]: fq12 = PyFq12()
In [6]: g1.py_pairing_with(g2, fq12)
In [7]: b = PyFq12()
In [8]: b.rand(0x5dbe6259, 0x8d313d76, 0x3237db17, 0xe5bc0654)
In [9]: b.mul_assign(fq12)
In [11]: b.__str__()
Out[11]: 'Fq12(Fq6(Fq2(Fq(0x02bf4c754e414a36c683522b12644a81cd10514fbfc53699185dd1df6315260ee0fb6edfff0d1ed1ffabd27bf6e9a266) + Fq(0x1828d48a8505bb9a2ecc7386035878725aa9f4eb926a1e661f9382e1c9b7e41352735e190994f3e2b48d3906d778f5c2) * u) + Fq2(Fq(0x0164ffa9d4b179856185c883f0bbfab8fa7cabbdceee861314cae9938b31378f2f1ba1288e7d04102a44509a15b19ea1) + Fq(0x0bf20f53d1bbbb5fdfcbfa8c76d42593770ef40c44dbab1624e0f4be5678ccd04b319a1714a254053cce642b472a6747) * u) * v, Fq2(Fq(0x017b90314d6950a7b523e32e6c746614604a975111d863611398fe9c015c8b8129f64c3a808d37a2b477c7d3419f7c26) + Fq(0x19e4e7f65a35e86e5c81afc0c34683bde6d311eef12e3737d1ca7a12d086f4cc0bbde714482eac5b8f0c4c8257b06d5b) * u) * v^2) + Fq6(Fq2(Fq(0x008a14dd442f97eed9f108b166efaeeae5b486a44042a799f71ef0c38efd9f1135d5a8ceffc18d4cd93155455bd8b6f4) + Fq(0x0369715cac97216f930a2507aa5aaf0b17e2e194a8f3b6f846fa95f2cab62dc3e66c61d3f076e0af0bb34b870c36eea5) * u) + Fq2(Fq(0x0239c17cbdc164ecfb1d7d45fb3456ec3365390ed86dd78af7f2884c9ac85359416278eb6ebae7f3c4de38e41f42e5d7) + Fq(0x061a02c2c70e342d947c1dde49711b4c3569d5c48e97421e8b31d7b2b80ac29154085c05cd1a70686f9a34ac16b3722d) * u) * v, Fq2(Fq(0x16ad16a4c3eb4cd036001d4de022eec7da96f081c6d01142b7699e44ff588b4db18693fa13dbd3a93919dabe6415b0ea) + Fq(0x038fbe30d8c47b65682a9574ac5112ca747c283d1593b9bd76806c7211173f23b4e6ab6829046bf5a13e25586ec17701) * u) * v^2) * w)'
```
