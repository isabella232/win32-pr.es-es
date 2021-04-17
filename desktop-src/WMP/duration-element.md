---
title: Elemento DURATION
description: El elemento DURATION define el período de tiempo durante el cual Windows Media Player representará la entrada de lista de reproducción asociada.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Elemento DURATION de Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700119"
---
# <a name="duration-element"></a><span data-ttu-id="08cf6-104">Elemento DURATION</span><span class="sxs-lookup"><span data-stu-id="08cf6-104">DURATION Element</span></span>

<span data-ttu-id="08cf6-105">El elemento **Duration** define el período de tiempo durante el cual Windows Media Player representará la entrada de lista de reproducción asociada.</span><span class="sxs-lookup"><span data-stu-id="08cf6-105">The **DURATION** element defines the length of time Windows Media Player will render the associated playlist entry.</span></span>

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="08cf6-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="08cf6-106">Attributes</span></span>

<span data-ttu-id="08cf6-107">**Valor** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="08cf6-107">**VALUE** (required)</span></span>

<span data-ttu-id="08cf6-108">La cantidad de tiempo, en horas, minutos, segundos y centésimas de segundo, que representa una entrada de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="08cf6-108">The length of time, in hours, minutes, seconds, and hundredths of a second, that an entry is rendered by Windows Media Player.</span></span> <span data-ttu-id="08cf6-109">El valor predeterminado es la longitud total de la entrada.</span><span class="sxs-lookup"><span data-stu-id="08cf6-109">The default value is the entire length of the entry.</span></span> <span data-ttu-id="08cf6-110">Si la entrada es un archivo gráfico, debe especificarse un valor de duración.</span><span class="sxs-lookup"><span data-stu-id="08cf6-110">If the entry is a graphic file, a duration value must be specified.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="08cf6-111">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="08cf6-111">Parent/Child Elements</span></span>



| <span data-ttu-id="08cf6-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="08cf6-112">Hierarchy</span></span>       | <span data-ttu-id="08cf6-113">Elementos</span><span class="sxs-lookup"><span data-stu-id="08cf6-113">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="08cf6-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="08cf6-114">Parent elements</span></span> | <span data-ttu-id="08cf6-115">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="08cf6-115">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="08cf6-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08cf6-116">Child elements</span></span>  | <span data-ttu-id="08cf6-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="08cf6-117">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="08cf6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08cf6-118">Remarks</span></span>

<span data-ttu-id="08cf6-119">Este elemento define el período de tiempo que se va a representar una secuencia.</span><span class="sxs-lookup"><span data-stu-id="08cf6-119">This element defines the length of time a stream is to be rendered.</span></span> <span data-ttu-id="08cf6-120">Si el atributo de **valor** supera la longitud de la secuencia de contenido, la secuencia finaliza en su punto final normal.</span><span class="sxs-lookup"><span data-stu-id="08cf6-120">If the **VALUE** attribute exceeds the length of the content stream, the stream terminates at its normal end-point.</span></span>

<span data-ttu-id="08cf6-121">Este elemento puede aparecer dentro de un elemento **ref** o dentro de un elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="08cf6-121">This element can appear either within a **REF** element or within an **ENTRY** element.</span></span> <span data-ttu-id="08cf6-122">Sin embargo, un elemento **Duration** definido dentro de un elemento **ref** reemplaza a uno que aparece dentro del elemento de **entrada** primario del elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="08cf6-122">However, a **DURATION** element defined within a **REF** element overrides one that appears within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="08cf6-123">El elemento **Duration** invalida un elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="08cf6-123">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="08cf6-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08cf6-124">Examples</span></span>


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a><span data-ttu-id="08cf6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08cf6-125">Requirements</span></span>



| <span data-ttu-id="08cf6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="08cf6-126">Requirement</span></span> | <span data-ttu-id="08cf6-127">Value</span><span class="sxs-lookup"><span data-stu-id="08cf6-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="08cf6-128">Versión</span><span class="sxs-lookup"><span data-stu-id="08cf6-128">Version</span></span><br/> | <span data-ttu-id="08cf6-129">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="08cf6-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08cf6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="08cf6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08cf6-131">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="08cf6-131">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="08cf6-132">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="08cf6-132">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





