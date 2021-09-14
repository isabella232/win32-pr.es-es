---
title: Porte de curvas de recorte
description: Las curvas de recorte openGL son muy similares a las curvas de recorte de IRIS GL. En la tabla siguiente se enumeran las funciones GL de IRIS para definir curvas de recorte y sus funciones OpenGL equivalentes.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Porte de IRIS GL, recortar curvas
- porting from IRIS GL,trimming curves
- porte a OpenGL desde IRIS GL, recortar curvas
- Porte de OpenGL desde IRIS GL, recortar curvas
- curvas de recorte
- curvas
- Porte de IRIS GL, curvas
- porting from IRIS GL,curves
- porte a OpenGL desde IRIS GL, curvas
- Porte de OpenGL desde IRIS GL, curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362035"
---
# <a name="porting-trimming-curves"></a>Porte de curvas de recorte

Las curvas de recorte openGL son muy similares a las curvas de recorte de IRIS GL. En la tabla siguiente se enumeran las funciones GL de IRIS para definir curvas de recorte y sus funciones OpenGL equivalentes.



| Función IRIS GL | Función OpenGL                        | Significado                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Comienza la definición de la curva de recorte.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Define una curva lineal por fragmentos.    |
| **ybscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Especifica atributos de curva de recorte. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Finaliza la definición de la curva de recorte.      |



 

??

 

 




