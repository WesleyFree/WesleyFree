- 👋 Hi, I’m @WesleyFree
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
WesleyFree/WesleyFree is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
graph TD
    A[开始] --> B{处理训练数据(data_train)}
    B --> C[调用set_missing_ages函数填充年龄缺失值]
    C --> D[获取已知年龄乘客数据known_age和未知年龄乘客数据unknown_age]
    D --> E[提取已知年龄乘客的年龄作为目标值y和其他特征作为X]
    E --> F[创建RandomForestRegressor并训练]
    F --> G[用训练好的模型预测未知年龄]
    G --> H[将预测年龄填充到原数据缺失处]
    H --> I[返回填充年龄后的数据和模型对象]
    I --> J[调用set_Cabin_type函数处理客舱类型]
    J --> K[将有客舱标记为"Yes"，无客舱标记为"No"]
    K --> L[返回处理后的训练数据]
    L --> M[对处理后的训练数据进行特征因子化]
    M --> N[对'Cabin'列进行独热编码生成dummies_Cabin]
    M --> O[对'Embarked'列进行独热编码生成dummies_Embarked]
    M --> P[对'Sex'列进行独热编码生成dummies_Sex]
    M --> Q[对'Pclass'列进行独热编码生成dummies_Pclass]
    N --> R[合并原始训练数据和各独热编码后的虚拟变量列]
    O --> R
    P --> R
    Q --> R
    R --> S[删除已进行独热编码处理的原始列]
    S --> T[查看处理后训练数据的前10行(data_train.head(10))]
    T --> U[结束]
