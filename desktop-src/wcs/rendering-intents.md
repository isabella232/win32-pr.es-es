---
title: Intenciones de representación
description: El International color Consortium (ICC) ha definido cuatro valores distintos denominados representación del intents.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Sistema de color de Windows (WCS), representación de intenciones
- WCS (sistema de colores de Windows), representación de intenciones
- Administración del color de imagen, representación de intenciones
- Administración del color, representación de intenciones
- colores, representación de intenciones
- representación de intenciones
- International Color Consortium (ICC)
- IIC (International color Consortium)
- Intento de imagen
- Intención de gráficos
- Intento de prueba
- Intento de coincidencia
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721385"
---
# <a name="rendering-intents"></a><span data-ttu-id="79c5d-115">Intenciones de representación</span><span class="sxs-lookup"><span data-stu-id="79c5d-115">Rendering Intents</span></span>

<span data-ttu-id="79c5d-116">El International color Consortium (ICC) ha definido cuatro valores distintos denominados *representación del intents*.</span><span class="sxs-lookup"><span data-stu-id="79c5d-116">The International Color Consortium (ICC) has defined four different values called *rendering intents*.</span></span> <span data-ttu-id="79c5d-117">Representan cuatro enfoques diferentes para crear una representación de color.</span><span class="sxs-lookup"><span data-stu-id="79c5d-117">These represent four different approaches to creating a color rendering.</span></span> <span data-ttu-id="79c5d-118">Estas cuatro intenciones y las constantes que se usan para hacer referencia a ellas en el código son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="79c5d-118">These four intents, and the constants used to refer to them in code are as follows.</span></span>



| <span data-ttu-id="79c5d-119">Intención</span><span class="sxs-lookup"><span data-stu-id="79c5d-119">Intent</span></span>                            | <span data-ttu-id="79c5d-120">Nombre de ICC</span><span class="sxs-lookup"><span data-stu-id="79c5d-120">ICC Name</span></span>              | <span data-ttu-id="79c5d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="79c5d-121">Description</span></span>                    |
|-----------------------------------|-----------------------|--------------------------------|
| <span data-ttu-id="79c5d-122">Imagen</span><span class="sxs-lookup"><span data-stu-id="79c5d-122">Picture</span></span> | <span data-ttu-id="79c5d-123">Perceptual</span><span class="sxs-lookup"><span data-stu-id="79c5d-123">Perceptual</span></span>            | <span data-ttu-id="79c5d-124">INTENCIÓN \_ perceptual</span><span class="sxs-lookup"><span data-stu-id="79c5d-124">INTENT\_PERCEPTUAL</span></span>             |
| <span data-ttu-id="79c5d-125">Graphic</span><span class="sxs-lookup"><span data-stu-id="79c5d-125">Graphic</span></span> | <span data-ttu-id="79c5d-126">Saturación</span><span class="sxs-lookup"><span data-stu-id="79c5d-126">Saturation</span></span>            | <span data-ttu-id="79c5d-127">saturación de intención \_</span><span class="sxs-lookup"><span data-stu-id="79c5d-127">INTENT\_SATURATION</span></span>             |
| <span data-ttu-id="79c5d-128">Prueba</span><span class="sxs-lookup"><span data-stu-id="79c5d-128">Proof</span></span>     | <span data-ttu-id="79c5d-129">Colorimétrico relativo</span><span class="sxs-lookup"><span data-stu-id="79c5d-129">Relative Colorimetric</span></span> | <span data-ttu-id="79c5d-130">\_referencia \_ colorimétrica relativa</span><span class="sxs-lookup"><span data-stu-id="79c5d-130">INTENT\_RELATIVE\_COLORIMETRIC</span></span> |
| <span data-ttu-id="79c5d-131">Match</span><span class="sxs-lookup"><span data-stu-id="79c5d-131">Match</span></span>     | <span data-ttu-id="79c5d-132">Colorimétrico absoluto</span><span class="sxs-lookup"><span data-stu-id="79c5d-132">Absolute Colorimetric</span></span> | <span data-ttu-id="79c5d-133">INTENCIÓN \_ absoluta \_ colorimétrica</span><span class="sxs-lookup"><span data-stu-id="79c5d-133">INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> |




 

