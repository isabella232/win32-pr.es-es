---
description: 'GDI+ admite varios tipos de curvas: elipses, arcos, curvas spline cardinales y B&\# 233; curvas spline de Bézier.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Crear y dibujar curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997521"
---
# <a name="constructing-and-drawing-curves"></a>Crear y dibujar curvas

GDI+ admite varios tipos de curvas: elipses, arcos, curvas spline cardinales y curvas spline de Bézier. Una elipse se define mediante su rectángulo delimitador; un arco es una parte de una elipse definida por un ángulo inicial y un ángulo de barrido. Una curva spline cardinal se define mediante una matriz de puntos y un parámetro de tensión: la curva se pasa sin problemas a través de cada punto de la matriz y el parámetro de tensión influye en la forma en que se curva la curva. Una curva spline de Bézier se define mediante dos puntos de conexión y dos puntos de control: la curva no pasa a través de los puntos de control, pero los puntos de control influyen en la dirección y el plegado a medida que la curva va de un extremo al otro.

En los temas siguientes se tratan las curvas spline cardinales y las curvas spline de Bézier con más detalle:

-   [Dibujar curvas spline cardinales](-gdiplus-drawing-cardinal-splines-use.md)
-   [Dibujar curvas spline de Bézier](-gdiplus-drawing-bezier-splines-use.md)

 

 



