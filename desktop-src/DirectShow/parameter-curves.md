---
description: Curvas de parámetros
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curvas de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5130cf158271ffe3cb3da5e4e16b5fffa8a5a6994b14b9f8766fe20cdf1510ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997394"
---
# <a name="parameter-curves"></a>Curvas de parámetros

Los parámetros multimedia pueden seguir una curva con el tiempo. Cada curva se describe mediante una fórmula matemática y dos puntos de conexión. Cada punto final se define mediante una hora de referencia y el valor de la curva en ese momento. La fórmula se usa para calcular los valores intermedios entre los puntos y determina la forma de la curva. Las curvas posibles son:

-   Saltar
-   Lineal
-   Square
-   Cuadrado inverso
-   Seno

"Salto" significa saltar directamente al valor final. Las demás curvas se muestran en el diagrama siguiente.

![curvas de parámetros](images/param-curves01.png)

Matemáticamente, las curvas funcionan de la siguiente manera. Supongamos que una curva comienza en el momento *₀* con un valor de *v*₀ y termina en el momento *₁* con un valor de *v*₁. Los dos puntos que definen la curva son (*t ₀,* *v*₀) y (*t*₁, *v*₁).

-   Deje que A *sea la* duración total de la curva, *t ₁–**t ₀.*
-   Deje que v *sea el* intervalo entre los valores inicial y final, *v*₁–*v*₀.
-   En cualquier *momento, para* que *t*₀ <= *t*  <=  *t ₁,* deje que A *t*' = *t*–*t*₀.

![cálculo de parámetros](images/param-curves02.png)

El valor del parámetro en el momento *t* es:

*v* = f( —*t '*/*—t ])* \* v *v*  +  *v*₀

donde f(x) es una función determinada por el tipo de curva:

-   Lineal: y = x
-   Cuadrado: y = x^2
-   Cuadrado inverso: y = sqrt(x)
-   Seno: y = \[ sin(πx – π/2) + \] 1/2

Observe que Y *t*" < A *t*, por lo que el término A *t "/* A *t"* va de 0 a 1. Por lo tanto, f(x) también oscila entre 0 y 1, y *v* siempre se encuentra entre *v*₀ *y v*₁. Esto es cierto si *v*₀ < *v*₁ o viceversa. En otras palabras, la curva está limitada por el rectángulo (*t*₀, *v*₀, *t*₁, *v*₁).

Para la curva seno, el valor de (πx – π/2) oscila entre –π/2 y π/2, lo que significa que sin(πx – π/2) oscila entre –1 y 1. A continuación, el resultado se normaliza para que f(x) entre en el intervalo (0-1).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 



