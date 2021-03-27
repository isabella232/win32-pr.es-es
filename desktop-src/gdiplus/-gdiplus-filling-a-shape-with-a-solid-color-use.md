---
description: Para rellenar una forma con un color sólido, cree un objeto SolidBrush y, a continuación, pase la dirección de ese objeto SolidBrush como argumento a uno de los métodos Fill de la clase Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Rellenar una forma con un color sólido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997497"
---
# <a name="filling-a-shape-with-a-solid-color"></a><span data-ttu-id="0ecd2-103">Rellenar una forma con un color sólido</span><span class="sxs-lookup"><span data-stu-id="0ecd2-103">Filling a Shape with a Solid Color</span></span>

<span data-ttu-id="0ecd2-104">Para rellenar una forma con un color sólido, cree un objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) y, a continuación, pase la dirección de ese objeto **SolidBrush** como argumento a uno de los métodos Fill de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="0ecd2-104">To fill a shape with a solid color, create a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object, and then pass the address of that **SolidBrush** object as an argument to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="0ecd2-105">En el ejemplo siguiente se muestra cómo rellenar una elipse con el color rojo:</span><span class="sxs-lookup"><span data-stu-id="0ecd2-105">The following example shows how to fill an ellipse with the color red:</span></span>


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



<span data-ttu-id="0ecd2-106">En el ejemplo anterior, el constructor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) toma una referencia de objeto de [**color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) como su único argumento.</span><span class="sxs-lookup"><span data-stu-id="0ecd2-106">In the preceding example, the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor takes a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object reference as its only argument.</span></span> <span data-ttu-id="0ecd2-107">Los valores utilizados por el constructor de **color** representan los componentes alfa, rojo, verde y azul del color.</span><span class="sxs-lookup"><span data-stu-id="0ecd2-107">The values used by the **Color** constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="0ecd2-108">Cada uno de estos valores debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="0ecd2-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="0ecd2-109">El primer 255 indica que el color es totalmente opaco y el segundo 255 indica que el componente rojo tiene una intensidad máxima.</span><span class="sxs-lookup"><span data-stu-id="0ecd2-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="0ecd2-110">Los dos ceros indican que los componentes verde y azul tienen una intensidad de 0.</span><span class="sxs-lookup"><span data-stu-id="0ecd2-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>

<span data-ttu-id="0ecd2-111">Los cuatro números (0, 0, 100, 60) pasados al método [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) especifican la ubicación y el tamaño del rectángulo delimitador de la elipse.</span><span class="sxs-lookup"><span data-stu-id="0ecd2-111">The four numbers (0, 0, 100, 60) passed to the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="0ecd2-112">El rectángulo tiene una esquina superior izquierda de (0,0), un ancho de 100 y un alto de 60.</span><span class="sxs-lookup"><span data-stu-id="0ecd2-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>

 

 
