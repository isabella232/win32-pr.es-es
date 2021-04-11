---
description: Especifica el tipo de unidad contenido en una IMFSample de una colección de MFSampleExtension \_ ForwardedDecodeUnits.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: Enumeración MF_CUSTOM_DECODE_UNIT_TYPE (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275959"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a><span data-ttu-id="dac29-103">\_ \_ \_ Enumeración de tipo de unidad de DEScodificación personalizada MF \_</span><span class="sxs-lookup"><span data-stu-id="dac29-103">MF\_CUSTOM\_DECODE\_UNIT\_TYPE enumeration</span></span>

<span data-ttu-id="dac29-104">Especifica el tipo de unidad contenido en una [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de una colección de [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) .</span><span class="sxs-lookup"><span data-stu-id="dac29-104">Specifies the type of unit contained in an [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in a [MFSampleExtension\_ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) collection.</span></span>

## <a name="members"></a><span data-ttu-id="dac29-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="dac29-105">Members</span></span>



| <span data-ttu-id="dac29-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="dac29-106">Member</span></span>                    | <span data-ttu-id="dac29-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac29-107">Description</span></span>                                                             | <span data-ttu-id="dac29-108">Value</span><span class="sxs-lookup"><span data-stu-id="dac29-108">Value</span></span> |
|---------------------------|-------------------------------------------------------------------------|-------|
| <span data-ttu-id="dac29-109">**\_unidad de DEScodificación de MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dac29-109">**MF\_DECODE\_UNIT\_NAL**</span></span> | <span data-ttu-id="dac29-110">El tipo de unidad es unidad de capa de abstracción de red (NALU).</span><span class="sxs-lookup"><span data-stu-id="dac29-110">The unit type is network abstraction layer unit (NALU).</span></span> <br/>     | <span data-ttu-id="dac29-111">0</span><span class="sxs-lookup"><span data-stu-id="dac29-111">0</span></span>     |
| <span data-ttu-id="dac29-112">**\_Sei de unidad de descodificación MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dac29-112">**MF\_DECODE\_UNIT\_SEI**</span></span> | <span data-ttu-id="dac29-113">El tipo de unidad es información de mejora complementaria (SEI).</span><span class="sxs-lookup"><span data-stu-id="dac29-113">The unit type is Supplemental Enhancement Information (SEI).</span></span><br/> | <span data-ttu-id="dac29-114">1</span><span class="sxs-lookup"><span data-stu-id="dac29-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="dac29-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dac29-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dac29-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac29-116">Requirements</span></span>



| <span data-ttu-id="dac29-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac29-117">Requirement</span></span> | <span data-ttu-id="dac29-118">Value</span><span class="sxs-lookup"><span data-stu-id="dac29-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dac29-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dac29-120">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac29-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dac29-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dac29-122">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac29-122">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dac29-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dac29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac29-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-124"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




