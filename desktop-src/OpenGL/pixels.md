---
title: píxeles
description: Los fragmentos se convierten en píxeles en el búfer de fotogramas.
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL, píxeles
- Canalización de procesamiento openGL, píxeles
- pixels OpenGL
- framebuffers, convertir fragmentos en píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbaf4e2263cd1978fe16d0fb1b4b96c6dfb6065986bb8648c124fec5b56b810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777275"
---
# <a name="pixels"></a>píxeles

Los fragmentos se convierten en píxeles en el búfer de fotogramas. El búfer de fotogramas se organiza en un conjunto de búferes lógicos de color, profundidad, galería de símbolos y búferes de acumulación. El búfer de color consta de un búfer frontal izquierdo, frontal a la derecha, hacia atrás a la izquierda, hacia atrás a la derecha y algún número de búferes auxiliares. Puede emitir funciones para controlar estos búferes y leer o copiar píxeles directamente de ellos. (Tenga en cuenta que el contexto de OpenGL concreto que está usando puede no proporcionar todos estos búferes).

-   [Operaciones de framebuffer](framebuffer-operations.md)
-   [Lectura o copia de píxeles](reading-or-copying-pixels.md)
-   [Referencia de píxeles](pixels-reference.md)

 

 




