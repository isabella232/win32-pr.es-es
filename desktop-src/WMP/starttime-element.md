---
title: STARTTIME (elemento)
description: El elemento STARTTIME define un índice de tiempo desde el que Windows Media Player comenzará a representar la secuencia.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTTIME Media Player Windows
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699468"
---
# <a name="starttime-element"></a><span data-ttu-id="e028a-104">STARTTIME (elemento)</span><span class="sxs-lookup"><span data-stu-id="e028a-104">STARTTIME Element</span></span>

<span data-ttu-id="e028a-105">El elemento **STARTTIME** define un índice de tiempo desde el que Windows Media Player comenzará a representar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e028a-105">The **STARTTIME** element defines a time index from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="e028a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e028a-106">Attributes</span></span>

<span data-ttu-id="e028a-107">**Valor** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="e028a-107">**VALUE** (required)</span></span>

<span data-ttu-id="e028a-108">El índice de tiempo (en horas, minutos, segundos y centésimas de segundo) desde el que Windows Media Player comienza a reproducir un flujo definido en el elemento asociado.</span><span class="sxs-lookup"><span data-stu-id="e028a-108">The time index (in hours, minutes, seconds, and hundredths of a second) from which Windows Media Player starts playing a stream defined in the associated element.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="e028a-109">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="e028a-109">Parent/Child Elements</span></span>



| <span data-ttu-id="e028a-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e028a-110">Hierarchy</span></span>       | <span data-ttu-id="e028a-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="e028a-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="e028a-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e028a-112">Parent elements</span></span> | <span data-ttu-id="e028a-113">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="e028a-113">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="e028a-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e028a-114">Child elements</span></span>  | <span data-ttu-id="e028a-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e028a-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="e028a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e028a-116">Remarks</span></span>

<span data-ttu-id="e028a-117">Este elemento define un índice de tiempo en el contenido donde Windows Media Player va a comenzar a representar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e028a-117">This element defines a time index into the content where Windows Media Player is to start rendering the stream.</span></span> <span data-ttu-id="e028a-118">Este elemento solo se puede usar con contenido almacenado a petición que se ha indexado.</span><span class="sxs-lookup"><span data-stu-id="e028a-118">This element can be used only with stored, on-demand content that has been indexed.</span></span>

## <a name="examples"></a><span data-ttu-id="e028a-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e028a-119">Examples</span></span>


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="e028a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e028a-120">Requirements</span></span>



| <span data-ttu-id="e028a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e028a-121">Requirement</span></span> | <span data-ttu-id="e028a-122">Value</span><span class="sxs-lookup"><span data-stu-id="e028a-122">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="e028a-123">Versión</span><span class="sxs-lookup"><span data-stu-id="e028a-123">Version</span></span><br/> | <span data-ttu-id="e028a-124">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="e028a-124">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e028a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e028a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e028a-126">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e028a-126">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e028a-127">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e028a-127">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