<span data-ttu-id="79c5d-134">La especificación de formato de Perfil de ICC versión 3,4, que describe estas intenciones, se puede descargar desde color.org.</span><span class="sxs-lookup"><span data-stu-id="79c5d-134">The ICC Profile Format Specification Version 3.4, which describes these intents, can be downloaded from color.org.</span></span>

## <a name="picture-intent"></a><span data-ttu-id="79c5d-135">Intento de imagen</span><span class="sxs-lookup"><span data-stu-id="79c5d-135">Picture Intent</span></span>

<span data-ttu-id="79c5d-136">Llamada perceptual en la cláusula 4,9 de la especificación de ICC, una intención de imagen hace que la [gama](./g.md) completa de la imagen se comprima o se expanda para rellenar la gama del dispositivo de destino, de modo que se conserve el equilibrio de gris, pero no se conserve la precisión de la colorimétrico.</span><span class="sxs-lookup"><span data-stu-id="79c5d-136">Called perceptual intent in the ICC specification clause 4.9, a Picture intent causes the full [gamut](./g.md) of the image to be compressed or expanded to fill the gamut of the destination device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span>

<span data-ttu-id="79c5d-137">En otras palabras, si ciertos colores de una imagen quedan fuera del intervalo de colores que el dispositivo de salida puede representar, el intento de imagen hará que se ajusten todos los colores de la imagen para que todos los colores de la imagen se encuentren dentro del intervalo que se puede representar y para que la relación entre los colores se conserve lo máximo posible.</span><span class="sxs-lookup"><span data-stu-id="79c5d-137">In other words, if certain colors in an image fall outside of the range of colors that the output device can render, the picture intent will cause all the colors in the image to be adjusted so that the every color in the image falls within the range that can be rendered and so that the relationship between colors is preserved as much as possible.</span></span>

<span data-ttu-id="79c5d-138">Esta intención es más adecuada para la presentación de fotografías e imágenes, y suele ser la intención predeterminada.</span><span class="sxs-lookup"><span data-stu-id="79c5d-138">This intent is most suitable for display of photographs and images, and is generally the default intent.</span></span>

## <a name="graphic-intent"></a><span data-ttu-id="79c5d-139">Intención de gráficos</span><span class="sxs-lookup"><span data-stu-id="79c5d-139">Graphic Intent</span></span>

<span data-ttu-id="79c5d-140">La cláusula 4,12 de la especificación de ICC llama al gráfico como intención de [saturación](s.md) .</span><span class="sxs-lookup"><span data-stu-id="79c5d-140">The ICC specification clause 4.12 calls the Graphic intent a [saturation](s.md) intent.</span></span> <span data-ttu-id="79c5d-141">Conserva el croma de los colores de la imagen con el posible gasto de [matiz](h.md) y [luminosidad](l.md).</span><span class="sxs-lookup"><span data-stu-id="79c5d-141">It preserves the chroma of colors in the image at the possible expense of [hue](h.md) and [lightness](l.md).</span></span>

<span data-ttu-id="79c5d-142">La implementación de esta intención sigue siendo problemática y el ICC sigue trabajando en métodos para lograr los efectos deseados.</span><span class="sxs-lookup"><span data-stu-id="79c5d-142">Implementation of this intent remains somewhat problematic, and the ICC is still working on methods to achieve the desired effects.</span></span>

<span data-ttu-id="79c5d-143">Esta intención es más adecuada para los gráficos empresariales, como los gráficos, donde es más importante que los colores sean intensos y contrasten bien entre sí, en lugar de con un color específico.</span><span class="sxs-lookup"><span data-stu-id="79c5d-143">This intent is most suitable for business graphics such as charts, where it is more important that the colors be vivid and contrast well with each other rather than a specific color.</span></span>

## <a name="proof-intent"></a><span data-ttu-id="79c5d-144">Intento de prueba</span><span class="sxs-lookup"><span data-stu-id="79c5d-144">Proof Intent</span></span>

<span data-ttu-id="79c5d-145">El intento de prueba, denominado el intento de colorimétrica en la especificación de ICC, se define de forma que los colores que se encuentran fuera del intervalo que el dispositivo de salida pueda representar se ajusten al color más cercano que se puede representar, mientras que todos los demás colores quedan inalterados.</span><span class="sxs-lookup"><span data-stu-id="79c5d-145">The Proof intent, called the colorimetric intent in the ICC specification, is defined such that any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span>

