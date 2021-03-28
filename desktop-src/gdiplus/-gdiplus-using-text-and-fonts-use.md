---
description: Windows GDI+ proporciona varias clases que forman la base del dibujo de texto.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Usar texto y fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541435"
---
# <a name="using-text-and-fonts"></a><span data-ttu-id="7cae3-103">Usar texto y fuentes</span><span class="sxs-lookup"><span data-stu-id="7cae3-103">Using Text and Fonts</span></span>

<span data-ttu-id="7cae3-104">Windows GDI+ proporciona varias clases que forman la base del dibujo de texto.</span><span class="sxs-lookup"><span data-stu-id="7cae3-104">Windows GDI+ provides several classes that form the foundation for drawing text.</span></span> <span data-ttu-id="7cae3-105">La clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tiene varios métodos [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) que le permiten especificar diversas características de texto, como la ubicación, el rectángulo delimitador, la fuente y el formato.</span><span class="sxs-lookup"><span data-stu-id="7cae3-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has several [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="7cae3-106">Otras clases que contribuyen a la representación de texto incluyen [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)y [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span><span class="sxs-lookup"><span data-stu-id="7cae3-106">Other classes that contribute to text rendering include [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection), and [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span></span>

<span data-ttu-id="7cae3-107">En los temas siguientes se tratan el texto y las fuentes con más detalle:</span><span class="sxs-lookup"><span data-stu-id="7cae3-107">The following topics cover text and fonts in more detail:</span></span>

-   [<span data-ttu-id="7cae3-108">Construir fuentes y familias de fuentes</span><span class="sxs-lookup"><span data-stu-id="7cae3-108">Constructing Font Families and Fonts</span></span>](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [<span data-ttu-id="7cae3-109">Dibujar texto</span><span class="sxs-lookup"><span data-stu-id="7cae3-109">Drawing Text</span></span>](-gdiplus-drawing-text-use.md)
-   [<span data-ttu-id="7cae3-110">Aplicar formato a texto</span><span class="sxs-lookup"><span data-stu-id="7cae3-110">Formatting Text</span></span>](-gdiplus-formatting-text-use.md)
-   [<span data-ttu-id="7cae3-111">Enumeración de fuentes instaladas</span><span class="sxs-lookup"><span data-stu-id="7cae3-111">Enumerating Installed Fonts</span></span>](-gdiplus-enumerating-installed-fonts-use.md)
-   [<span data-ttu-id="7cae3-112">Creación de una colección de fuentes privadas</span><span class="sxs-lookup"><span data-stu-id="7cae3-112">Creating a Private Font Collection</span></span>](-gdiplus-creating-a-private-font-collection-use.md)
-   [<span data-ttu-id="7cae3-113">Obtener métricas de fuente</span><span class="sxs-lookup"><span data-stu-id="7cae3-113">Obtaining Font Metrics</span></span>](-gdiplus-obtaining-font-metrics-use.md)
-   [<span data-ttu-id="7cae3-114">Suavizado de contorno con texto</span><span class="sxs-lookup"><span data-stu-id="7cae3-114">Antialiasing with Text</span></span>](-gdiplus-antialiasing-with-text-use.md)

 

 



