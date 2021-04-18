---
title: Datos de entrada
description: La canalización de OpenGL requiere que escriba varios tipos de datos
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Canalización de procesamiento de OpenGL, datos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665629"
---
# <a name="input-data"></a>Datos de entrada

La canalización de OpenGL requiere que escriba varios tipos de datos:

-   **Vértices**. Los vértices describen la forma del objeto geométrico deseado. Para especificar vértices, use las funciones [**\* glVertex**](glvertex-functions.md) junto con [**glBegin**](glbegin.md) y [**glEnd**](glend.md) para crear un punto, línea o polígono. También puede usar [**glRect**](glrect-functions.md) para describir un rectángulo completo al mismo tiempo.
-   **Marca perimetral**. De forma predeterminada, todos los bordes de polígonos son bordes del límite. Use [**glEdgeFlag \***](gledgeflag-functions.md) para establecer explícitamente la marca perimetral.
-   **Posición de la trama actual**. Especificado con [**glRasterPos \***](glrasterpos-functions.md), la posición de la trama actual se usa para determinar las coordenadas de trama para las operaciones de dibujo de píxeles y de mapas de bits.
-   **Normal actual**. Un vector normal asociado a un vértice determinado determina cómo se orienta una superficie en ese vértice en un espacio tridimensional; Esto, a su vez, afecta a la cantidad de luz que recibe el vértice en particular. Use [**glNormal \***](glnormal-functions.md) para especificar un vector normal.
-   **Color actual**. El color de un vértice, junto con las condiciones de iluminación, determinan el color final iluminado. El color se especifica [**con \* glColor**](glcolor-functions.md) si está en modo RGBA, o con [**glIndex \***](glindex-functions.md) si está en modo de índice de color.
-   **Coordenadas de textura actuales**. Especificado con [**glTexCoord \***](gltexcoord-functions.md), las coordenadas de textura determinan la ubicación en un mapa de textura que se va a asociar a un vértice de un objeto.

> [!Note]  
> Cuando se llama a **glVertex \*** , el vértice resultante hereda la marca de borde actual, las coordenadas normal, de color y de textura. Por lo tanto, se debe llamar a **glEdgeFlag \***, **glNormal \***, **glColor \*** y **glTexCoord \*** antes de **glVertex \***, en caso de que afecte al vértice resultante.

 

 

 