<span data-ttu-id="79c5d-146">El intento de prueba no conserva el [punto blanco](w.md).</span><span class="sxs-lookup"><span data-stu-id="79c5d-146">Proof intent does not preserve the [white point](w.md).</span></span>

<span data-ttu-id="79c5d-147">Por ejemplo, el blanco más blanco de un papel es más amarillo que el blanco más blanco de un monitor de equipo.</span><span class="sxs-lookup"><span data-stu-id="79c5d-147">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="79c5d-148">Una imagen convertida en la gama de la impresora con la intención colorimétrico relativo haría que todos los colores se convirtieran en más amarillo.</span><span class="sxs-lookup"><span data-stu-id="79c5d-148">An image converted into the gamut of the printer using relative colorimetric intent would result in all colors becoming more yellow.</span></span> <span data-ttu-id="79c5d-149">El punto blanco de la imagen se mueve para que coincida con el punto blanco de la impresora.</span><span class="sxs-lookup"><span data-stu-id="79c5d-149">The white point of the image is moved to match the white point of the printer.</span></span> <span data-ttu-id="79c5d-150">Todos los demás colores de la imagen mantienen su posición en relación con el punto blanco.</span><span class="sxs-lookup"><span data-stu-id="79c5d-150">All other colors in the image keep their position relative to the white point.</span></span> <span data-ttu-id="79c5d-151">Esto produce una imagen que refleja con más precisión el aspecto que tendrá la imagen impresa.</span><span class="sxs-lookup"><span data-stu-id="79c5d-151">This produces an image that more accurately reflects what the printed image will look like.</span></span> <span data-ttu-id="79c5d-152">Sin embargo, el usuario puede encontrarla desconcertado visualmente.</span><span class="sxs-lookup"><span data-stu-id="79c5d-152">However, the user may find it visually disconcerting.</span></span>

## <a name="match-intent"></a><span data-ttu-id="79c5d-153">Intento de coincidencia</span><span class="sxs-lookup"><span data-stu-id="79c5d-153">Match Intent</span></span>

<span data-ttu-id="79c5d-154">En un intento de coincidencia, los colores que se encuentran fuera del intervalo que el dispositivo de salida puede representar se ajustan al color más cercano que se puede representar, mientras que todos los demás colores permanecen inalterados.</span><span class="sxs-lookup"><span data-stu-id="79c5d-154">In a Match intent, any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span> <span data-ttu-id="79c5d-155">La especificación ICC llama al intento de coincidencia de la intención de colorimétrico absoluto.</span><span class="sxs-lookup"><span data-stu-id="79c5d-155">The ICC specification calls the match intent absolute colorimetric intent.</span></span>

<span data-ttu-id="79c5d-156">La intención de coincidencia conserva el punto blanco.</span><span class="sxs-lookup"><span data-stu-id="79c5d-156">Match intent preserves the white point.</span></span>

<span data-ttu-id="79c5d-157">Por ejemplo, el blanco más blanco de un papel es más amarillo que el blanco más blanco de un monitor de equipo.</span><span class="sxs-lookup"><span data-stu-id="79c5d-157">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="79c5d-158">Una imagen convertida en la [gama](./g.md) de la impresora con la intención de coincidencia haría que todos los colores se convirtieran y coincidían con la gama de la impresora.</span><span class="sxs-lookup"><span data-stu-id="79c5d-158">An image converted into the [gamut](./g.md) of the printer using match intent would result in all colors being converted and matched into the gamut of the printer.</span></span> <span data-ttu-id="79c5d-159">El punto blanco de la imagen no se mueve para que coincida con el punto blanco de la impresora.</span><span class="sxs-lookup"><span data-stu-id="79c5d-159">The white point of the image is not moved to match the white point of the printer.</span></span> <span data-ttu-id="79c5d-160">Por lo tanto, la distancia de los colores al punto blanco puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="79c5d-160">Therefore, the distance of the colors to the white point may change.</span></span> <span data-ttu-id="79c5d-161">Esto produce una imagen que es menos visualmente disparando al usuario, pero también es una representación menos precisa de la salida de la impresora.</span><span class="sxs-lookup"><span data-stu-id="79c5d-161">This produces an image that is less visually disconcerting to the user, but is also a less accurate rendition of printer output.</span></span>

 

 