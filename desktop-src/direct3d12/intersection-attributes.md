---
title: Estructura de atributos de intersección
description: Estructura declarada en HLSL que representa los atributos de acierto para la intersección de triángulo de función fija o el rectángulo de selección alineado con el eje para la intersección de primitiva de procedimiento.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105717339"
---
# <a name="intersection-attributes-structure"></a>Estructura de atributos de intersección 

Estructura declarada en HLSL que representa los atributos de acierto para la intersección de triángulo de función fija o el rectángulo de selección alineado con el eje para la intersección de primitiva de procedimiento.

## <a name="fixed-function-triangle-intersection"></a>Intersección de triángulo de función fija

La siguiente estructura se declara en HLSL para representar los atributos de acierto para la intersección de triangulación de función fija:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Cualquier posicionamiento](any-hit-shader.md) y sombreadores de [posicionamiento más cercanos](closest-hit-shader.md) invocados mediante la intersección de triángulo de función fija debe utilizar esta estructura para los atributos de acceso. Determinados atributos a0, a1 y a2 para los 3 vértices de un triángulo, barycentrics. x es el peso de a1 y barycentrics. y es el peso de a2.  Por ejemplo, la aplicación puede interpolar haciendo lo siguiente: a = a0 + barycentrics. x * (a1-a0) + barycentrics. y * (a2 – a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Cuadro de límite alineado con el eje para la intersección de primitiva de procedimiento

Cuando se usan cuadros de límite alineados con el eje para la intersección con primitivas de procedimiento, se desencadena un sombreador de intersección.  Ese sombreador proporciona una estructura de atributo de intersección definida por el usuario a la llamada [**ReportHit**](reporthit-function.md) .  Los sombreadores de aciertos y de posicionamiento más cercanos enlazados al mismo grupo de visitas con este sombreador de intersección deben usar la misma estructura para los atributos de aciertos, incluso si no se hace referencia a los atributos.  El tamaño máximo de la estructura de atributo es de 32 bytes, definido como **D3D12 \_ RAYTRACING \_ Max \_ Attribute \_ size \_ en \_ bytes**.


