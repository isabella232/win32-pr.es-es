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
- porting to OpenGL from IRIS GL,curves
- Porte de OpenGL desde IRIS GL, curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad544431adaa7f0b049341ec7314e3e53ae60752d633a48c760ca09334f79d33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553865"
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

 

 




