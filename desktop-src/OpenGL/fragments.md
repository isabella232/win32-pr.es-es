---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL,fragments
- Canalización de procesamiento de OpenGL, fragmentos
- fragmentos de OpenGL
- framebuffers,fragments modifying pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab5d4124445455e518e4f091730e6e38e899442785b9f86ef73a230b99fbd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082415"
---
# <a name="fragments"></a>Fragments

Un fragmento generado por la rasterización modifica el píxel correspondiente en el búfer de fotogramas solo si supera las siguientes pruebas:

-   [Prueba de propiedad de píxeles](pixel-ownership-test.md)
-   [Prueba de la indesa](scissor-test.md)
-   [Prueba alfa](alpha-test.md)
-   [Prueba de galería de símbolos](stencil-test.md)
-   [Prueba de búfer de profundidad](depth-buffer-test.md)

Si se pasa, los datos del fragmento pueden reemplazar los valores de framebuffer existentes, o bien puede combinarlos con datos existentes en el búfer de fotogramas, en función del estado de determinados modos. Puede combinar el fragmento con los datos del búfer de fotogramas mediante:

-   [Mezcla](blending.md)
-   [Tramado](dithering.md)
-   [Operaciones lógicas](logical-operations.md)

 

 




