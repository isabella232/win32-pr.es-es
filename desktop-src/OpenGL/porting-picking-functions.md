---
title: Porting Picking Functions
description: Todas las funciones de selección de IRIS GL tienen equivalentes openGL, a excepción de clearhitcode. En la tabla siguiente se enumeran las funciones de selección de IRIS GL y sus funciones openGL equivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Porte de IRIS GL, selección
- porting from IRIS GL,picking
- porting to OpenGL from IRIS GL,picking
- Porte de OpenGL desde IRIS GL, selección
- Recogiendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074003"
---
# <a name="porting-picking-functions"></a>Porting Picking Functions

Todas las funciones de selección de IRIS GL tienen equivalentes openGL, a excepción **de clearhitcode**. En la tabla siguiente se enumeran las funciones de selección de IRIS GL y sus funciones openGL equivalentes.



| Función IRIS GL                | Función OpenGL                                                                           | Significado                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | No compatible.                                                                            | Borra la variable global y el código de acceso.    |
| **selección de selección**<br/>       | [**glRenderMode**](glrendermode.md) ( GL \_ SELECT )                                       | Cambia al modo de selección o selección. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( GL \_ RENDER )                                       | Cambia al modo de representación.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Establece la matriz de devolución.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Para obtener más información sobre la selección, [**vea gluPickMatrix**](glupickmatrix.md).

 

 





