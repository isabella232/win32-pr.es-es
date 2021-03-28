---
title: numthreads
description: Define el número de subprocesos que se van a ejecutar en un único grupo de subprocesos cuando se envía un sombreador de cálculo (consulte ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421350"
---
# <a name="numthreads"></a>numthreads

Define el número de subprocesos que se van a ejecutar en un único grupo de subprocesos cuando se envía un sombreador de cálculo (vea [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



Los valores X, Y y Z indican el tamaño del grupo de subprocesos en una dirección determinada y el total de X \* y \* Z proporciona el número de subprocesos del grupo. La capacidad de especificar el tamaño del grupo de subprocesos en tres dimensiones permite tener acceso a los subprocesos individuales de una manera que sea lógicamente estructuras de datos 2D y 3D.

Por ejemplo, si un sombreador de cálculo está realizando la adición de matriz 4x4, numthreads podría establecerse en numthreads (4, 4, 1) y la indexación de los subprocesos individuales coincidiría automáticamente con las entradas de la matriz. El sombreador de cálculo también podría declarar un grupo de subprocesos con el mismo número de subprocesos (16) mediante numthreads (16, 1, 1), pero tendría que calcular la entrada de matriz actual en función del número de subproceso actual.

Los valores de parámetro permitidos para **numthreads** dependen de la versión del sombreador de cálculo.



| Sombreador de cálculo | Z como máximo | Número máximo de subprocesos (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| CS \_ 4 \_ x       | 1         | 768                       |
| CS \_ 5 \_ 0       | 64        | 1024                      |



 

En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo numthreads, numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso ([VP \_ GroupIndex](sv-groupindex.md),[VP \_ DispatchThreadID](sv-dispatchthreadid.md),[VP \_ GroupThreadID](sv-groupthreadid.md),[VP \_ GroupID](sv-groupid.md))

![Ilustración de la relación entre el envío, los grupos de subprocesos y los subprocesos](images/threadgroupids.png)

Este atributo es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 