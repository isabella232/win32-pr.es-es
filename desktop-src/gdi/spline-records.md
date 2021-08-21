---
description: Los registros spline representan las curvas cuadráticas (es decir, b-splines cuadráticas) usadas por TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Registros spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbaf3730f327501bd55b2e35b9410f03fd0559cbb5e36d87a3052901d26e5f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613655"
---
# <a name="spline-records"></a>Registros spline

Los registros spline representan las curvas cuadráticas (es decir, b-splines cuadráticas) usadas por TrueType. Un registro spline comienza con el último punto del registro anterior (o para el primer registro del contorno, con el punto inicial). Para el primer registro spline, el punto inicial y el último punto del registro se encuentran en el contorno del glifo. Para todos los demás registros spline, solo el último punto está en el contorno del glifo. Todos los demás puntos de los registros spline están fuera del contorno del glifo y deben representarse como puntos de control de b-splines.

El último registro de spline o polilínea de un contorno siempre termina con el punto inicial del contorno. Esta disposición garantiza que se cierren todos los contornos.

Dado que b-splines requieren tres puntos (un punto fuera del contorno del glifo entre dos puntos que están en el contorno), debe realizar algunos cálculos cuando un registro spline contenga más de un punto fuera de curva.

Por ejemplo, si un registro spline contiene tres puntos (A, B y C) y no es el primer registro, los puntos A y B están fuera del contorno del glifo. Para interpretar el punto A, use la posición actual (que siempre está en el contorno del glifo) y el punto en el contorno del glifo entre los puntos A y B. Para buscar el punto medio (M) entre A y B, puede realizar el siguiente cálculo.

M = A + (B A)/2

El punto medio entre los puntos fuera de esquema consecutivos de un registro spline es un punto en el contorno del glifo, según la definición del formato spline utilizado en las fuentes TrueType.

Si la posición actual la designa P, las dos splines cuadráticas definidas por este registro spline son (P, A, M) y (M, B, C).

 

 



