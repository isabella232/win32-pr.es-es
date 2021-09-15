---
title: Tipo de vector (HLSL)
description: Un vector contiene entre uno y cuatro componentes escalares; cada componente de un vector debe ser del mismo tipo.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Tipo de vector HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573752"
---
# <a name="vector-type"></a>Tipo de vector

Un vector contiene entre uno y cuatro componentes escalares; cada componente de un vector debe ser del mismo tipo.



|                     |
|---------------------|
| **Nombre typeNumber** |



 


```
TypeComponents Name
```



## <a name="components"></a>Componentes



| Elemento                                                                                                                             | Descripción                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Nombre único que contiene dos partes. La primera parte es uno de los [tipos escalares.](dx-graphics-hlsl-data-types.md) La segunda parte es el número de componentes, que deben estar entre 1 y 4 inclusive.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>                                         | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                                                                                                                                                |



 

## <a name="examples"></a>Ejemplos

A continuación se muestran algunos ejemplos:


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



Un vector también se puede declarar mediante esta sintaxis:


```
vector <Type, Number> VariableName
```



A continuación se muestran algunos ejemplos:


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





