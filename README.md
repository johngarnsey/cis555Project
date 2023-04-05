# cis555Project
Merkle Hash Tree for Integrity Check of Files


L1, L2, L3 and L4 are files. Your program is supposed to compute Top Hash. You can choose to use MD5 or SHA1 for hashing. You can use source code of SHA1 or MD5 from the internet.

Input: Pathnames of files. There should be no upper bound on the number of files. Your program should be able to handle thousands of files.

Output: Compute Top Hash and demonstrate that Top Hash does not match when one or more files are modified.

Deliverables: 
•	Source code submission using github.
•	A printout of the output.

The following grading criteria will be applied: 
•	Correctness & Completeness 70% 
•	Program Output & Testing 15% 
•	Program Organization & Source Code Management 10% 
•	Documentation 5%



Documentation:


Sample code:
'''
>>> from merklelib import MerkleTree, beautify
>>> import hashlib
>>> hashfunc = lambda x: hashlib.sha256(str(x).encode()).hexdigest()
>>> tree = MerkleTree(get_data(), hashfunc)
>>> beautify(tree)
c9f33d24dd8e472976c0198b0f836b3874b5c6467eb23cc1adf7b687ac586498
├── d28b1b2d721c2ccc607af28cfbb419013bc942927d04392ee0c1dc2a9066a81d
│   ├── e8fe3173b1b0986b3d790924ff035f7180becf69bc1ffd169bf00f3282e0c24b
│   │   ├── 8da651a777f744d24c3dfe78e4aba4db4b38c0503b751976a1deca5791d4f104
│   │   └── 2793603d2dbc9ecb01075e8ee79c9705840bfde2d7e04ddfc952aea2ae46e79c
│   └── 677faacca2f4bf2c6ffcd46a7a1f1dfcf693399782072f9abf3c2c6a696e3a25
│       ├── 6ee8afcc0c19ab6c4193a332f862a85931093e425e417a598e9586c118fbcd47
│       └── 01849571e994a62e59b9ec206cd0bd979349d6462b6cc2ecb8c79b2da5132f51
└── 33f61b85350855f9b3f6b72ff82e69a13e5a9558257ac070a6ea0b4221993afa
    ├── 3b7ff0501fc23acda03364ff531814d0052958314774af33dda4bf7a0ab31de9
    │   ├── 7fc3c4c5ce8ddbe92d0cc088e16453a7de577ea2550e5c488b567e5405589cb9
    │   └── 125f0aa386a98c76a2da004a97c65f22a09604df1af359ef8998da3220214b0d
    └── a72b9a1cc7b60477746a12c0d94281878bf5475d0ae8b474dc614165f99dbe82
        ├── a18ae51c18a80e1d68422384fb497382059c64197267646e9eae863de83ec3ec
        └── f72db255ff769c583833da5417f460ea4af0c588e0c5291626e51726462ffb94
'''
        The Above is the output of the trees showing that it worked ---

