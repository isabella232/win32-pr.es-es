---
description: 'Un patrón de trama se realiza a partir de dos colores: uno para el fondo y otro para las líneas que forman el patrón en el fondo.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Relleno de una forma con un patrón de trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988130"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a><span data-ttu-id="c4a91-103">Relleno de una forma con un patrón de trama</span><span class="sxs-lookup"><span data-stu-id="c4a91-103">Filling a Shape with a Hatch Pattern</span></span>

<span data-ttu-id="c4a91-104">Un patrón de trama se realiza a partir de dos colores: uno para el fondo y otro para las líneas que forman el patrón en el fondo.</span><span class="sxs-lookup"><span data-stu-id="c4a91-104">A hatch pattern is made from two colors: one for the background and one for the lines that form the pattern over the background.</span></span> <span data-ttu-id="c4a91-105">Para rellenar una forma cerrada con un patrón de trama, use un objeto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) .</span><span class="sxs-lookup"><span data-stu-id="c4a91-105">To fill a closed shape with a hatch pattern, use a [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) object.</span></span> <span data-ttu-id="c4a91-106">En el ejemplo siguiente se muestra cómo rellenar una elipse con un patrón de trama:</span><span class="sxs-lookup"><span data-stu-id="c4a91-106">The following example demonstrates how to fill an ellipse with a hatch pattern:</span></span>


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



<span data-ttu-id="c4a91-107">En la ilustración siguiente se muestra la elipse rellenada.</span><span class="sxs-lookup"><span data-stu-id="c4a91-107">The following illustration shows the filled ellipse.</span></span>

![Ilustración de una elipse rellena con el patrón de trama de las líneas horizontales sobre un fondo sólido](images/hatch1.png)

<span data-ttu-id="c4a91-109">El constructor [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) toma tres argumentos: el estilo de trama, el color de la línea de sombreado y el color del fondo.</span><span class="sxs-lookup"><span data-stu-id="c4a91-109">The [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) constructor takes three arguments: the hatch style, the color of the hatch line, and the color of the background.</span></span> <span data-ttu-id="c4a91-110">El argumento de estilo de trama puede ser cualquier elemento de la enumeración [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) .</span><span class="sxs-lookup"><span data-stu-id="c4a91-110">The hatch style argument can be any element of the [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) enumeration.</span></span> <span data-ttu-id="c4a91-111">Hay más de 50 elementos en la enumeración **HatchStyle** ; algunos de esos elementos se muestran en la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4a91-111">There are more than fifty elements in the **HatchStyle** enumeration; a few of those elements are shown in the following list:</span></span>

-   <span data-ttu-id="c4a91-112">**HatchStyleHorizontal**</span><span class="sxs-lookup"><span data-stu-id="c4a91-112">**HatchStyleHorizontal**</span></span>
-   <span data-ttu-id="c4a91-113">**HatchStyleVertical**</span><span class="sxs-lookup"><span data-stu-id="c4a91-113">**HatchStyleVertical**</span></span>
-   <span data-ttu-id="c4a91-114">**HatchStyleForwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="c4a91-114">**HatchStyleForwardDiagonal**</span></span>
-   <span data-ttu-id="c4a91-115">**HatchStyleBackwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="c4a91-115">**HatchStyleBackwardDiagonal**</span></span>
-   <span data-ttu-id="c4a91-116">**HatchStyleCross**</span><span class="sxs-lookup"><span data-stu-id="c4a91-116">**HatchStyleCross**</span></span>
-   <span data-ttu-id="c4a91-117">**HatchStyleDiagonalCross**</span><span class="sxs-lookup"><span data-stu-id="c4a91-117">**HatchStyleDiagonalCross**</span></span>

 

 



