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
ms.openlocfilehash: 2c1ed55fb60e3e7f42418e5bdfea48c1e298af34e9a7d76df17dfa7a021b3f50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024245"
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

Estos son algunos ejemplos:


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



Un vector también se puede declarar mediante esta sintaxis:


```
vector <Type, Number> VariableName
```



Estos son algunos ejemplos:


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





