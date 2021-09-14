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
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244874"
---
# <a name="opengl-processing-pipeline"></a>Canalización de procesamiento de OpenGL

Muchas funciones OpenGL se usan específicamente para dibujar objetos como puntos, líneas, polígonos y mapas de bits. Algunas funciones controlan la forma en que se produce parte de este dibujo (por ejemplo, aquellas que permiten suavizar contornos o texturizar). Otras funciones se refieren específicamente a la manipulación del búfer de fotogramas. En los temas de esta sección se describe cómo funcionan todas las funciones de OpenGL conjuntamente para crear la canalización de procesamiento de OpenGL. En esta sección también se observan más de cerca las fases en las que se procesan realmente los datos y se vinculan estas fases a las funciones openGL.

En el diagrama siguiente se detalla la canalización de procesamiento de OpenGL. Para la mayor parte de la canalización, puede ver tres flechas verticales entre las fases principales. Estas flechas representan vértices y los dos tipos principales de datos que se pueden asociar a los vértices: valores de color y coordenadas de textura. Tenga en cuenta también que los vértices se ensamblan en primitivos, luego en fragmentos y, por último, en píxeles en el búfer de fotogramas. Esta progresión se describe con más detalle en [Vértices, Primitivos,](primitives.md) [Fragmentos](fragments.md)y [Píxeles.](pixels.md) [](vertices.md)

![Diagrama que muestra la canalización de procesamiento de OpenGL.](images/proc01.png)

 

 




