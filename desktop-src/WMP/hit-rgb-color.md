---
title: Golpear color RGB
description: Golpear color RGB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Máscaras móviles de Windows Media Player, colores de botón
- máscaras, colores de botón
- referencia de las máscaras, botones
- botones en máscaras, colores
- referencia de color para máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695422"
---
# <a name="hit-rgb-color"></a><span data-ttu-id="54bb8-108">Golpear color RGB</span><span class="sxs-lookup"><span data-stu-id="54bb8-108">Hit RGB Color</span></span>

<span data-ttu-id="54bb8-109">Si utiliza los botones de región (PushHit, ToggleHit y 2PushHit), debe definir el color que usará Windows Media Player para determinar el área de aciertos del botón.</span><span class="sxs-lookup"><span data-stu-id="54bb8-109">If you are using region buttons (PushHit, ToggleHit, and 2PushHit), you must define the color that Windows Media Player will use to determine the hit area of your button.</span></span> <span data-ttu-id="54bb8-110">Este valor debe especificarse mediante tres enteros positivos separados por comas.</span><span class="sxs-lookup"><span data-stu-id="54bb8-110">This value must be specified using three positive integers separated by commas.</span></span> <span data-ttu-id="54bb8-111">Estos enteros representan la cantidad de rojo, verde y azul para un color de mapa de bits y oscilan entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="54bb8-111">These integers represent the amount of red, green, and blue for a bitmap color, and range from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="54bb8-112">Los tipos de botones están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="54bb8-112">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="54bb8-113">Puede usar los colores de los valores, pero asegúrese de que cada botón de la región que defina tenga un color único en el archivo de imagen de región y que el valor de color que defina aquí como un número coincida con el color real utilizado en la imagen de la región.</span><span class="sxs-lookup"><span data-stu-id="54bb8-113">You can use any colors for the values, but be sure that each region button you define has a unique color in the Region image file and that the color value you define here as a number matches the actual color used in the Region image.</span></span>

<span data-ttu-id="54bb8-114">En la tabla siguiente se muestran algunos colores típicos que podría querer usar.</span><span class="sxs-lookup"><span data-stu-id="54bb8-114">The following table shows some typical colors you might want to use.</span></span>



| <span data-ttu-id="54bb8-115">Value</span><span class="sxs-lookup"><span data-stu-id="54bb8-115">Value</span></span>       | <span data-ttu-id="54bb8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="54bb8-116">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="54bb8-117">0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="54bb8-117">0,0,0</span></span>       | <span data-ttu-id="54bb8-118">Negro</span><span class="sxs-lookup"><span data-stu-id="54bb8-118">Black</span></span>       |
| <span data-ttu-id="54bb8-119">255.255.255</span><span class="sxs-lookup"><span data-stu-id="54bb8-119">255,255,255</span></span> | <span data-ttu-id="54bb8-120">Blanco</span><span class="sxs-lookup"><span data-stu-id="54bb8-120">White</span></span>       |
| <span data-ttu-id="54bb8-121">255, 0, 0</span><span class="sxs-lookup"><span data-stu-id="54bb8-121">255,0,0</span></span>     | <span data-ttu-id="54bb8-122">Rojo</span><span class="sxs-lookup"><span data-stu-id="54bb8-122">Red</span></span>         |
| <span data-ttu-id="54bb8-123">0255, 0</span><span class="sxs-lookup"><span data-stu-id="54bb8-123">0,255,0</span></span>     | <span data-ttu-id="54bb8-124">Verde</span><span class="sxs-lookup"><span data-stu-id="54bb8-124">Green</span></span>       |
| <span data-ttu-id="54bb8-125">0, 0255</span><span class="sxs-lookup"><span data-stu-id="54bb8-125">0,0,255</span></span>     | <span data-ttu-id="54bb8-126">Azul</span><span class="sxs-lookup"><span data-stu-id="54bb8-126">Blue</span></span>        |



 

<span data-ttu-id="54bb8-127">Si no utiliza botones de región, debe escribir lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="54bb8-127">If you do not use region buttons, you must enter the following:</span></span>


```C++
0,0,0

```



## <a name="related-topics"></a><span data-ttu-id="54bb8-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54bb8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54bb8-129">**Botones**</span><span class="sxs-lookup"><span data-stu-id="54bb8-129">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




