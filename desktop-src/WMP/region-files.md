---
title: Archivos de regiones
description: Archivos de regiones
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos de regiones
- Aspectos móviles de Windows Media Player, archivos de regiones
- máscaras, archivos de regiones
- Archivos de regiones en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357631"
---
# <a name="region-files"></a><span data-ttu-id="c438b-110">Archivos de regiones</span><span class="sxs-lookup"><span data-stu-id="c438b-110">Region Files</span></span>

<span data-ttu-id="c438b-111">Los archivos de regiones son necesarios si se usa cualquier tipo de botón de posicionamiento (2PushHit, PushHit o ToggleHit).</span><span class="sxs-lookup"><span data-stu-id="c438b-111">Region files are required if you use any type of hit button (2PushHit, PushHit, or ToggleHit).</span></span>

<span data-ttu-id="c438b-112">Los archivos de región se usan para definir áreas que responderán a una pulsación, también conocida como golpe, en un botón específico.</span><span class="sxs-lookup"><span data-stu-id="c438b-112">Region files are used to define areas that will respond to a tap, also known as a hit, on a specific button.</span></span> <span data-ttu-id="c438b-113">Para cada botón de posicionamiento, se asigna un color Web específico a un área en el mapa de bits de la región (por ejemplo \# , FF0000, que es el valor de rojo sólido).</span><span class="sxs-lookup"><span data-stu-id="c438b-113">For each hit button, an area in the Region bitmap is given a specific Web color (such as \#FF0000, which is the value for solid red).</span></span> <span data-ttu-id="c438b-114">El número de color se especifica en la definición del botón de región.</span><span class="sxs-lookup"><span data-stu-id="c438b-114">The color number is specified in the region button definition.</span></span> <span data-ttu-id="c438b-115">Cuando el usuario muestra la máscara, la imagen del botón se superpone en el fondo mediante las coordenadas del área en el mapa de bits de la región.</span><span class="sxs-lookup"><span data-stu-id="c438b-115">When the user displays the skin, the button image is superimposed onto the background using the coordinates of the area in the Region bitmap.</span></span>

<span data-ttu-id="c438b-116">Por ejemplo, puede dibujar un círculo rojo en una ubicación que corresponda a la ubicación del botón siguiente y colorearlo en rojo sólido ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="c438b-116">For example, you could draw a red circle in a location corresponding to the location of the Next button and color it solid red (\#FF0000).</span></span> <span data-ttu-id="c438b-117">Después, en la definición del botón, podría asignar un valor RGB de posicionamiento de 255, 0, 0 (que es el equivalente RGB de \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="c438b-117">Then in the button definition, you could assign a hit RGB value of 255,0,0 (which is the RGB equivalent of \#FF0000).</span></span> <span data-ttu-id="c438b-118">En este caso, el botón siguiente solo respondería a los grifos (aciertos) dentro del círculo rojo.</span><span class="sxs-lookup"><span data-stu-id="c438b-118">In this case, the Next button would only respond to taps (hits) inside the red circle.</span></span>

<span data-ttu-id="c438b-119">Los botones de acceso se utilizan cuando se desea definir formas que no sean rectángulos.</span><span class="sxs-lookup"><span data-stu-id="c438b-119">Hit buttons are used when you want to define shapes other than rectangles.</span></span> <span data-ttu-id="c438b-120">Todavía debe definir las coordenadas de cada botón para que las imágenes secundarias, como Insert y Disabled, se puedan encontrar correctamente.</span><span class="sxs-lookup"><span data-stu-id="c438b-120">You must still define the coordinates for each button so that secondary images such as Pushed and Disabled can be located correctly.</span></span> <span data-ttu-id="c438b-121">En la práctica, cada botón está limitado por un rectángulo y estos rectángulos de límite imaginarios no deben superponerse.</span><span class="sxs-lookup"><span data-stu-id="c438b-121">In practice, each button is bounded by a rectangle, and these imaginary boundary rectangles must not overlap.</span></span>

> [!Note]  
> <span data-ttu-id="c438b-122">Los archivos de región no son necesarios en las máscaras móviles de Windows Media Player 10 porque los tipos de botón no se admiten en Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="c438b-122">Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="c438b-123">La siguiente imagen es un archivo de región típico.</span><span class="sxs-lookup"><span data-stu-id="c438b-123">The following image is a typical Region file.</span></span>

![archivo de región](images/cesdkreg.png)

<span data-ttu-id="c438b-125">Este archivo define los elementos de la máscara para cada botón de tipo de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="c438b-125">This file defines the parts of the skin for each hit-type button.</span></span> <span data-ttu-id="c438b-126">Cada color se identificará por su número de color en la sección botones del archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="c438b-126">Each color will be identified by its color number in the Buttons section of the skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c438b-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c438b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c438b-128">**Archivos de imagen**</span><span class="sxs-lookup"><span data-stu-id="c438b-128">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




