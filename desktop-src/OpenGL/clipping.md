---
title: Recorte (OpenGL)
description: El recorte se produce en dos pasos
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Canalización de procesamiento de OpenGL, recorte
- recorte de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421820"
---
# <a name="clipping-opengl"></a>Recorte (OpenGL)

El recorte se produce en dos pasos:

1.  **Ver el recorte específico del clippingApplication de volumen.** Inmediatamente después de ensamblar los primitivos, se recortan en coordenadas oculares según sea necesario para los planos de recorte que haya definido con [**glClipPlane**](glclipplane.md). (OpenGL requiere compatibilidad con al menos seis planos de recorte específicos de la aplicación).
2.  Las primitivas se transforman mediante la matriz de proyección en coordenadas de recorte y se recortan por el volumen de vista correspondiente. Esta matriz se puede controlar mediante las funciones de transformación de matriz (vea [transformaciones de matriz](matrix-transformations.md)) pero normalmente se especifica mediante [**glFrustum**](glfrustum.md) o [**glOrtho**](glortho.md).

Los puntos, segmentos de línea y polígonos se controlan de forma diferente durante el recorte:

-   Los puntos se retienen en su estado original (si están dentro del volumen de clip) o se descartan (si están fuera del volumen de clip).
-   Si partes de segmentos de línea o polígonos están fuera del volumen de clip, se generan nuevos vértices en los puntos de recorte.
-   En el caso de los polígonos, es posible que sea necesario construir un borde completo entre los nuevos vértices generados en los puntos de recorte.
-   En el caso de segmentos de línea y polígonos que se recortan, la información de marca de borde, color y textura se asigna a todos los nuevos vértices.

 

 




