---
description: Curvas de parámetro
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curvas de parámetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152501"
---
# <a name="parameter-curves"></a>Curvas de parámetro

Los parámetros multimedia pueden seguir una curva a lo largo del tiempo. Cada curva se describe mediante una fórmula matemática y dos puntos de conexión. Cada extremo se define mediante un tiempo de referencia y el valor de la curva en ese momento. La fórmula se usa para calcular valores intermedios entre los puntos y determina la forma de la curva. Las curvas posibles son:

-   Avanzar
-   Lineal
-   Square
-   Cuadrado inverso
-   Seno

"Salto" significa saltar directamente al valor final. Las demás curvas se muestran en el diagrama siguiente.

![curvas de parámetro](images/param-curves01.png)

Matemáticamente, las curvas funcionan como se indica a continuación. Supongamos que una curva comienza en el momento *t*₀ con un valor de *v*₀ y termina en el tiempo *t*₁ con un valor de *v*₁. Los dos puntos que definen la curva son (*t*₀, *v*₀) and (*t*₁, *v*₁).

-   Deje que Δ *t* sea la duración total de la curva, *t*₁ –*t*₀.
-   Permita que Δ *v* sea el intervalo entre los valores inicial y final, *v*₁ –*v*₀.
-   En cualquier momento *t* como t *₀ <*= *t*  <=  *t*₁, deje Δ *t*' = *t*–*t*₀.

![cálculo del parámetro](images/param-curves02.png)

El valor del parámetro en el momento *t* es:

*v* = f (Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀

donde f (x) es una función determinada por el tipo de curva:

-   Lineal: y = x
-   Cuadrado: y = x ^ 2
-   Cuadrado inverso: y = sqrt (x)
-   Seno: y = \[ sin (πx – π/2) + 1 \] /2

Observe que Δ *t*' < Δ t, por lo que el término Δ *t*'/Δ *t* oscila entre *0 y 1*. Por lo tanto, f (x) también oscila entre 0 y 1, y *v* siempre cae entre *v*₀ y *v*₁. Esto es así si *v*₀ < *v*₁ o viceversa. En otras palabras, la curva está limitada por el rectángulo (*t*₀, *v*₀, *t*₁, *v*₁).

En el caso de la curva sinusoidal, el valor de (πx – π/2) va de – π/2 a π/2, lo que significa que sin (πx – π/2) oscila entre – 1 y 1. A continuación, el resultado se normaliza de modo que f (x) caiga en el intervalo (0 – 1).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 



