---
title: Elemento ENDMARKER
description: El elemento ENDMARKER especifica un marcador en el que Windows Media Player detendrá la representación de la secuencia.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Elemento ENDMARKER Media Player Windows
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700324"
---
# <a name="endmarker-element"></a><span data-ttu-id="b703a-104">Elemento ENDMARKER</span><span class="sxs-lookup"><span data-stu-id="b703a-104">ENDMARKER Element</span></span>

<span data-ttu-id="b703a-105">El elemento **ENDMARKER** especifica un marcador en el que Windows Media Player detendrá la representación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b703a-105">The **ENDMARKER** element specifies a marker at which Windows Media Player will stop rendering the stream.</span></span>

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="b703a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b703a-106">Attributes</span></span>

<span data-ttu-id="b703a-107">**NÚMEROS**</span><span class="sxs-lookup"><span data-stu-id="b703a-107">**NUMBER**</span></span>

<span data-ttu-id="b703a-108">El número de un marcador numérico en el índice.</span><span class="sxs-lookup"><span data-stu-id="b703a-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="b703a-109">El valor predeterminado es el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="b703a-109">The default value is the end of the content.</span></span>

<span data-ttu-id="b703a-110">**NOMBRE**</span><span class="sxs-lookup"><span data-stu-id="b703a-110">**NAME**</span></span>

<span data-ttu-id="b703a-111">Nombre de un marcador con nombre en el índice.</span><span class="sxs-lookup"><span data-stu-id="b703a-111">The name of a named marker in the index.</span></span> <span data-ttu-id="b703a-112">El valor predeterminado es el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="b703a-112">The default value is the end of the content.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b703a-113">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="b703a-113">Parent/Child Elements</span></span>



| <span data-ttu-id="b703a-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b703a-114">Hierarchy</span></span>       | <span data-ttu-id="b703a-115">Elementos</span><span class="sxs-lookup"><span data-stu-id="b703a-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="b703a-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b703a-116">Parent elements</span></span> | <span data-ttu-id="b703a-117">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="b703a-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="b703a-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b703a-118">Child elements</span></span>  | <span data-ttu-id="b703a-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b703a-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="b703a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b703a-120">Remarks</span></span>

<span data-ttu-id="b703a-121">Este elemento especifica el marcador donde Windows Media Player va a detener la representación de la secuencia definida en el elemento primario **entry** o **ref** .</span><span class="sxs-lookup"><span data-stu-id="b703a-121">This element specifies the marker where Windows Media Player is to stop rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="b703a-122">Nota</span><span class="sxs-lookup"><span data-stu-id="b703a-122">Note</span></span>

<span data-ttu-id="b703a-123">Use el elemento **ENDMARKER** con el atributo **número** o **nombre** , pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="b703a-123">Use the **ENDMARKER** element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="b703a-124">En el modo de vista previa, al alcanzar un marcador final se detiene la vista previa, incluso si no ha transcurrido el tiempo especificado por el elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="b703a-124">In preview mode, reaching an end marker stops the preview, even if the time specified by the **PREVIEWDURATION** element has not elapsed.</span></span> <span data-ttu-id="b703a-125">El elemento **ENDMARKER** también tiene prioridad sobre el elemento **Duration** .</span><span class="sxs-lookup"><span data-stu-id="b703a-125">The **ENDMARKER** element also takes precedence over the **DURATION** element.</span></span>

<span data-ttu-id="b703a-126">Un elemento **ENDMARKER** definido dentro de un elemento **ref** tiene prioridad sobre un **ENDMARKER** definido en el elemento de **entrada** primario del elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="b703a-126">An **ENDMARKER** element defined within a **REF** element takes precedence over an **ENDMARKER** defined within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="b703a-127">Si el marcador especificado por un elemento **ENDMARKER** se produce antes en el flujo que el marcador definido por un elemento **STARTMARKER** , no se reproduce ningún contenido, pero no se genera ningún error.</span><span class="sxs-lookup"><span data-stu-id="b703a-127">If the marker specified by an **ENDMARKER** element occurs earlier in the stream than the marker defined by a **STARTMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="b703a-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b703a-128">Examples</span></span>


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

```



## <a name="requirements"></a><span data-ttu-id="b703a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b703a-129">Requirements</span></span>



| <span data-ttu-id="b703a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b703a-130">Requirement</span></span> | <span data-ttu-id="b703a-131">Value</span><span class="sxs-lookup"><span data-stu-id="b703a-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b703a-132">Versión</span><span class="sxs-lookup"><span data-stu-id="b703a-132">Version</span></span><br/> | <span data-ttu-id="b703a-133">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="b703a-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b703a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b703a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b703a-135">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b703a-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b703a-136">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b703a-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





