---
title: Tipo de botón
description: Tipo de botón
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Aspectos de Windows Media Player Mobile, tipos de botón
- máscaras, tipos de botón
- referencia de las máscaras, botones
- botones en máscaras, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903243"
---
# <a name="button-type"></a><span data-ttu-id="a4805-107">Tipo de botón</span><span class="sxs-lookup"><span data-stu-id="a4805-107">Button Type</span></span>

<span data-ttu-id="a4805-108">Los botones tienen dos tipos generales: ubicación y región.</span><span class="sxs-lookup"><span data-stu-id="a4805-108">Buttons come in two general types: location and region.</span></span> <span data-ttu-id="a4805-109">Cada tipo general tiene tres tipos específicos, lo que convierte seis tipos de botón en todos.</span><span class="sxs-lookup"><span data-stu-id="a4805-109">Each general type has three specific types, making six button types in all.</span></span>

> [!Note]  
> <span data-ttu-id="a4805-110">Los tipos de botones están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="a4805-110">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="a4805-111">Tipos de botón de ubicación</span><span class="sxs-lookup"><span data-stu-id="a4805-111">Location Button Types</span></span>

<span data-ttu-id="a4805-112">Los botones de ubicación usan coordenadas para definir sus ubicaciones en relación con el fondo.</span><span class="sxs-lookup"><span data-stu-id="a4805-112">Location buttons use coordinates to define their locations relative to the background.</span></span> <span data-ttu-id="a4805-113">En la tabla siguiente se muestran los valores que son válidos para los tipos de botón de ubicación.</span><span class="sxs-lookup"><span data-stu-id="a4805-113">The following table shows the values that are valid for location button types.</span></span> <span data-ttu-id="a4805-114">No es necesario definir valores para los tipos que no se vayan a usar en la máscara.</span><span class="sxs-lookup"><span data-stu-id="a4805-114">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="a4805-115">Value</span><span class="sxs-lookup"><span data-stu-id="a4805-115">Value</span></span>  | <span data-ttu-id="a4805-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4805-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4805-117">Inserción</span><span class="sxs-lookup"><span data-stu-id="a4805-117">Push</span></span>   | <span data-ttu-id="a4805-118">Define un botón que desencadena un evento una vez.</span><span class="sxs-lookup"><span data-stu-id="a4805-118">Defines a button that triggers an event once.</span></span> <span data-ttu-id="a4805-119">El botón se debe insertar cada vez para desencadenar eventos adicionales.</span><span class="sxs-lookup"><span data-stu-id="a4805-119">The button must be pushed each time to trigger further events.</span></span> <span data-ttu-id="a4805-120">Un ejemplo sería un botón que se desplaza al siguiente elemento de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a4805-120">An example would be a button that moves to the next item in the playlist.</span></span> <span data-ttu-id="a4805-121">La ubicación del botón se define mediante sus coordenadas.</span><span class="sxs-lookup"><span data-stu-id="a4805-121">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a4805-122">Alternancia</span><span class="sxs-lookup"><span data-stu-id="a4805-122">Toggle</span></span> | <span data-ttu-id="a4805-123">Define un botón que desencadena un evento que cambia un estado.</span><span class="sxs-lookup"><span data-stu-id="a4805-123">Defines a button that triggers an event that changes a state.</span></span> <span data-ttu-id="a4805-124">El estado permanecerá hasta que se vuelva a insertar el botón.</span><span class="sxs-lookup"><span data-stu-id="a4805-124">The state remains until the button is pushed again.</span></span> <span data-ttu-id="a4805-125">Un ejemplo es un botón que reordena la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a4805-125">An example is a button that shuffles the playlist.</span></span> <span data-ttu-id="a4805-126">Una vez que la lista de reproducción esté en un estado aleatorio, permanecerá en orden aleatorio hasta que el botón se vuelva a insertar.</span><span class="sxs-lookup"><span data-stu-id="a4805-126">Once the playlist is in a shuffled state, it will remain shuffled until the button is pushed again.</span></span> <span data-ttu-id="a4805-127">La ubicación del botón se define mediante sus coordenadas.</span><span class="sxs-lookup"><span data-stu-id="a4805-127">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a4805-128">2Push</span><span class="sxs-lookup"><span data-stu-id="a4805-128">2Push</span></span>  | <span data-ttu-id="a4805-129">Define un botón que desencadena un evento y, a continuación, cambia a un estado que está listo para desencadenar un evento diferente.</span><span class="sxs-lookup"><span data-stu-id="a4805-129">Defines a button that triggers an event, and then changes to a state that is ready to trigger a different event.</span></span> <span data-ttu-id="a4805-130">Los dos Estados se alternan cada vez que se inserta el botón.</span><span class="sxs-lookup"><span data-stu-id="a4805-130">The two states are toggled every time the button is pushed.</span></span> <span data-ttu-id="a4805-131">Un ejemplo es un botón que utiliza la función **playpause** para alternar entre reproducir y pausar el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="a4805-131">An example is a button that uses the **PlayPause** function to toggle between playing and pausing the current media item.</span></span> <span data-ttu-id="a4805-132">Cuando el botón se inserta por primera vez, se desencadena el estado de reproducción principal y se muestra una imagen secundaria para indicar que se puede desencadenar un evento de **pausa** .</span><span class="sxs-lookup"><span data-stu-id="a4805-132">When the button is pushed the first time, the primary Play state is triggered and a secondary image is displayed to indicate that a **Pause** event can be triggered.</span></span> <span data-ttu-id="a4805-133">Cuando el botón se vuelve a insertar, se desencadena el estado de pausa y se muestra la imagen original para indicar que se puede desencadenar un evento de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="a4805-133">When the button is pushed again, the Pause state is triggered and the original image is displayed to indicate that a **Play** event can be triggered.</span></span> <span data-ttu-id="a4805-134">La ubicación del botón se define mediante sus coordenadas.</span><span class="sxs-lookup"><span data-stu-id="a4805-134">The location of the button is defined by its coordinates.</span></span> |



 

