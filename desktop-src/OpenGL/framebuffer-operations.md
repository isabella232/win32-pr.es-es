---
title: Operaciones de fotogramas
description: Para seleccionar el búfer en el que se escriben los valores de color, use glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Canalización de procesamiento de OpenGL, operaciones fotogramas
- framebuffers, operaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531983"
---
# <a name="framebuffer-operations"></a>Operaciones de fotogramas

Para seleccionar el búfer en el que se escriben los valores de color, use [**glDrawBuffer**](gldrawbuffer.md). Se usan cuatro funciones diferentes para enmascarar la escritura de bits en cada una de las framebuffers lógicas después de que se hayan realizado todas las operaciones por fragmento:

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

La función [**glAccum**](glaccum.md) controla el funcionamiento del búfer de acumulación. Por último, [**glClear**](glclear.md) establece cada píxel de un subconjunto especificado de los búferes en el valor especificado con [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)o [**glClearAccum**](glclearaccum.md).

 

 




