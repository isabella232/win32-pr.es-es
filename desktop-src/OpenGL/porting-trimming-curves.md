---
title: Trasladar curvas de recorte
description: Las curvas de recorte de OpenGL son muy similares a las curvas de recorte de la contabilidad de IRIS. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para definir curvas de recorte y sus funciones de OpenGL equivalentes.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Migración de la contabilidad de IRIS, curvas de recorte
- trasladar de IRIS GL, curvas de recorte
- trasladar a OpenGL desde IRIS GL, curvas de recorte
- Exportación de OpenGL desde IRIS GL, curvas de recorte
- curvas de recorte
- curvas
- Migración de la contabilidad de IRIS, curvas
- trasladar de IRIS GL, curvas
- trasladar a OpenGL desde IRIS GL, curvas
- Exportación de OpenGL de IRIS GL, curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269164"
---
# <a name="porting-trimming-curves"></a>Trasladar curvas de recorte

Las curvas de recorte de OpenGL son muy similares a las curvas de recorte de la contabilidad de IRIS. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para definir curvas de recorte y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS | Función OpenGL                        | Significado                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Comienza la definición de la curva de recorte.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Define una curva lineal a trozos.    |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Especifica los atributos de curva de recorte. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Finaliza la definición de curva de recorte.      |



 

??

 

 




