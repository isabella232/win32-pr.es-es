---
description: El clip epecifica un origen multimedia.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: clip (Elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d937f942ba7b564e65b0e37d9c11929805287da
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908673"
---
# <a name="clip-element"></a><span data-ttu-id="0633e-103">clip (Elemento)</span><span class="sxs-lookup"><span data-stu-id="0633e-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="0633e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="0633e-104">\[Deprecated.</span></span> <span data-ttu-id="0633e-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0633e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0633e-106">`clip`epecifica un origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="0633e-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="0633e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0633e-107">Attributes</span></span>

<span data-ttu-id="0633e-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="0633e-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="0633e-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="0633e-109">Parent/Child Information</span></span>



| <span data-ttu-id="0633e-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="0633e-110">Label</span></span> | <span data-ttu-id="0633e-111">Value</span><span class="sxs-lookup"><span data-stu-id="0633e-111">Value</span></span> |
|----------|----------------------------------|
| <span data-ttu-id="0633e-112">Parent</span><span class="sxs-lookup"><span data-stu-id="0633e-112">Parent</span></span>   | [<span data-ttu-id="0633e-113">**track**</span><span class="sxs-lookup"><span data-stu-id="0633e-113">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="0633e-114">Children</span><span class="sxs-lookup"><span data-stu-id="0633e-114">Children</span></span> | [<span data-ttu-id="0633e-115">**Efecto**</span><span class="sxs-lookup"><span data-stu-id="0633e-115">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="0633e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0633e-116">Remarks</span></span>

<span data-ttu-id="0633e-117">El **atributo clsid** especifica el CLSID de un filtro de origen que se usará como origen.</span><span class="sxs-lookup"><span data-stu-id="0633e-117">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="0633e-118">No especifique los **atributos src** **y clsid** dentro del mismo `clip` elemento.</span><span class="sxs-lookup"><span data-stu-id="0633e-118">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="0633e-119">Especifique al menos un atributo de hora de inicio **(start** o **mstart)** y un atributo de tiempo de detenerse **(stop** o **mstop).**</span><span class="sxs-lookup"><span data-stu-id="0633e-119">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="0633e-120">Si uno de los atributos de hora de inicio no está especificado, el valor predeterminado es 0 (el principio de la escala de tiempo para **start** o el principio del clip para **mstart**).</span><span class="sxs-lookup"><span data-stu-id="0633e-120">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="0633e-121">Si uno de los atributos de tiempo de detenerse no está especificado, DES asume una velocidad de reproducción normal y calcula el tiempo de detenerse no especificado en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="0633e-121">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="0633e-122">Si se especifican ambos tiempos de detenerse, la reproducción es más rápida o más lenta de lo normal, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="0633e-122">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="0633e-123">En el ejemplo siguiente, la duración de la escala de tiempo es de siete segundos **(detener** menos **iniciar**).</span><span class="sxs-lookup"><span data-stu-id="0633e-123">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="0633e-124">Se supone que la velocidad de reproducción es normal, por lo que el tiempo de detenerse de los medios es predeterminado de 10 segundos (la duración más **mstart).**</span><span class="sxs-lookup"><span data-stu-id="0633e-124">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="0633e-125">En el ejemplo siguiente, el valor predeterminado de la hora de inicio del medio es 0, lo que obliga a que la duración del medio sea de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="0633e-125">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="0633e-126">La duración de la escala de tiempo es de cinco segundos, por lo que el clip se reproduce al doble de la velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="0633e-126">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="0633e-127">Si el **atributo src** especifica una imagen fija, DES intenta cargar una serie de imágenes fijas para crear una animación.</span><span class="sxs-lookup"><span data-stu-id="0633e-127">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="0633e-128">Por ejemplo, si el **atributo src** IMAGE001.BMP, DES busca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="0633e-128">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="0633e-129">Suponiendo que existen, se muestran en orden numérico secuencial, a la velocidad especificada por el atributo **de velocidad de** fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0633e-129">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="0633e-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0633e-130">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="0633e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0633e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0633e-132">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="0633e-132">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



