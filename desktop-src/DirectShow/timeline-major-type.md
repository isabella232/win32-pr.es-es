---
description: La \_ \_ enumeración de tipo principal de la escala de tiempo especifica el tipo principal de un objeto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Enumeración TIMELINE_MAJOR_TYPE (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690097"
---
# <a name="timeline_major_type-enumeration"></a><span data-ttu-id="99377-103">\_Enumeración de tipo principal de escala de tiempo \_</span><span class="sxs-lookup"><span data-stu-id="99377-103">TIMELINE\_MAJOR\_TYPE enumeration</span></span>

> [!Note]  
> <span data-ttu-id="99377-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="99377-104">\[Deprecated.</span></span> <span data-ttu-id="99377-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99377-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="99377-106">La `TIMELINE_MAJOR_TYPE` enumeración especifica el tipo principal de un objeto.</span><span class="sxs-lookup"><span data-stu-id="99377-106">The `TIMELINE_MAJOR_TYPE` enumeration specifies the major type of an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="99377-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99377-107">Syntax</span></span>


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="99377-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="99377-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="99377-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**tipo principal de escala de tiempo \_ \_ \_ compuesto**</span><span class="sxs-lookup"><span data-stu-id="99377-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE\_MAJOR\_TYPE\_COMPOSITE**</span></span>
</dt> <dd>

<span data-ttu-id="99377-110">Objeto compuesto.</span><span class="sxs-lookup"><span data-stu-id="99377-110">Composite object.</span></span> <span data-ttu-id="99377-111">Contiene una o más pistas.</span><span class="sxs-lookup"><span data-stu-id="99377-111">Holds one or more tracks.</span></span>

</dd> <dt>

<span data-ttu-id="99377-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_pista de \_ tipo \_ principal de escala de tiempo**</span><span class="sxs-lookup"><span data-stu-id="99377-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TIMELINE\_MAJOR\_TYPE\_TRACK**</span></span>
</dt> <dd>

<span data-ttu-id="99377-113">Objeto Track.</span><span class="sxs-lookup"><span data-stu-id="99377-113">Track object.</span></span> <span data-ttu-id="99377-114">Contiene uno o más orígenes.</span><span class="sxs-lookup"><span data-stu-id="99377-114">Holds one or more sources.</span></span>

</dd> <dt>

<span data-ttu-id="99377-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_origen de \_ tipo \_ principal de la escala de tiempo**</span><span class="sxs-lookup"><span data-stu-id="99377-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**TIMELINE\_MAJOR\_TYPE\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="99377-116">Objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="99377-116">Source object.</span></span> <span data-ttu-id="99377-117">Contiene una referencia a un origen de multimedia.</span><span class="sxs-lookup"><span data-stu-id="99377-117">Contains a reference to a media source.</span></span>

</dd> <dt>

<span data-ttu-id="99377-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_transición de \_ tipo \_ principal de escala de tiempo**</span><span class="sxs-lookup"><span data-stu-id="99377-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TIMELINE\_MAJOR\_TYPE\_TRANSITION**</span></span>
</dt> <dd>

<span data-ttu-id="99377-119">Objeto de transición.</span><span class="sxs-lookup"><span data-stu-id="99377-119">Transition object.</span></span> <span data-ttu-id="99377-120">Define una transición entre compuestos, pistas o orígenes.</span><span class="sxs-lookup"><span data-stu-id="99377-120">Defines a transition between composites, tracks, or sources.</span></span>

</dd> <dt>

<span data-ttu-id="99377-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_efecto de \_ tipo \_ principal de la escala de tiempo**</span><span class="sxs-lookup"><span data-stu-id="99377-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**TIMELINE\_MAJOR\_TYPE\_EFFECT**</span></span>
</dt> <dd>

<span data-ttu-id="99377-122">Objeto de efecto.</span><span class="sxs-lookup"><span data-stu-id="99377-122">Effect object.</span></span> <span data-ttu-id="99377-123">Define un efecto de entrada única que se va a aplicar a un objeto compuesto, de seguimiento o de origen.</span><span class="sxs-lookup"><span data-stu-id="99377-123">Defines a single-input effect to be applied to a composite, track, or source object.</span></span>

</dd> <dt>

<span data-ttu-id="99377-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**Grupo de tipo de escala de tiempo \_ principal \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99377-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**TIMELINE\_MAJOR\_TYPE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="99377-125">Objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="99377-125">Group object.</span></span> <span data-ttu-id="99377-126">Contiene una o más pistas de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="99377-126">Contains one or more tracks of a given type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99377-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99377-127">Requirements</span></span>



| <span data-ttu-id="99377-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="99377-128">Requirement</span></span> | <span data-ttu-id="99377-129">Value</span><span class="sxs-lookup"><span data-stu-id="99377-129">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99377-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99377-130">Header</span></span><br/> | <dl> <span data-ttu-id="99377-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="99377-131"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99377-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="99377-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99377-133">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="99377-133">**IAMTimeline**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="99377-134">**IAMTimelineComp::GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="99377-134">**IAMTimelineComp::GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[<span data-ttu-id="99377-135">**IAMTimelineObj::GetTimelineType**</span><span class="sxs-lookup"><span data-stu-id="99377-135">**IAMTimelineObj::GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




