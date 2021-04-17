---
title: Elemento STARTMARKER
description: El elemento STARTMARKER especifica un marcador desde el que Windows Media Player comenzará a representar la secuencia.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Elemento STARTMARKER Media Player Windows
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700116"
---
# <a name="startmarker-element"></a><span data-ttu-id="77670-104">Elemento STARTMARKER</span><span class="sxs-lookup"><span data-stu-id="77670-104">STARTMARKER Element</span></span>

<span data-ttu-id="77670-105">El elemento **STARTMARKER** especifica un marcador desde el que Windows Media Player comenzará a representar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="77670-105">The **STARTMARKER** element specifies a marker from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="77670-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="77670-106">Attributes</span></span>

<span data-ttu-id="77670-107">**NÚMEROS**</span><span class="sxs-lookup"><span data-stu-id="77670-107">**NUMBER**</span></span>

<span data-ttu-id="77670-108">El número de un marcador numérico en el índice.</span><span class="sxs-lookup"><span data-stu-id="77670-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="77670-109">El valor predeterminado es el principio del contenido a petición o la posición actual en un flujo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="77670-109">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

<span data-ttu-id="77670-110">**NOMBRE**</span><span class="sxs-lookup"><span data-stu-id="77670-110">**NAME**</span></span>

<span data-ttu-id="77670-111">Nombre de un marcador con nombre en el índice.</span><span class="sxs-lookup"><span data-stu-id="77670-111">The name of a named marker in the index.</span></span> <span data-ttu-id="77670-112">El valor predeterminado es el principio del contenido a petición o la posición actual en un flujo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="77670-112">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="77670-113">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="77670-113">Parent/Child Elements</span></span>



| <span data-ttu-id="77670-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="77670-114">Hierarchy</span></span>       | <span data-ttu-id="77670-115">Elementos</span><span class="sxs-lookup"><span data-stu-id="77670-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="77670-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="77670-116">Parent elements</span></span> | <span data-ttu-id="77670-117">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="77670-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="77670-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="77670-118">Child elements</span></span>  | <span data-ttu-id="77670-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="77670-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="77670-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77670-120">Remarks</span></span>

<span data-ttu-id="77670-121">Este elemento especifica el marcador desde el que Windows Media Player va a comenzar a representar la secuencia definida en el elemento primario **entry** o **ref** .</span><span class="sxs-lookup"><span data-stu-id="77670-121">This element specifies the marker from which Windows Media Player is to start rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="77670-122">**Note**</span><span class="sxs-lookup"><span data-stu-id="77670-122">**Note**</span></span>

<span data-ttu-id="77670-123">Use este elemento con el atributo **número** o **nombre** , pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="77670-123">Use this element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="77670-124">Un elemento **STARTMARKER** definido dentro de un elemento **ref** tiene prioridad sobre un elemento **STARTMARKER** definido en el elemento de **entrada** primario del elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="77670-124">A **STARTMARKER** element defined within a **REF** element takes precedence over a **STARTMARKER** element defined within the **REF** element's parent **ENTRY** element.</span></span> <span data-ttu-id="77670-125">Un elemento **STARTMARKER** también tiene prioridad sobre un elemento **STARTTIME** .</span><span class="sxs-lookup"><span data-stu-id="77670-125">A **STARTMARKER** element also takes precedence over a **STARTTIME** element.</span></span>

<span data-ttu-id="77670-126">Si el marcador especificado por un elemento **STARTMARKER** se produce posteriormente en la secuencia que el marcador definido por un elemento **ENDMARKER** , no se reproduce ningún contenido, pero no se genera ningún error.</span><span class="sxs-lookup"><span data-stu-id="77670-126">If the marker specified by a **STARTMARKER** element occurs later in the stream than the marker defined by an **ENDMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="77670-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="77670-127">Examples</span></span>


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a><span data-ttu-id="77670-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77670-128">Requirements</span></span>



| <span data-ttu-id="77670-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="77670-129">Requirement</span></span> | <span data-ttu-id="77670-130">Value</span><span class="sxs-lookup"><span data-stu-id="77670-130">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="77670-131">Versión</span><span class="sxs-lookup"><span data-stu-id="77670-131">Version</span></span><br/> | <span data-ttu-id="77670-132">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="77670-132">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77670-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="77670-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77670-134">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="77670-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="77670-135">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="77670-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





