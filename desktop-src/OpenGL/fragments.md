---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL,fragments
- Canalización de procesamiento openGL, fragmentos
- fragmentos de OpenGL
- framebuffers,fragmentos que modifican píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071509"
---
# <a name="fragments"></a>Fragments

Un fragmento generado por la rasterización modifica el píxel correspondiente en el búfer de fotogramas solo si supera las siguientes pruebas:

-   [Prueba de propiedad de píxeles](pixel-ownership-test.md)
-   [Prueba de deserción](scissor-test.md)
-   [Prueba alfa](alpha-test.md)
-   [Prueba de galería de símbolos](stencil-test.md)
-   [Prueba de búfer de profundidad](depth-buffer-test.md)

Si se pasa, los datos del fragmento pueden reemplazar los valores de búfer de fotogramas existentes, o bien puede combinarlos con los datos existentes en el búfer de fotogramas, en función del estado de determinados modos. Puede combinar el fragmento con datos en el búfer de fotogramas mediante:

-   [Mezcla](blending.md)
-   [Tramado](dithering.md)
-   [Operaciones lógicas](logical-operations.md)

 

 




