---
title: Porte de funciones de selección
description: Todas las funciones de selección de IRIS GL tienen equivalentes de OpenGL, a excepción de clearhitcode. En la tabla siguiente se enumeran las funciones de selección de IRIS GL y sus funciones OpenGL equivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Porte de IRIS GL, selección
- porting from IRIS GL,picking
- porting to OpenGL from IRIS GL,picking
- Porte de OpenGL desde IRIS GL, selección
- Recogiendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2cbeed54a18e7f1d3f26ec01dca2ad352aa4e190fbdc667ed75a60badec29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034815"
---
# <a name="porting-picking-functions"></a>Porte de funciones de selección

Todas las funciones de selección de IRIS GL tienen equivalentes de OpenGL, a excepción **de clearhitcode.** En la tabla siguiente se enumeran las funciones de selección de IRIS GL y sus funciones OpenGL equivalentes.



| Función GL de IRIS                | Función OpenGL                                                                           | Significado                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | No compatible.                                                                            | Borra la variable global y el código de acceso.    |
| **selección de selección**<br/>       | [**glRenderMode**](glrendermode.md) ( GL \_ SELECT )                                       | Cambia al modo de selección o selección. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( GL \_ RENDER )                                       | Cambia al modo de representación.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Establece la matriz de devolución.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Para obtener más información sobre la selección, [**vea gluPickMatrix**](glupickmatrix.md).

 

 





