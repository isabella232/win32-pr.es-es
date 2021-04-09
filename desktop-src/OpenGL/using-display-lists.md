---
title: Usar listas de visualización
description: Usar listas de visualización
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, mostrar listas
- Mostrar listas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903310"
---
# <a name="using-display-lists"></a>Usar listas de visualización

Una lista de visualización es un grupo de funciones OpenGL que se ha almacenado para su posterior ejecución. La función [**glNewList**](glnewlist.md) inicia la creación de una lista de visualización y [**glEndList**](glendlist.md) la finaliza. Con pocas excepciones, las funciones de OpenGL llamadas entre **glNewList** y **glEndList** se anexan a la lista de visualización. (Consulte **glNewList** para obtener una lista de las funciones que no se pueden almacenar y ejecutar desde dentro de una lista de visualización). Para desencadenar la ejecución de una lista o un conjunto de listas, use [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) y proporcione el número de identificación de una lista o listas determinadas. Los índices que se usan para identificar las listas de visualización se administran con [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)y [**glIsList**](glislist.md). Para eliminar un conjunto de listas de visualización, use [**glDeleteLists**](gldeletelists.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de listas de visualización](display-lists-reference.md)
</dt> </dl>

 

 




