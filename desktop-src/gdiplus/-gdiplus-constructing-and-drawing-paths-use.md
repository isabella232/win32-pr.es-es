---
description: Una ruta de acceso es una secuencia de primitivas de gráficos (líneas, rectángulos, curvas, texto y similares) que se pueden manipular y dibujar como una sola unidad. Una ruta de acceso se puede dividir en figuras que estén abiertas o cerradas. Una figura puede contener varios tipos primitivos.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Crear y dibujar trazados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997520"
---
# <a name="constructing-and-drawing-paths"></a>Crear y dibujar trazados

Una ruta de acceso es una secuencia de primitivas de gráficos (líneas, rectángulos, curvas, texto y similares) que se pueden manipular y dibujar como una sola unidad. Una ruta de acceso se puede dividir en *figuras* que estén abiertas o cerradas. Una figura puede contener varios tipos primitivos.

Puede dibujar una ruta de acceso llamando al método [**Graphics::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , y puede rellenar una ruta de acceso llamando al método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) de la clase **Graphics** .

En los temas siguientes se tratan los trazados con más detalle:

-   [Creación de figuras a partir de líneas, curvas y formas](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [Rellenar figuras abiertas](-gdiplus-filling-open-figures-use.md)

 

 



