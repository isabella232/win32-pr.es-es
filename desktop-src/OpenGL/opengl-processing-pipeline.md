---
title: Canalización de procesamiento de OpenGL
description: Canalización de procesamiento de OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, canalización de procesamiento
- procesamiento de la canalización OpenGL
- OpenGL de canalización
- framebuffers, canalización de procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552886"
---
# <a name="opengl-processing-pipeline"></a>Canalización de procesamiento de OpenGL

Muchas funciones de OpenGL se utilizan específicamente para dibujar objetos como puntos, líneas, polígonos y mapas de bits. Algunas funciones controlan la forma en que se produce parte de este dibujo (como los que habilitan el suavizado de contorno o la texturización). Otras funciones están especialmente preocupadas por la manipulación de fotogramas. En los temas de esta sección se describe el funcionamiento conjunto de todas las funciones de OpenGL para crear la canalización de procesamiento de OpenGL. En esta sección también se examinan con más detalle las fases en las que se procesan los datos y se vinculan estas fases a las funciones de OpenGL.

En el siguiente diagrama se detalla la canalización de procesamiento de OpenGL. Para la mayor parte de la canalización, puede ver tres flechas verticales entre las fases principales. Estas flechas representan los vértices y los dos tipos principales de datos que se pueden asociar a los vértices: valores de color y coordenadas de textura. Tenga en cuenta también que los vértices se ensamblan en primitivos, luego en fragmentos y, por último, en píxeles en el fotogramas. Esta progresión se describe con más detalle en [vértices](vertices.md), [primitivas](primitives.md), [fragmentos](fragments.md)y [píxeles](pixels.md).

![Diagrama que muestra la canalización de procesamiento de OpenGL.](images/proc01.png)

 

 




