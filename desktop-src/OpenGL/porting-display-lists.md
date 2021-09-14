---
title: Porte de listas de presentación
description: La implementación de OpenGL de las listas de presentación es similar a la implementación de IRIS GL, con dos excepciones en OpenGL, no se pueden editar listas de visualización una vez que las haya creado y no se puedan llamar a funciones desde dentro de las listas de presentación.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Porte de IRIS GL, listas de visualización
- porting from IRIS GL,display lists
- porte a OpenGL desde IRIS GL, mostrar listas
- Porte de OpenGL desde IRIS GL, mostrar listas
- mostrar listas, porte desde IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169177"
---
# <a name="porting-display-lists"></a>Porte de listas de presentación

La implementación de OpenGL de las listas de presentación es similar a la implementación de IRIS GL, con dos excepciones: en OpenGL no se pueden editar listas de presentación una vez creadas y no se pueden llamar a funciones desde listas para mostrar.

Dado que no se pueden editar ni llamar a funciones desde dentro de las listas de visualización, estas funciones GL de IRIS no tienen ningún equivalente en OpenGL:

-   **editobj**
-   **objdelete,** **obobjsert** y **objreplace**
-   **maketag,** **gentag,** **istag** y **deltag**
-   **callfunc**

En IRIS GL, se usan las **funciones makeobj** y **closeobj** para crear listas de visualización. En OpenGL, se usa [**glNewList**](glnewlist.md) y [**glEndList.**](glendlist.md)

En la tabla siguiente se enumeran las funciones de lista de visualización de IRIS GL con sus funciones OpenGL equivalentes.



| Función GL de IRIS | Función OpenGL                                                      | Significado                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | Crea una nueva lista de visualización.                                   |
| **closeobj**     | **glEndList**                                                        | Indica el final de la lista de visualización.                                  |
| **callobj**      | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Ejecuta listas para mostrar.                               |
| **isobj**        | [**glIsList**](glislist.md)                                         | Comprueba la existencia de la lista de visualización.                             |
| **delobj**       | [**glDeleteLists**](gldeletelists.md)                               | Elimina el grupo contiguo de listas para mostrar.                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | Genera el número especificado de listas de visualización vacías contiguas. |



 

En este tema se incluye información sobre lo siguiente.

-   [Porte de la función bbox2](porting-the-bbox2-function.md)
-   [Porte de listas de presentación editadas](porting-edited-display-lists.md)
-   [Un puerto de ejemplo de una lista de visualización](a-sample-port-of-a-display-list.md)

 

 




