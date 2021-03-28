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
# <a name="constructing-and-drawing-paths"></a><span data-ttu-id="94d02-105">Crear y dibujar trazados</span><span class="sxs-lookup"><span data-stu-id="94d02-105">Constructing and Drawing Paths</span></span>

<span data-ttu-id="94d02-106">Una ruta de acceso es una secuencia de primitivas de gráficos (líneas, rectángulos, curvas, texto y similares) que se pueden manipular y dibujar como una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="94d02-106">A path is a sequence of graphics primitives (lines, rectangles, curves, text, and the like) that can be manipulated and drawn as a single unit.</span></span> <span data-ttu-id="94d02-107">Una ruta de acceso se puede dividir en *figuras* que estén abiertas o cerradas.</span><span class="sxs-lookup"><span data-stu-id="94d02-107">A path can be divided into *figures* that are either open or closed.</span></span> <span data-ttu-id="94d02-108">Una figura puede contener varios tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="94d02-108">A figure can contain several primitives.</span></span>

<span data-ttu-id="94d02-109">Puede dibujar una ruta de acceso llamando al método [**Graphics::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , y puede rellenar una ruta de acceso llamando al método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) de la clase **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="94d02-109">You can draw a path by calling the [**Graphics::DrawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, and you can fill a path by calling the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method of the **Graphics** class.</span></span>

<span data-ttu-id="94d02-110">En los temas siguientes se tratan los trazados con más detalle:</span><span class="sxs-lookup"><span data-stu-id="94d02-110">The following topics cover paths in more detail:</span></span>

-   [<span data-ttu-id="94d02-111">Creación de figuras a partir de líneas, curvas y formas</span><span class="sxs-lookup"><span data-stu-id="94d02-111">Creating Figures from Lines, Curves, and Shapes</span></span>](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [<span data-ttu-id="94d02-112">Rellenar figuras abiertas</span><span class="sxs-lookup"><span data-stu-id="94d02-112">Filling Open Figures</span></span>](-gdiplus-filling-open-figures-use.md)

 

 



