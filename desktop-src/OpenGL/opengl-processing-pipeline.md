---
title: Canalización de procesamiento de OpenGL
description: Canalización de procesamiento de OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, canalización de procesamiento
- canalización de procesamiento OpenGL
- pipeline OpenGL
- framebuffers,canalización de procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b52568de344404e9bddbedbacc40beda064b09d3e3af96c2657f670e677c32a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936874"
---
# <a name="opengl-processing-pipeline"></a>Canalización de procesamiento de OpenGL

Muchas funciones OpenGL se usan específicamente para dibujar objetos como puntos, líneas, polígonos y mapas de bits. Algunas funciones controlan la forma en que se produce parte de este dibujo (por ejemplo, aquellas que permiten suavizar contornos o texturizar). Otras funciones se refieren específicamente a la manipulación del búfer de fotogramas. En los temas de esta sección se describe cómo funcionan todas las funciones de OpenGL conjuntamente para crear la canalización de procesamiento de OpenGL. En esta sección también se observan más de cerca las fases en las que se procesan realmente los datos y se vinculan estas fases a las funciones openGL.

En el diagrama siguiente se detalla la canalización de procesamiento de OpenGL. Para la mayor parte de la canalización, puede ver tres flechas verticales entre las fases principales. Estas flechas representan vértices y los dos tipos principales de datos que se pueden asociar a los vértices: valores de color y coordenadas de textura. Tenga en cuenta también que los vértices se ensamblan en primitivos, luego en fragmentos y, por último, en píxeles en el búfer de fotogramas. Esta progresión se describe con más detalle en [Vértices, Primitivos,](primitives.md) [Fragmentos](fragments.md)y [Píxeles.](pixels.md) [](vertices.md)

![Diagrama que muestra la canalización de procesamiento de OpenGL.](images/proc01.png)

 

 




