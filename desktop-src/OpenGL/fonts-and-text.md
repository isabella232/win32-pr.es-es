---
title: Fuentes y texto (OpenGL)
description: La implementación de OpenGL en Windows de Microsoft admite gráficos GDI en una ventana de OpenGL de un solo búfer.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL en Windows, fuentes
- OpenGL en Windows, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421816"
---
# <a name="fonts-and-text-opengl"></a><span data-ttu-id="9da63-105">Fuentes y texto (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="9da63-105">Fonts and Text (OpenGL)</span></span>

<span data-ttu-id="9da63-106">La implementación de OpenGL en Windows de Microsoft admite gráficos GDI en una ventana de OpenGL de un solo búfer.</span><span class="sxs-lookup"><span data-stu-id="9da63-106">Microsoft's implementation of OpenGL in Windows supports GDI graphics in a single-buffered OpenGL window.</span></span> <span data-ttu-id="9da63-107">No admite gráficos de GDI en una ventana de OpenGL de doble búfer.</span><span class="sxs-lookup"><span data-stu-id="9da63-107">It does not support GDI graphics in a double-buffered OpenGL window.</span></span> <span data-ttu-id="9da63-108">Por lo tanto, solo puede llamar a las funciones de texto y fuente de GDI estándar para dibujar texto en una ventana de OpenGL de un solo búfer. no se puede llamar a esas funciones para dibujar texto en una ventana de OpenGL de doble búfer.</span><span class="sxs-lookup"><span data-stu-id="9da63-108">Thus, you can call only the standard GDI font and text functions to draw text in a single-buffered OpenGL window; you cannot call those functions to draw text in a double-buffered OpenGL window.</span></span>

<span data-ttu-id="9da63-109">Existe una solución alternativa para esta restricción en el texto de las ventanas de doble búfer: Cree listas de visualización de OpenGL para imágenes de mapa de bits de caracteres y, a continuación, ejecute esas listas de visualización para dibujar caracteres.</span><span class="sxs-lookup"><span data-stu-id="9da63-109">There is a workaround for this restriction on text in double-buffered windows: build OpenGL display lists for bitmap images of characters, and then execute those display lists to draw characters.</span></span> <span data-ttu-id="9da63-110">Existen tres pasos principales en este proceso:</span><span class="sxs-lookup"><span data-stu-id="9da63-110">There are three main steps in this process:</span></span>

1.  <span data-ttu-id="9da63-111">Seleccione una fuente para un contexto de dispositivo y establezca las propiedades de la fuente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9da63-111">Select a font for a device context, setting the font's properties as desired.</span></span>
2.  <span data-ttu-id="9da63-112">Cree un conjunto de listas de presentación de mapas de bits en función de los glifos de la fuente del contexto del dispositivo, una lista de visualización para cada glifo que la aplicación va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="9da63-112">Create a set of bitmap display lists based on the glyphs in the device context's font, one display list for each glyph that the application will draw.</span></span>
3.  <span data-ttu-id="9da63-113">Dibuje cada glifo en una cadena mediante las listas de visualización del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="9da63-113">Draw each glyph in a string, using those bitmap display lists.</span></span>

<span data-ttu-id="9da63-114">Para crear las listas de visualización, llame a las funciones [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) y [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) .</span><span class="sxs-lookup"><span data-stu-id="9da63-114">To create the display lists, call the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions.</span></span> <span data-ttu-id="9da63-115">Para dibujar caracteres en una cadena mediante esas listas de visualización, llame a [**glCallLists**](glcalllists.md).</span><span class="sxs-lookup"><span data-stu-id="9da63-115">To draw characters in a string using those display lists, call [**glCallLists**](glcalllists.md).</span></span>

<span data-ttu-id="9da63-116">Para crear aplicaciones que sean fáciles de localizar y que utilicen los recursos de manera moderada, la creación y el almacenamiento de estas listas de visualización de imágenes de glifo deben administrarse con cuidado.</span><span class="sxs-lookup"><span data-stu-id="9da63-116">To create applications that are easy to localize and that use resources sparingly, the creation and storage of these glyph image display lists must be managed carefully.</span></span> <span data-ttu-id="9da63-117">Muchos idiomas, a diferencia del inglés, tienen alfabetos cuyos códigos de carácter van a través de un conjunto de valores relativamente grande.</span><span class="sxs-lookup"><span data-stu-id="9da63-117">Many languages, unlike English, have alphabets whose character codes range over a relatively large set of values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9da63-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9da63-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da63-119">Funciones de fuente y texto</span><span class="sxs-lookup"><span data-stu-id="9da63-119">Font and Text Functions</span></span>](font-and-text-functions.md)
</dt> </dl>

 

 




