---
title: Portabilidad de listas de presentación
description: La implementación de OpenGL de las listas de visualización es similar a la implementación de la contabilidad de IRIS, con dos excepciones en OpenGL no se pueden editar las listas de visualización una vez creadas y no se pueden llamar a funciones desde las listas de visualización.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Migración de la contabilidad de IRIS, mostrar listas
- trasladar de IRIS GL, mostrar listas
- trasladar a OpenGL desde IRIS GL, mostrar listas
- Exportación de OpenGL desde IRIS GL, mostrar listas
- Mostrar listas, trasladar de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356808"
---
# <a name="porting-display-lists"></a>Portabilidad de listas de presentación

La implementación de OpenGL de las listas de visualización es similar a la implementación de la contabilidad de IRIS, con dos excepciones: en OpenGL no se pueden editar listas de visualización una vez creadas y no se puede llamar a funciones desde las listas de visualización.

Dado que no puede editar ni llamar a funciones desde las listas de visualización, estas funciones de la contabilidad de IRIS no tienen ningún equivalente en OpenGL:

-   **editobj**
-   **objdelete**, **objinsert** y **objreplace**
-   **maketag**, **gentag**, **ISTAG** y **DelTag**
-   **callfunc**

En IRIS GL, se usan las funciones **Makeobj** y **closeobj** para crear listas de visualización. En OpenGL, se usa [**glNewList**](glnewlist.md) y [**glEndList**](glendlist.md).

En la tabla siguiente se enumeran las funciones de lista de visualización de IRIS GL con sus funciones de OpenGL equivalentes.



| Función de GL de IRIS | Función OpenGL                                                      | Significado                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | Crea una nueva lista de visualización.                                   |
| **closeobj**     | **glEndList**                                                        | Señala el final de la lista de visualización.                                  |
| **callobj**      | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Ejecuta Mostrar lista o listas.                               |
| **isobj**        | [**glIsList**](glislist.md)                                         | Comprueba la existencia de la lista de visualización.                             |
| **delobj**       | [**glDeleteLists**](gldeletelists.md)                               | Elimina un grupo contiguo de listas de presentación.                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | Genera el número especificado de listas de presentación vacías contiguas. |



 

En este tema se incluye información sobre lo siguiente.

-   [Trasladar la función bbox2](porting-the-bbox2-function.md)
-   [Trasladar listas de visualización editadas](porting-edited-display-lists.md)
-   [Un puerto de ejemplo de una lista de visualización](a-sample-port-of-a-display-list.md)

 

 




