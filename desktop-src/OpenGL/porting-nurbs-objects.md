---
title: Porte de objetos DE BASE DE DATOS
description: OpenGL trata ASEBS como objetos, de forma similar a la forma en que trata los cuádigos, se crea un objeto DE LABS y, a continuación, se especifica cómo se debe representar. En la tabla siguiente se enumeran las funciones GLU de OpenGL para administrar objetos DE LABS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Porte de IRIS GL, objetos DE LABS
- porte de objetos IRIS GL,GLBS
- porte a OpenGL desde objetos IRIS GL,GLBS
- Porte de OpenGL desde objetos IRIS GL,GLBS
- Objetos DE LA BASE DE DATOS
- SPLINEBS (B-spline no uniforme lógica)
- Spline B no uniforme lógica (SPLINE) (SPLINEBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074006"
---
# <a name="porting-nurbs-objects"></a>Porte de objetos DE BASE DE DATOS

OpenGL trata ASEBS como objetos, de forma similar a la forma en que trata los cuádigos: se crea un objeto GAMMABS y, a continuación, se especifica cómo se debe representar. En la tabla siguiente se enumeran las funciones GLU de OpenGL para administrar objetos DE LABS.



| Función GLU de OpenGL                                      | Significado                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | Crea un nuevo objeto RECORDSETBS.                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | Elimina un objeto DESPRBS.                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | Asocia una devolución de llamada a un objeto RECORDSETBS para el control de errores. |



 

Al portear el código DE IRIS GL LOBS a OpenGL, tenga en cuenta los siguientes puntos:

-   Los puntos de control DE LABS son flotantes, no dobles.
-   El parámetro stride se cuenta en floats, no en bytes.
-   Si usa iluminación y no especifica normales, llame a [**glEnable**](glenable.md) con GL AUTO NORMAL como parámetro para generar \_ \_ normales automáticamente.

??

 

 




