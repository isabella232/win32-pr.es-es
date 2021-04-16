---
description: El clip epecifies un origen multimedia.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494500"
---
# <a name="clip-element"></a><span data-ttu-id="21232-103">Elemento clip</span><span class="sxs-lookup"><span data-stu-id="21232-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="21232-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="21232-104">\[Deprecated.</span></span> <span data-ttu-id="21232-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="21232-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21232-106">`clip`Epecifies un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="21232-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="21232-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="21232-107">Attributes</span></span>

<span data-ttu-id="21232-108">[**CLSID**](clsid-attribute.md), [**velocidad de fotogramas**](framerate-attribute.md), [**bloqueo**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**silenciar**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="21232-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="21232-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="21232-109">Parent/Child Information</span></span>



|          |                                  |
|----------|----------------------------------|
| <span data-ttu-id="21232-110">Parent</span><span class="sxs-lookup"><span data-stu-id="21232-110">Parent</span></span>   | [<span data-ttu-id="21232-111">**track**</span><span class="sxs-lookup"><span data-stu-id="21232-111">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="21232-112">Children</span><span class="sxs-lookup"><span data-stu-id="21232-112">Children</span></span> | [<span data-ttu-id="21232-113">**realizado**</span><span class="sxs-lookup"><span data-stu-id="21232-113">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="21232-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21232-114">Remarks</span></span>

<span data-ttu-id="21232-115">El atributo **CLSID** especifica el CLSID de un filtro de origen que se va a utilizar como origen.</span><span class="sxs-lookup"><span data-stu-id="21232-115">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="21232-116">No especifique los atributos **src** y **CLSID** en el mismo `clip` elemento.</span><span class="sxs-lookup"><span data-stu-id="21232-116">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="21232-117">Especifique al menos un atributo de tiempo de inicio (**Start** o **mstart**) y un atributo de tiempo de parada (**Stop** o **mstop**).</span><span class="sxs-lookup"><span data-stu-id="21232-117">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="21232-118">Si no se especifica uno de los atributos de hora de inicio, el valor predeterminado es 0 (el principio de la escala de tiempo para el **Inicio** o el principio del clip para **mstart**).</span><span class="sxs-lookup"><span data-stu-id="21232-118">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="21232-119">Si no se especifica uno de los atributos de tiempo de parada, DES supone una velocidad de reproducción normal y calcula la hora de detención no especificada en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="21232-119">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="21232-120">Si se especifican ambas horas de detención, la reproducción es más rápida o más lenta que la normal, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="21232-120">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="21232-121">En el ejemplo siguiente, la duración de la escala de tiempo es de siete segundos (**detener** menos **Inicio**).</span><span class="sxs-lookup"><span data-stu-id="21232-121">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="21232-122">Se presupone la velocidad de reproducción normal, por lo que el tiempo de detención del medio predeterminado es de 10 segundos (la duración más **mstart**).</span><span class="sxs-lookup"><span data-stu-id="21232-122">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="21232-123">En el ejemplo siguiente, el valor predeterminado de la hora de inicio del medio es 0, lo que obliga a que la duración del medio sea de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="21232-123">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="21232-124">La duración de la escala de tiempo es de cinco segundos, por lo que el clip vuelve a reproducirse dos veces la tarifa normal.</span><span class="sxs-lookup"><span data-stu-id="21232-124">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="21232-125">Si el atributo **src** especifica una imagen fija, des intenta cargar una serie de imágenes fijas para crear una animación.</span><span class="sxs-lookup"><span data-stu-id="21232-125">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="21232-126">Por ejemplo, si el atributo **src** es IMAGE001.BMP, DES busca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, etc.</span><span class="sxs-lookup"><span data-stu-id="21232-126">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="21232-127">Suponiendo que existen, se muestran en orden numérico secuencial, a la velocidad especificada por el atributo de **velocidad de fotogramas** .</span><span class="sxs-lookup"><span data-stu-id="21232-127">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="21232-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="21232-128">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="21232-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="21232-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21232-130">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="21232-130">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



