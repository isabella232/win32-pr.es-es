---
description: El elemento Group define un grupo, el objeto de nivel superior en una escala de tiempo.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997992"
---
# <a name="group-element"></a><span data-ttu-id="2921f-103">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="2921f-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="2921f-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2921f-104">\[Deprecated.</span></span> <span data-ttu-id="2921f-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2921f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2921f-106">El elemento **Group** define un grupo, el objeto de nivel superior en una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2921f-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="2921f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2921f-107">Attributes</span></span>

<span data-ttu-id="2921f-108">[**bitdepth**](bitdepth-attribute.md), [**almacenamiento en búfer**](buffering-attribute.md), [**velocidad de fotogramas**](framerate-attribute.md), [**alto**](height-attribute.md), [**bloqueo**](lock-attribute.md), [**silencio**](mute-attribute.md), [**nombre**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**Samplingrate**](samplingrate-attribute.md), [**tipo**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nombre de usuario**](username-attribute.md), [**ancho**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="2921f-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="2921f-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="2921f-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2921f-110">Parent</span><span class="sxs-lookup"><span data-stu-id="2921f-110">Parent</span></span>   | [<span data-ttu-id="2921f-111">**marco**</span><span class="sxs-lookup"><span data-stu-id="2921f-111">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="2921f-112">Children</span><span class="sxs-lookup"><span data-stu-id="2921f-112">Children</span></span> | <span data-ttu-id="2921f-113">[**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**seguimiento**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="2921f-113">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2921f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2921f-114">Remarks</span></span>

<span data-ttu-id="2921f-115">Dentro de un `group` elemento, la prioridad de las capas anidadas viene determinada implícitamente por el orden en que aparecen dentro del elemento.</span><span class="sxs-lookup"><span data-stu-id="2921f-115">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="2921f-116">La primera capa tiene prioridad 0 y las capas siguientes tienen valores de prioridad crecientes.</span><span class="sxs-lookup"><span data-stu-id="2921f-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="2921f-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2921f-117">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="2921f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2921f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2921f-119">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="2921f-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



