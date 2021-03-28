---
description: Los registros de spline representan las curvas cuadráticas (es decir, las splines de b cuadrática) utilizadas por TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Registros de spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813028"
---
# <a name="spline-records"></a>Registros de spline

Los registros de spline representan las curvas cuadráticas (es decir, las splines de b cuadrática) utilizadas por TrueType. Un registro de spline comienza con el último punto del registro anterior (o para el primer registro del contorno, con el punto inicial). En el primer registro de spline, el punto inicial y el último punto del registro se encuentran en el contorno del glifo. En el caso de todos los demás registros de spline, solo el último punto está en el contorno del glifo. Todos los demás puntos de los registros de spline están fuera del contorno del glifo y deben representarse como puntos de control de las splines b.

El último registro de spline o Polyline de un contorno finaliza siempre con el punto inicial del contorno. Esta disposición garantiza que todos los contornos estén cerrados.

Dado que las splines b requieren tres puntos (un punto en el contorno del glifo entre dos puntos que se encuentran en el contorno), debe realizar algunos cálculos cuando un registro de spline contiene más de un punto fuera de curva.

Por ejemplo, si un registro de spline contiene tres puntos (A, B y C) y no es el primer registro, los puntos A y B están fuera del contorno del glifo. Para interpretar el punto A, use la posición actual (que siempre está en el contorno del glifo) y el punto en el contorno del glifo entre los puntos A y B. Para buscar el punto medio (M) entre A y B, puede realizar el cálculo siguiente.

M = A + (B A)/2

El punto medio entre los puntos no contornos consecutivos en un registro de spline es un punto en el contorno del glifo, de acuerdo con la definición del formato de spline usado en las fuentes TrueType.

Si la posición actual se designa mediante P, las dos curvas spline cuadráticas definidas por este registro de spline son (P, A, M) y (M, B, C).

 

 



