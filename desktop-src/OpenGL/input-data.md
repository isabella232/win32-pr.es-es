---
title: Datos de entrada
description: La canalización de OpenGL requiere que se introduzcan varios tipos de datos.
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Canalización de procesamiento de OpenGL, datos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a588e60991ad068653890659e236f8a7a96e62cad524b13ea72bfd38fb5bba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937432"
---
# <a name="input-data"></a>Datos de entrada

La canalización de OpenGL requiere que se introduzcan varios tipos de datos:

-   **Vértices**. Los vértices describen la forma del objeto geométrico deseado. Para especificar vértices, use las funciones [ * *glVertex \** _](glvertex-functions.md) junto con _ [*glBegin* *](glbegin.md) y [**glEnd**](glend.md) para crear un punto, una línea o un polígono. También puede usar [**glRect para**](glrect-functions.md) describir un rectángulo completo a la vez.
-   **Marca de borde**. De forma predeterminada, todos los bordes de los polígonos son bordes de límite. Use [**glEdgeFlag \* para**](gledgeflag-functions.md) establecer explícitamente la marca perimetral.
-   **Posición de trama actual.** Se especifica con [**glRasterPos \***](glrasterpos-functions.md), la posición de trama actual se usa para determinar las coordenadas de trama para las operaciones de dibujo de píxeles y mapas de bits.
-   **Normal actual.** Un vector normal asociado a un vértice determinado determina cómo se orienta una superficie de ese vértice en un espacio tridimensional; esto a su vez afecta a la cantidad de luz que recibe ese vértice determinado. Use [**glNormal \* para**](glnormal-functions.md) especificar un vector normal.
-   **Color actual.** El color de un vértice, junto con las condiciones de iluminación, determinan el color final encendido. El color se especifica con [ * *glColor \** _](glcolor-functions.md) si está en modo RGBA o con _ [*glIndex \** *](glindex-functions.md) si está en modo de índice de color.
-   **Coordenadas de textura actuales.** Especificadas con [**glTexCoord, \***](gltexcoord-functions.md)las coordenadas de textura determinan la ubicación en un mapa de textura que se asociará a un vértice de un objeto.

> [!Note]  
> Cuando se llama a glVertex _ , el vértice resultante hereda las coordenadas actuales de marca **\* *de borde, normal, color y textura. Por lo tanto, _* glEdgeFlag \* *_, _* glNormal \* *_, _* glColor \* *_, y _* glTexCoord _ deben llamarse antes de \* *_* glVertex \***, si van a afectar al vértice resultante.

 

 

 




