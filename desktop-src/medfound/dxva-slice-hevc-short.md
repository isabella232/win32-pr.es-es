---
description: Especifica los datos de control de sector.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: DXVA_Slice_HEVC_Short estructura (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080315"
---
# <a name="dxva_slice_hevc_short-structure"></a><span data-ttu-id="bf765-103">\_Estructura corta del segmento de DXVA \_ HEVC \_</span><span class="sxs-lookup"><span data-stu-id="bf765-103">DXVA\_Slice\_HEVC\_Short structure</span></span>

<span data-ttu-id="bf765-104">Especifica los datos de control de sector.</span><span class="sxs-lookup"><span data-stu-id="bf765-104">Specifies slice control data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf765-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf765-105">Syntax</span></span>


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a><span data-ttu-id="bf765-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf765-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf765-107">**BSNALunitDataLocation**</span><span class="sxs-lookup"><span data-stu-id="bf765-107">**BSNALunitDataLocation**</span></span>
</dt> <dd>

<span data-ttu-id="bf765-108">Especifica la ubicación de la unidad NAL.</span><span class="sxs-lookup"><span data-stu-id="bf765-108">Specifies the location of the NAL unit.</span></span>

</dd> <dt>

<span data-ttu-id="bf765-109">**SliceBytesInBuffer**</span><span class="sxs-lookup"><span data-stu-id="bf765-109">**SliceBytesInBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="bf765-110">El número de bytes del búfer de datos fragmentada que están asociados a esta estructura de datos del control de segmento.</span><span class="sxs-lookup"><span data-stu-id="bf765-110">The number of bytes in the bitstream data buffer that are associated with this slice control data structure.</span></span>

</dd> <dt>

<span data-ttu-id="bf765-111">**wBadSliceChopping**</span><span class="sxs-lookup"><span data-stu-id="bf765-111">**wBadSliceChopping**</span></span>
</dt> <dd>

<span data-ttu-id="bf765-112">Si se usa el análisis de fragmentada fuera del host, este valor indica el segmento incorrecto cortar y contiene uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="bf765-112">If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:</span></span>



| <span data-ttu-id="bf765-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf765-113">Requirement</span></span> | <span data-ttu-id="bf765-114">Value</span><span class="sxs-lookup"><span data-stu-id="bf765-114">Value</span></span> |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf765-115">Value</span><span class="sxs-lookup"><span data-stu-id="bf765-115">Value</span></span> | <span data-ttu-id="bf765-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf765-116">Description</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="bf765-117">0</span><span class="sxs-lookup"><span data-stu-id="bf765-117">0</span></span>     | <span data-ttu-id="bf765-118">Todos los bits del segmento se encuentran en el búfer de datos de fragmentada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bf765-118">All bits for the slice are located within the corresponding bitstream data buffer.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="bf765-119">1</span><span class="sxs-lookup"><span data-stu-id="bf765-119">1</span></span>     | <span data-ttu-id="bf765-120">El búfer de datos fragmentada contiene el inicio del segmento, pero no el segmento completo, porque el búfer está lleno.</span><span class="sxs-lookup"><span data-stu-id="bf765-120">The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full.</span></span>                                                                                                                                        |
| <span data-ttu-id="bf765-121">2</span><span class="sxs-lookup"><span data-stu-id="bf765-121">2</span></span>     | <span data-ttu-id="bf765-122">El búfer de datos fragmentada contiene el final del segmento.</span><span class="sxs-lookup"><span data-stu-id="bf765-122">The bitstream data buffer contains the end of the slice.</span></span> <span data-ttu-id="bf765-123">No contiene el inicio del segmento, porque el inicio del segmento se encontraba en el búfer de datos fragmentada anterior.</span><span class="sxs-lookup"><span data-stu-id="bf765-123">It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer.</span></span>                                                                  |
| <span data-ttu-id="bf765-124">3</span><span class="sxs-lookup"><span data-stu-id="bf765-124">3</span></span>     | <span data-ttu-id="bf765-125">El búfer de datos fragmentada no contiene el inicio del segmento porque el inicio del segmento se encontraba en el búfer de datos fragmentada anterior y no contiene el final del segmento porque el búfer de datos fragmentada actual también está lleno.</span><span class="sxs-lookup"><span data-stu-id="bf765-125">The bitstream data buffer does not contain the start of the slice because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf765-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf765-126">Remarks</span></span>

<span data-ttu-id="bf765-127">**DXVA \_ El segmento \_ HEVC \_ Short** contiene datos de control de segmento que se pasan al Acelerador de hardware desde el descodificador de software del host.</span><span class="sxs-lookup"><span data-stu-id="bf765-127">**DXVA\_Slice\_HEVC\_Short** contains slice control data which is passed to the hardware accelerator from the host software decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf765-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf765-128">Requirements</span></span>



| <span data-ttu-id="bf765-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf765-129">Requirement</span></span> | <span data-ttu-id="bf765-130">Value</span><span class="sxs-lookup"><span data-stu-id="bf765-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bf765-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf765-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bf765-132">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="bf765-132">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bf765-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf765-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bf765-134">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf765-134">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bf765-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf765-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf765-136"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf765-136"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf765-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf765-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf765-138">Media Foundation estructuras</span><span class="sxs-lookup"><span data-stu-id="bf765-138">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




