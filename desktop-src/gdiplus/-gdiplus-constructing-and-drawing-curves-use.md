---
description: 'GDI+ admite varios tipos de curvas: elipses, arcos, splines cardinales y B&\# 233;splines zier.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Crear y dibujar curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78ebd7ce81099d5b7f483939c0f4b238d1f124357bf6e1863b25fedb7e22f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015225"
---
# <a name="constructing-and-drawing-curves"></a>Crear y dibujar curvas

GDI+ admite varios tipos de curvas: elipses, arcos, splines cardinales y splines de Bézier. Una elipse se define mediante su rectángulo delimitador; un arco es una parte de una elipse definida por un ángulo inicial y un ángulo de barrido. Una curva spline cardinal se define mediante una matriz de puntos y un parámetro de tensión: la curva pasa sin problemas a través de cada punto de la matriz y el parámetro de tensión influye en la forma en que la curva se curva. Una curva spline de Bézier se define mediante dos puntos de conexión y dos puntos de control: la curva no pasa a través de los puntos de control, pero los puntos de control influyen en la dirección y la curva a medida que la curva va de un punto de conexión al otro.

En los temas siguientes se tratan con más detalle las curvas spline cardinales y las splines de Bézier:

-   [Dibujar splines cardinales](-gdiplus-drawing-cardinal-splines-use.md)
-   [Dibujar curvas spline de Bézier](-gdiplus-drawing-bezier-splines-use.md)

 

 



