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
ms.openlocfilehash: eb6660452930683943da780fad3aeb001e531711
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069305"
---
# <a name="pixels"></a>píxeles

Los fragmentos se convierten en píxeles en el búfer de fotogramas. El búfer de fotogramas se organiza en un conjunto de búferes lógicos de color, profundidad, galería de símbolos y búferes de acumulación. El propio búfer de color consta de un búfer frontal a la izquierda, al lado derecho, a la izquierda hacia atrás, hacia atrás a la derecha y un número de búferes auxiliares. Puede emitir funciones para controlar estos búferes y leer o copiar píxeles directamente de ellos. (Tenga en cuenta que el contexto de OpenGL concreto que está usando puede no proporcionar todos estos búferes).

-   [Operaciones de Framebuffer](framebuffer-operations.md)
-   [Lectura o copia de píxeles](reading-or-copying-pixels.md)
-   [Referencia de píxeles](pixels-reference.md)

 

 




