---
title: Transformaciones de matriz
description: Los vértices y normales se transforman mediante las matrices modelview y projection antes de que se utilicen para generar una imagen en el búfer de fotogramas.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Canalización de procesamiento openGL, matrices
- matrices OpenGL
- Matriz modelview
- Matriz de proyección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e3c88ffcfebc989400cfa9a85c16f355c0a7090ff4d16531cf03c3697ee869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937324"
---
# <a name="matrix-transformations"></a>Transformaciones de matriz

Los vértices y normales se transforman mediante las matrices modelview y projection antes de que se utilicen para generar una imagen en el búfer de fotogramas. Use funciones como [**glMatrixMode**](glmatrixmode.md), [ * *glMultMatrix \** _](glmultmatrix.md), [_*glRotate \**_](glrotate.md), [_*glTranslate \**_](gltranslate.md)y [_*glScale \**_](glscale.md) para crear las transformaciones deseadas. O bien, especifique matrices directamente [_*con glLoadMatrix \**_](glloadmatrix.md) y [_ *glLoadIdentity* *](glloadidentity.md). Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix para**](glpopmatrix.md) guardar y restaurar matrices de proyección y vista de modelos en sus respectivas pilas.

 

 




