---
title: Trasladar funciones de picking
description: Todas las funciones de selección de la contabilidad de IRIS tienen equivalentes de OpenGL, con la excepción de clearhitcode. En la tabla siguiente se enumeran las funciones de picking de IRIS GL y sus funciones de OpenGL equivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Migración de la contabilidad de IRIS, picking
- portabilidad de IRIS GL, picking
- trasladar a OpenGL desde IRIS GL, picking
- Exportación de OpenGL desde IRIS GL, picking
- recogida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665693"
---
# <a name="porting-picking-functions"></a>Trasladar funciones de picking

Todas las funciones de selección de la contabilidad de IRIS tienen equivalentes de OpenGL, con la excepción de **clearhitcode**. En la tabla siguiente se enumeran las funciones de picking de IRIS GL y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                | Función OpenGL                                                                           | Significado                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | No se admite.                                                                            | Borra la variable global y hitcode.    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) (selección de libro \_ )                                       | Cambia a la selección o al modo de selección. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) (representación en GL \_ )                                       | Cambia al modo de representación.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Establece la matriz devuelta.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Para obtener más información sobre la selección, vea [**gluPickMatrix**](glupickmatrix.md).

 

 





