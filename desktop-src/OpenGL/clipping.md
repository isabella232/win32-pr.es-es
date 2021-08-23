---
title: Recorte (OpenGL)
description: El recorte se produce en dos pasos
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Canalización de procesamiento de OpenGL, recorte
- recorte de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb518b9208b73dad2071531f6a30cdff6cab2ec5dcbe937fa3e66fea8bb0a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289045"
---
# <a name="clipping-opengl"></a>Recorte (OpenGL)

El recorte se produce en dos pasos:

1.  **Visualización del recorte de volumen Recorte específico de la aplicación.** Inmediatamente después de ensamblar las primitivas, se recortan en coordenadas de los ojos según sea necesario para los planos de recorte que haya definido con [**glClipPlane**](glclipplane.md). (OpenGL requiere compatibilidad con al menos seis de estos planos de recorte específicos de la aplicación).
2.  Las primitivas se transforman mediante la matriz de proyección en coordenadas de recorte y se recortan mediante el volumen de vista correspondiente. Esta matriz se puede controlar mediante las funciones de transformación de matriz (vea Transformaciones [de](matrix-transformations.md)matriz), pero normalmente se especifica [**mediante glFrustum**](glfrustum.md) o [**glOrtho**](glortho.md).

Los puntos, segmentos de línea y polígonos se controlan de forma diferente durante el recorte:

-   Los puntos se conservan en su estado original (si están dentro del volumen de recorte) o se descartan (si están fuera del volumen de recorte).
-   Si partes de segmentos de línea o polígonos están fuera del volumen de recorte, se generan nuevos vértices en los puntos de recorte.
-   En el caso de los polígonos, es posible que sea necesario construir un borde completo entre los nuevos vértices generados en los puntos de recorte.
-   Para los segmentos de línea y los polígonos recortados, la información de marca de borde, color y textura se asigna a todos los nuevos vértices.

 

 




