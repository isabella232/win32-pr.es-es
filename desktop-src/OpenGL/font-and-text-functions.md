---
title: Funciones de fuente y texto (OpenGL)
description: Las siguientes funciones se pueden usar para administrar fuentes y texto.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funciones de WGL, texto
- Funciones de WGL, fuente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421817"
---
# <a name="font-and-text-functions-opengl"></a><span data-ttu-id="8a25a-105">Funciones de fuente y texto (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="8a25a-105">Font and Text Functions (OpenGL)</span></span>

<span data-ttu-id="8a25a-106">Las siguientes funciones se pueden usar para administrar fuentes y texto.</span><span class="sxs-lookup"><span data-stu-id="8a25a-106">The following functions can be used to manage fonts and text.</span></span>



| <span data-ttu-id="8a25a-107">Función de Windows</span><span class="sxs-lookup"><span data-stu-id="8a25a-107">Windows Function</span></span>                                 | <span data-ttu-id="8a25a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a25a-108">Description</span></span>                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a25a-109">**wglUseFontBitmaps**</span><span class="sxs-lookup"><span data-stu-id="8a25a-109">**wglUseFontBitmaps**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | <span data-ttu-id="8a25a-110">Crea un conjunto de listas de visualización de mapas de bits de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a25a-110">Creates a set of character bitmap display lists.</span></span> <span data-ttu-id="8a25a-111">Los caracteres proceden de la fuente actual del contexto del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8a25a-111">Characters come from a specified device context's current font.</span></span> <span data-ttu-id="8a25a-112">Los caracteres se especifican como una ejecución consecutiva en el conjunto de glifos de la fuente.</span><span class="sxs-lookup"><span data-stu-id="8a25a-112">Characters are specified as a consecutive run within the font's glyph set.</span></span>                                      |
| [<span data-ttu-id="8a25a-113">**wglUseFontOutlines**</span><span class="sxs-lookup"><span data-stu-id="8a25a-113">**wglUseFontOutlines**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | <span data-ttu-id="8a25a-114">Crea un conjunto de listas de presentación, en función de los glifos de la fuente de contorno seleccionada actualmente de un contexto de dispositivo, para su uso con el contexto de representación actual.</span><span class="sxs-lookup"><span data-stu-id="8a25a-114">Creates a set of display lists, based on the glyphs of the currently selected outline font of a device context, for use with the current rendering context.</span></span> <span data-ttu-id="8a25a-115">Las listas de visualización se utilizan para dibujar caracteres 3D de fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="8a25a-115">The display lists are used to draw 3-D characters of TrueType fonts.</span></span> |



 

<span data-ttu-id="8a25a-116">Las funciones **wglUseFontBitmaps** y **wglUseFontOutlines** toman un identificador de un contexto de dispositivo y usan la fuente actual del contexto del dispositivo como origen de los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="8a25a-116">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions take a handle to a device context, and use that device context's current font as a source for the bitmaps.</span></span> <span data-ttu-id="8a25a-117">Por lo tanto, es necesario establecer la fuente del contexto del dispositivo y las propiedades de la fuente antes de llamar a **wglUseFontBitmaps** o **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="8a25a-117">It is therefore necessary to set the device context's font and the font's properties before calling **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="8a25a-118">Las funciones [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) y [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) también toman un parámetro que convierte el primer glifo de la fuente en una lista de visualización de mapa de bits y un parámetro que especifica el número de glifos que se van a convertir en listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="8a25a-118">The [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions also take a parameter that turns the first glyph in the font into a bitmap display list, and a parameter that specifies how many glyphs to turn into display lists.</span></span> <span data-ttu-id="8a25a-119">A continuación, la función crea listas de visualización para la ejecución consecutiva de glifos especificada.</span><span class="sxs-lookup"><span data-stu-id="8a25a-119">The function then creates display lists for the specified consecutive run of glyphs.</span></span> <span data-ttu-id="8a25a-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8a25a-120">For example:</span></span>

-   <span data-ttu-id="8a25a-121">Para crear un conjunto de listas de visualización de mapas de bits de 224 para todos los glifos de juego de caracteres de Windows, establezca estos dos parámetros en 32 y 224, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8a25a-121">To create a set of 224 bitmap display lists for all of the Windows character set glyphs, set these two parameters to 32 and 224, respectively.</span></span>
-   <span data-ttu-id="8a25a-122">Para crear un conjunto de listas de visualización de mapas de bits de 256 para todos los glifos de juego de caracteres OEM, establezca estos dos parámetros en 0 y 256, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8a25a-122">To create a set of 256 bitmap display lists for all of the OEM character set glyphs, set these two parameters to 0 and 256, respectively.</span></span>
-   <span data-ttu-id="8a25a-123">Para crear una lista de visualización de un solo mapa de bits para un glifo de un solo juego de caracteres, establezca el segundo de estos parámetros en 1.</span><span class="sxs-lookup"><span data-stu-id="8a25a-123">To create a single bitmap display list for any single character set glyph, set the second of these parameters to 1.</span></span>

<span data-ttu-id="8a25a-124">Las funciones **wglUseFontBitmaps** y **wglUseFontOutlines** representan un glifo nulo en una fuente con una lista de visualización vacía.</span><span class="sxs-lookup"><span data-stu-id="8a25a-124">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions represent a null glyph in a font with an empty display list.</span></span>

<span data-ttu-id="8a25a-125">Las listas de visualización creadas mediante una llamada a **wglUseFontBitmaps** o **wglUseFontOutlines** se numeran automáticamente de forma consecutiva.</span><span class="sxs-lookup"><span data-stu-id="8a25a-125">The display lists created by a call to **wglUseFontBitmaps** or **wglUseFontOutlines** are automatically numbered consecutively.</span></span>

<span data-ttu-id="8a25a-126">Después de llamar a la función [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) o [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , llame a [**glCallLists**](glcalllists.md) para dibujar una cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a25a-126">After calling the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) or [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) function, call [**glCallLists**](glcalllists.md) to draw a string of characters.</span></span> <span data-ttu-id="8a25a-127">Vea [dibujar texto en una Double-Buffered ventana de OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) para ver el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8a25a-127">See [Drawing Text in a Double-Buffered OpenGL Window](drawing-text-in-a-double-buffered-opengl-window.md) for sample code.</span></span> <span data-ttu-id="8a25a-128">En este contexto, **glCallLists** usa cada carácter de una cadena como un índice en la matriz de listas de presentación numeradas de forma consecutiva creadas por **wglUseFontBitmaps** o **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="8a25a-128">In this context, **glCallLists** uses each character in a string as an index into the array of consecutively numbered display lists created by **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="8a25a-129">Cuando termine de dibujar texto, llame a la función [**glDeleteLists**](gldeletelists.md) para liberar el conjunto contiguo de listas de presentación creadas por **wglUseFontBitmaps** y **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="8a25a-129">When you finish drawing text, call the [**glDeleteLists**](gldeletelists.md) function to release the contiguous set of display lists created by **wglUseFontBitmaps** and **wglUseFontOutlines**.</span></span>

 

 




