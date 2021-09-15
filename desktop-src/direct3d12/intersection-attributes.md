---
title: Estructura de atributos de intersección
description: Estructura declarada en HLSL para representar atributos de acceso para la intersección del triángulo de función fija o el rectángulo de selección alineado con ejes para la intersección primitiva de procedimientos.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567996"
---
# <a name="intersection-attributes-structure"></a>Estructura de atributos de intersección 

Estructura declarada en HLSL para representar atributos de acceso para la intersección del triángulo de función fija o el rectángulo de selección alineado con ejes para la intersección primitiva de procedimientos.

## <a name="fixed-function-triangle-intersection"></a>Intersección de triángulo de función fija

La siguiente estructura se declara en HLSL para representar los atributos de llamada para la intersección del triángulo de función fija:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Los sombreadores de](any-hit-shader.md) impacto [y los](closest-hit-shader.md) más cercanos invocados mediante la intersección de triángulos de función fija deben usar esta estructura para los atributos de impacto. Dados los atributos a0, a1 y a2 para los tres vértices de un triángulo, barycentrics.x es el peso de a1 y barycentrics.y es el peso de a2.  Por ejemplo, la aplicación puede interpolarse haciendo: a = a0 + barycentrics.x * (a1-a0) + barycentrics.y* (a2 – a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Rectángulo de selección alineado con el eje para la intersección primitiva de procedimientos

Cuando se usan rectángulos delimitadores alineados con ejes para la intersección con primitivas de procedimientos, se desencadena un sombreador de intersección.  Ese sombreador proporciona una estructura de atributo de intersección definida por el usuario para la [**llamada a ReportHit.**](reporthit-function.md)  Los sombreadores de referencias y los más cercanos enlazados en el mismo grupo de referencias con este sombreador de intersección deben usar la misma estructura para los atributos de impacto, incluso si no se hace referencia a los atributos.  El tamaño máximo de la estructura de atributo es de 32 bytes, definido como **D3D12 \_ RAYTRACING \_ MAX ATTRIBUTE SIZE IN \_ \_ \_ \_ BYTES**.


