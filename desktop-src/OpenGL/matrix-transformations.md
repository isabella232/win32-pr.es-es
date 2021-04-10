---
title: Transformaciones de matriz
description: Los vértices y las normales se transforman mediante las matrices de proyección y MODELVIEW antes de que se usen para producir una imagen en el fotogramas.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Canalización de procesamiento de OpenGL, matrices
- matrices OpenGL
- matriz MODELVIEW
- matriz de proyección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268675"
---
# <a name="matrix-transformations"></a>Transformaciones de matriz

Los vértices y las normales se transforman mediante las matrices de proyección y MODELVIEW antes de que se usen para producir una imagen en el fotogramas. Use funciones como [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix \***](glmultmatrix.md), [**glRotate \***](glrotate.md), [**glTranslate \***](gltranslate.md)y [**glScale \***](glscale.md) para crear las transformaciones deseadas. O bien, especifique las matrices directamente con [**glLoadMatrix \***](glloadmatrix.md) y [**glLoadIdentity**](glloadidentity.md). Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar las matrices de MODELVIEW y proyección en sus respectivas pilas.

 

 




