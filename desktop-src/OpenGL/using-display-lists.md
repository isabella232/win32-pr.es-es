---
title: Usar listas para mostrar
description: Usar listas para mostrar
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, mostrar listas
- mostrar listas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322721868f3bf994382a7604aa2cb76802f268aec7a1298aaa14e3066d5f6cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932805"
---
# <a name="using-display-lists"></a>Usar listas para mostrar

Una lista de visualización es un grupo de funciones de OpenGL que se han almacenado para su posterior ejecución. La [**función glNewList**](glnewlist.md) comienza la creación de una lista de visualización y [**glEndList**](glendlist.md) la finaliza. Con pocas excepciones, las funciones openGL llamadas entre **glNewList** y **glEndList** se anexan a la lista de visualización. (Vea **glNewList para** obtener una lista de las funciones que no se pueden almacenar y ejecutar desde dentro de una lista de visualización). Para desencadenar la ejecución de una lista o un conjunto de listas, use [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) y proporcione el número de identificación de una lista o listas determinadas. Los índices usados para identificar las listas de visualización se administran [**con glGenLists,**](glgenlists.md) [**glListBase**](gllistbase.md)y [**glIsList.**](glislist.md) Para eliminar un conjunto de listas para mostrar, use [**glDeleteLists**](gldeletelists.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de listas para mostrar](display-lists-reference.md)
</dt> </dl>

 

 




