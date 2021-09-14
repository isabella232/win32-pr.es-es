---
title: numthreads
description: Define el número de subprocesos que se ejecutarán en un único grupo de subprocesos cuando se envía un sombreador de proceso (vea ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263876"
---
# <a name="numthreads"></a>numthreads

Define el número de subprocesos que se ejecutarán en un único grupo de subprocesos cuando se envía un sombreador de proceso (vea [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



Los valores X, Y y Z indican el tamaño del grupo de subprocesos en una dirección determinada y el total de X Y Z proporciona el número de subprocesos \* \* del grupo. La capacidad de especificar el tamaño del grupo de subprocesos en tres dimensiones permite tener acceso a subprocesos individuales de manera que las estructuras de datos 2D y 3D lógicamente.

Por ejemplo, si un sombreador de proceso realiza la adición de matriz 4x4, numthreads podría establecerse en numthreads(4,4,1) y la indexación en los subprocesos individuales coincidiría automáticamente con las entradas de la matriz. El sombreador de proceso también podría declarar un grupo de subprocesos con el mismo número de subprocesos (16) mediante numthreads(16,1,1), pero tendría que calcular la entrada de matriz actual en función del número de subproceso actual.

Los valores de parámetro permitidos para **numthreads** dependen de la versión del sombreador de proceso.



| Sombreador de proceso | Z máximo | Máximo de subprocesos (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| cs \_ 4 \_ x       | 1         | 768                       |
| cs \_ 5 \_ 0       | 64        | 1024                      |



 

En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo numthreads, numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos [(SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

Este atributo se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 