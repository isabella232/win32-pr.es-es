---
title: Elemento PREVIEWDURATION
description: El elemento PREVIEWDURATION define la cantidad de tiempo que se reproduce un clip en el modo de vista previa.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Elemento PREVIEWDURATION Media Player Windows
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708283"
---
# <a name="previewduration-element"></a><span data-ttu-id="e737c-104">Elemento PREVIEWDURATION</span><span class="sxs-lookup"><span data-stu-id="e737c-104">PREVIEWDURATION Element</span></span>

<span data-ttu-id="e737c-105">El elemento **PREVIEWDURATION** define la cantidad de tiempo que se reproduce un clip en el modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="e737c-105">The **PREVIEWDURATION** element defines the length of time a clip plays in preview mode.</span></span>

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="e737c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e737c-106">Attributes</span></span>

<span data-ttu-id="e737c-107">**Valor** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="e737c-107">**VALUE** (required)</span></span>

<span data-ttu-id="e737c-108">Período de tiempo (en horas, minutos, segundos y centésimas de segundo) que el clip reproduce en el modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="e737c-108">Length of time (in hours, minutes, seconds, and hundredths of a second) that the clip plays in preview mode.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="e737c-109">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="e737c-109">Parent/Child Elements</span></span>



| <span data-ttu-id="e737c-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e737c-110">Hierarchy</span></span>       | <span data-ttu-id="e737c-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="e737c-111">Elements</span></span>                    |
|-----------------|-----------------------------|
| <span data-ttu-id="e737c-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e737c-112">Parent elements</span></span> | <span data-ttu-id="e737c-113">**ASX**, **entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="e737c-113">**ASX**, **ENTRY**, **REF**</span></span> |
| <span data-ttu-id="e737c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e737c-114">Child elements</span></span>  | <span data-ttu-id="e737c-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e737c-115">None</span></span>                        |



 

## <a name="remarks"></a><span data-ttu-id="e737c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e737c-116">Remarks</span></span>

<span data-ttu-id="e737c-117">Este elemento define el período de tiempo que un clip se reproduce en el modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="e737c-117">This element defines the length of time that a clip plays in preview mode.</span></span> <span data-ttu-id="e737c-118">Si este elemento aparece dentro de un elemento **entry** o **ref** , se aplica al clip definido por ese elemento.</span><span class="sxs-lookup"><span data-stu-id="e737c-118">If this element appears within an **ENTRY** element or a **REF** element, it applies to the clip defined by that element.</span></span> <span data-ttu-id="e737c-119">Si aparece dentro del ámbito de un elemento **ASX** , se aplica a todos los clips del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="e737c-119">If it appears within the scope of an **ASX** element, it applies to every clip in the metafile.</span></span> <span data-ttu-id="e737c-120">Un elemento **PREVIEWDURATION** de un elemento **ref** tiene prioridad sobre uno en un **elemento** entry y tiene prioridad sobre un elemento **PREVIEWDURATION** en un elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="e737c-120">A **PREVIEWDURATION** element in a **REF** element takes precedence over one in an ENTRY **element**, and either takes precedence over a **PREVIEWDURATION** element in an **ASX** element.</span></span> <span data-ttu-id="e737c-121">Si no se define ningún elemento **PREVIEWDURATION** para un clip, la hora de la vista previa predeterminada es de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="e737c-121">If no **PREVIEWDURATION** element is defined for a clip, the default preview time is 10 seconds.</span></span>

<span data-ttu-id="e737c-122">Si hay un elemento **STARTTIME** o **STARTMARKER** para el clip, Windows Media Player representa el clip comenzando en el punto definido por uno de estos elementos. en caso contrario, se representa desde el principio del clip.</span><span class="sxs-lookup"><span data-stu-id="e737c-122">If there is a **STARTTIME** or **STARTMARKER** element for the clip, Windows Media Player renders the clip starting at the point defined by one of these elements; otherwise it renders from the beginning of the clip.</span></span> <span data-ttu-id="e737c-123">El clip se detiene normalmente si es menor que el tiempo definido por el elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="e737c-123">The clip stops normally if it is shorter than the time defined by the **PREVIEWDURATION** element.</span></span>

<span data-ttu-id="e737c-124">El elemento **Duration** invalida un elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="e737c-124">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="e737c-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e737c-125">Examples</span></span>


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="e737c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e737c-126">Requirements</span></span>



| <span data-ttu-id="e737c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e737c-127">Requirement</span></span> | <span data-ttu-id="e737c-128">Value</span><span class="sxs-lookup"><span data-stu-id="e737c-128">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="e737c-129">Versión</span><span class="sxs-lookup"><span data-stu-id="e737c-129">Version</span></span><br/> | <span data-ttu-id="e737c-130">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="e737c-130">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e737c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e737c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e737c-132">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e737c-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e737c-133">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e737c-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





