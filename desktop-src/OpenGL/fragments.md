---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, fragmentos
- Canalización de procesamiento de OpenGL, fragmentos
- fragmentos OpenGL
- framebuffers, fragmentos modificar píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676193"
---
# <a name="fragments"></a>Fragments

Un fragmento generado mediante la rasterización modifica el píxel correspondiente en el fotogramas solo si pasa las siguientes pruebas:

-   [Prueba de propiedad de píxeles](pixel-ownership-test.md)
-   [Prueba de tijera](scissor-test.md)
-   [Prueba alfa](alpha-test.md)
-   [Prueba de estarcido](stencil-test.md)
-   [Prueba de búfer de profundidad](depth-buffer-test.md)

Si se supera, los datos del fragmento pueden reemplazar los valores de fotogramas existentes o puede combinarlos con los datos existentes en el fotogramas, en función del estado de ciertos modos. Puede combinar el fragmento con datos en fotogramas por:

-   [Combinación](blending.md)
-   [Interpolación](dithering.md)
-   [Operaciones lógicas](logical-operations.md)

 

 




