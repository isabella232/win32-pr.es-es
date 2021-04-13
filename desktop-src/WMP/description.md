---
title: Descripción (SDK de Windows Media Player)
description: Descripción
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Aspectos de Windows Media Player Mobile, sección Descripción
- aspectos, sección Descripción
- referencia de las máscaras, sección Descripción
- Sección de descripción en máscaras
- archivos de definición de máscara, sección Descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421823"
---
# <a name="description-windows-media-player-sdk"></a><span data-ttu-id="2597a-108">Descripción (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="2597a-108">Description (Windows Media Player SDK)</span></span>

<span data-ttu-id="2597a-109">Al crear una máscara para Windows Media Player 9 series para Windows Mobile 2003 o posterior, debe incluir una sección de descripción.</span><span class="sxs-lookup"><span data-stu-id="2597a-109">When you create a skin for Windows Media Player 9 Series for Windows Mobile 2003 or later, you must include a Description section.</span></span> <span data-ttu-id="2597a-110">La sección Descripción le permite especificar el ancho y el alto de la pantalla, la resolución de pantalla y la orientación de la pantalla para la que se diseñó la máscara.</span><span class="sxs-lookup"><span data-stu-id="2597a-110">The Description section enables you to specify the width and height of the display, the display resolution, and the display orientation for which the skin was designed.</span></span> <span data-ttu-id="2597a-111">La sección Descripción debe aparecer en el archivo de definición de máscara antes que cualquier otra sección y justo después de la declaración de versión inicial.</span><span class="sxs-lookup"><span data-stu-id="2597a-111">The Description section must appear in the skin definition file before any other section, and just after the initial version declaration.</span></span>

<span data-ttu-id="2597a-112">La sección de Descripción del archivo de definición de máscara debe comenzar con la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="2597a-112">The Description section of the skin definition file must begin with the following line:</span></span>


```C++
[ Description ]

```



<span data-ttu-id="2597a-113">A continuación, debe agregar información sobre las dimensiones de la máscara y la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2597a-113">You then must add information about the dimensions of the skin and the display resolution.</span></span> <span data-ttu-id="2597a-114">En el ejemplo siguiente se muestra cómo especificar dimensiones:</span><span class="sxs-lookup"><span data-stu-id="2597a-114">The following example shows how to specify dimensions:</span></span>


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



<span data-ttu-id="2597a-115">Esto especifica que se ha diseñado la máscara para mostrar 240 píxeles de ancho, 320 píxeles de alto y el uso de la resolución de pantalla de PPP de 96.</span><span class="sxs-lookup"><span data-stu-id="2597a-115">This specifies that you designed the skin to be displayed 240 pixels wide, 320 pixels high, and using 96 DPI display resolution.</span></span> <span data-ttu-id="2597a-116">Tenga en cuenta que esto implica una orientación en modo vertical.</span><span class="sxs-lookup"><span data-stu-id="2597a-116">Note that this implies a portrait mode orientation.</span></span>

<span data-ttu-id="2597a-117">Opcionalmente, puede especificar el modo de orientación para el que ha diseñado la máscara en la sección Descripción.</span><span class="sxs-lookup"><span data-stu-id="2597a-117">You may optionally specify the orientation mode for which you designed the skin in the description section.</span></span> <span data-ttu-id="2597a-118">En el ejemplo siguiente se muestra cómo especificar la orientación:</span><span class="sxs-lookup"><span data-stu-id="2597a-118">The following example shows how to specify orientation:</span></span>


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



<span data-ttu-id="2597a-119">En la tabla siguiente se muestran los valores que puede usar para la orientación.</span><span class="sxs-lookup"><span data-stu-id="2597a-119">The following table lists the values you may use for Orientation.</span></span>



| <span data-ttu-id="2597a-120">Orientación</span><span class="sxs-lookup"><span data-stu-id="2597a-120">Orientation</span></span> | <span data-ttu-id="2597a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2597a-121">Description</span></span>                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2597a-122">Horizontal</span><span class="sxs-lookup"><span data-stu-id="2597a-122">Landscape</span></span>   | <span data-ttu-id="2597a-123">El ancho de la máscara es mayor que el alto de la máscara.</span><span class="sxs-lookup"><span data-stu-id="2597a-123">The width of the skin is greater than height of the skin.</span></span> <span data-ttu-id="2597a-124">La presentación está orientada horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="2597a-124">The display is oriented in a horizontal fashion.</span></span>   |
| <span data-ttu-id="2597a-125">Vertical</span><span class="sxs-lookup"><span data-stu-id="2597a-125">Portrait</span></span>    | <span data-ttu-id="2597a-126">El alto de la máscara es mayor que el ancho de la máscara.</span><span class="sxs-lookup"><span data-stu-id="2597a-126">The height of the skin is greater than the width of the skin.</span></span> <span data-ttu-id="2597a-127">La presentación está orientada verticalmente.</span><span class="sxs-lookup"><span data-stu-id="2597a-127">The display is oriented in a vertical fashion.</span></span> |
| <span data-ttu-id="2597a-128">Square</span><span class="sxs-lookup"><span data-stu-id="2597a-128">Square</span></span>      | <span data-ttu-id="2597a-129">El alto de la máscara es igual al ancho de la máscara.</span><span class="sxs-lookup"><span data-stu-id="2597a-129">The height of the skin is equal to the width of the skin.</span></span> <span data-ttu-id="2597a-130">La pantalla no tiene ninguna orientación.</span><span class="sxs-lookup"><span data-stu-id="2597a-130">The display has no orientation.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="2597a-131">Windows Media Player 9 series para Windows Mobile 2003 solo mostrará una máscara determinada cuando la sección de descripción especificada en el archivo de definición de máscara coincida con el estado actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2597a-131">Windows Media Player 9 Series for Windows Mobile 2003 will only display a particular skin when the description section specified in the skin definition file matches the current state of the device.</span></span>

 

<span data-ttu-id="2597a-132">Debe tener cuidado de especificar siempre las dimensiones, la resolución y la orientación correctas para los que se creó la máscara.</span><span class="sxs-lookup"><span data-stu-id="2597a-132">You should be careful to always specify the correct dimensions, resolution, and orientation for which your skin was authored.</span></span> <span data-ttu-id="2597a-133">Por ejemplo, si las dimensiones especificadas por la máscara describen una orientación horizontal, la máscara no estará disponible cuando el dispositivo esté en modo vertical, aunque especifique vertical en la línea de orientación.</span><span class="sxs-lookup"><span data-stu-id="2597a-133">For example, if the dimensions specified by your skin describe a landscape orientation, your skin will not be available when the device is in portrait mode, even if you specify Portrait in the orientation line.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2597a-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2597a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2597a-135">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="2597a-135">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