<span data-ttu-id="a4805-135">Tipos de botón de región</span><span class="sxs-lookup"><span data-stu-id="a4805-135">Region Button Types</span></span>

<span data-ttu-id="a4805-136">Los botones de región usan áreas de color de la imagen de región para definir dónde se procesarán los grifos para un botón concreto.</span><span class="sxs-lookup"><span data-stu-id="a4805-136">Region buttons use color areas in the Region image to define where taps will be processed for a particular button.</span></span> <span data-ttu-id="a4805-137">En la tabla siguiente se muestran los valores que son válidos para los tipos de botón de región.</span><span class="sxs-lookup"><span data-stu-id="a4805-137">The following table shows the values that are valid for region button types.</span></span> <span data-ttu-id="a4805-138">No es necesario definir valores para los tipos que no se vayan a usar en la máscara.</span><span class="sxs-lookup"><span data-stu-id="a4805-138">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="a4805-139">Value</span><span class="sxs-lookup"><span data-stu-id="a4805-139">Value</span></span>     | <span data-ttu-id="a4805-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4805-140">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4805-141">PushHit</span><span class="sxs-lookup"><span data-stu-id="a4805-141">PushHit</span></span>   | <span data-ttu-id="a4805-142">Similar al valor del botón de la tecla de acceso, salvo que el área de aciertos del botón se define mediante el valor de color de la imagen de la región.</span><span class="sxs-lookup"><span data-stu-id="a4805-142">Similar to the Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>   |
| <span data-ttu-id="a4805-143">ToggleHit</span><span class="sxs-lookup"><span data-stu-id="a4805-143">ToggleHit</span></span> | <span data-ttu-id="a4805-144">Similar al valor del botón de alternancia, salvo que el área de aciertos del botón se define mediante el valor de color de la imagen de la región.</span><span class="sxs-lookup"><span data-stu-id="a4805-144">Similar to the Toggle button value except that the hit area of the button is defined by the color value in the Region image.</span></span> |
| <span data-ttu-id="a4805-145">2PushHit</span><span class="sxs-lookup"><span data-stu-id="a4805-145">2PushHit</span></span>  | <span data-ttu-id="a4805-146">Similar al valor del botón 2Push, excepto que el área de aciertos del botón se define mediante el valor de color de la imagen de la región.</span><span class="sxs-lookup"><span data-stu-id="a4805-146">Similar to the 2Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="a4805-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4805-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4805-148">**Botones**</span><span class="sxs-lookup"><span data-stu-id="a4805-148">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




