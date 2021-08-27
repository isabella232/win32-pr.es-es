---
title: Operaciones del búfer de fotogramas
description: Para seleccionar el búfer en el que se escriben los valores de color, use glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Canalización de procesamiento openGL, operaciones de búfer de fotogramas
- framebuffers,operations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ad9d3bb04d9c063ecd9ec588843577cc577bbe62f686f136a40cdaddcbfc77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082335"
---
# <a name="framebuffer-operations"></a>Operaciones del búfer de fotogramas

Para seleccionar el búfer en el que se escriben los valores de color, use [**glDrawBuffer**](gldrawbuffer.md). Se usan cuatro funciones diferentes para enmascarar la escritura de bits en cada uno de los búferes de fotogramas lógicos después de que se hayan realizado todas las operaciones por fragmento:

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

La [**función glAccum**](glaccum.md) controla el funcionamiento del búfer de acumulación. Por último, [**glClear**](glclear.md) establece cada píxel de un subconjunto especificado de los búferes en el valor especificado con [**glClearColor**](glclearcolor.md), [**glClearIndex,**](glclearindex.md) [**glClearDepth,**](glcleardepth.md) [**glClearStencil**](glclearstencil.md)o [**glClearAccum**](glclearaccum.md).

 

 




