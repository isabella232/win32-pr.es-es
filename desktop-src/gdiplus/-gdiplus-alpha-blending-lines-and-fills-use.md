---
description: En Windows GDI+, un color es un valor de 32 bits con 8 bits para alfa, rojo, verde y azul.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Líneas y rellenos con mezcla alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908902"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="0719c-103">Líneas y rellenos con mezcla alfa</span><span class="sxs-lookup"><span data-stu-id="0719c-103">Alpha Blending Lines and Fills</span></span>

<span data-ttu-id="0719c-104">En Windows GDI+, un color es un valor de 32 bits con 8 bits para alfa, rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="0719c-104">In Windows GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="0719c-105">El valor alfa indica la transparencia del color, la medida en la que el color se mezcla con el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="0719c-105">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="0719c-106">Los valores alfa oscilan entre 0 y 255, donde 0 representa un color completamente transparente y 255 representa un color totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="0719c-106">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>

<span data-ttu-id="0719c-107">La combinación alfa es una combinación píxel a píxel de datos de color de origen y de fondo.</span><span class="sxs-lookup"><span data-stu-id="0719c-107">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="0719c-108">Cada uno de los tres componentes (rojo, verde y azul) de un color de origen determinado se combina con el componente correspondiente del color de fondo según la fórmula siguiente:</span><span class="sxs-lookup"><span data-stu-id="0719c-108">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>

<span data-ttu-id="0719c-109">displayColor = sourceColor × Alpha/255 + backgroundColor × (255 – Alpha)/255</span><span class="sxs-lookup"><span data-stu-id="0719c-109">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>

<span data-ttu-id="0719c-110">Por ejemplo, supongamos que el componente rojo del color de origen es 150 y el componente rojo del color de fondo es 100.</span><span class="sxs-lookup"><span data-stu-id="0719c-110">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="0719c-111">Si el valor alfa es 200, el componente rojo del color resultante se calcula de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="0719c-111">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>

<span data-ttu-id="0719c-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="0719c-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>

<span data-ttu-id="0719c-113">En los temas siguientes se trata la combinación alfa con más detalle:</span><span class="sxs-lookup"><span data-stu-id="0719c-113">The following topics cover alpha blending in more detail:</span></span>

-   [<span data-ttu-id="0719c-114">Dibujo de líneas opacas y semitransparentes</span><span class="sxs-lookup"><span data-stu-id="0719c-114">Drawing Opaque and Semitransparent Lines</span></span>](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [<span data-ttu-id="0719c-115">Dibujar con pinceles opacos y semitransparentes</span><span class="sxs-lookup"><span data-stu-id="0719c-115">Drawing with Opaque and Semitransparent Brushes</span></span>](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [<span data-ttu-id="0719c-116">Usar el modo de composición para controlar la mezcla alfa</span><span class="sxs-lookup"><span data-stu-id="0719c-116">Using Compositing Mode to Control Alpha Blending</span></span>](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [<span data-ttu-id="0719c-117">Uso una matriz de colores para establecer valores alfa en imágenes</span><span class="sxs-lookup"><span data-stu-id="0719c-117">Using a Color Matrix to Set Alpha Values in Images</span></span>](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [<span data-ttu-id="0719c-118">Establecer los valores alfa de píxeles individuales</span><span class="sxs-lookup"><span data-stu-id="0719c-118">Setting the Alpha Values of Individual Pixels</span></span>](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



