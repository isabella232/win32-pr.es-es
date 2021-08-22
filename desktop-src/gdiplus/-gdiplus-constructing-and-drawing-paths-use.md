---
description: Un trazado es una secuencia de primitivas de gráficos (líneas, rectángulos, curvas, texto y otros) que se pueden manipular y dibujar como una sola unidad. Una ruta de acceso se puede dividir en figuras abiertas o cerradas. Una ilustración puede contener varios primitivos.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Crear y dibujar trazados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83608dfacbd75bcbe916c9b5528f4bed7be4ed65713927a65f3823670c93311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612505"
---
# <a name="constructing-and-drawing-paths"></a>Crear y dibujar trazados

Un trazado es una secuencia de primitivas de gráficos (líneas, rectángulos, curvas, texto y otros) que se pueden manipular y dibujar como una sola unidad. Una ruta de acceso se puede dividir en *figuras* abiertas o cerradas. Una ilustración puede contener varios primitivos.

Puede dibujar una ruta de acceso llamando al método [**Graphics::D rawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y puede rellenar una ruta llamando al método [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) de la clase **Graphics.**

Los temas siguientes tratan las rutas de acceso con más detalle:

-   [Creación de figuras a partir de líneas, curvas y formas](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [Rellenar cifras abiertas](-gdiplus-filling-open-figures-use.md)

 

 



