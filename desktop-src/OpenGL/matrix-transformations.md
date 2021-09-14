---
title: Transformaciones de matriz
description: Los vértices y las normales se transforman mediante las matrices modelview y projection antes de que se utilicen para generar una imagen en el búfer de fotogramas.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Canalización de procesamiento de OpenGL, matrices
- matrices OpenGL
- Matriz modelview
- Matriz de proyección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265695"
---
# <a name="matrix-transformations"></a>Transformaciones de matriz

Los vértices y las normales se transforman mediante las matrices modelview y projection antes de que se utilicen para generar una imagen en el búfer de fotogramas. Use funciones como [**glMatrixMode**](glmatrixmode.md), [ * *glMultMatrix \** _](glmultmatrix.md), [_*glRotate \**_](glrotate.md), [_*glTranslate \**_](gltranslate.md)y [_*glScale \**_](glscale.md) para componer las transformaciones deseadas. O bien, especifique matrices directamente [_*con glLoadMatrix \**_](glloadmatrix.md) y _ [*glLoadIdentity.* *](glloadidentity.md) Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix para**](glpopmatrix.md) guardar y restaurar matrices de modelview y proyección en sus respectivas pilas.

 

 




