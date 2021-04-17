---
description: Representa el tipo de origen del marco.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696759"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a><span data-ttu-id="fc7e7-103">Atributo MF \_ DEVICESTREAM \_ atributo \_ FRAMESOURCE \_ Types</span><span class="sxs-lookup"><span data-stu-id="fc7e7-103">MF\_DEVICESTREAM\_ATTRIBUTE\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="fc7e7-104">Representa el tipo de origen del marco.</span><span class="sxs-lookup"><span data-stu-id="fc7e7-104">Represents the frame source type.</span></span>

## <a name="data-type"></a><span data-ttu-id="fc7e7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fc7e7-105">Data type</span></span>

<span data-ttu-id="fc7e7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fc7e7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fc7e7-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc7e7-107">Remarks</span></span>

<span data-ttu-id="fc7e7-108">Este valor de este atributo debe ser una máscara de máscara de uno o más valores de la enumeración [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) .</span><span class="sxs-lookup"><span data-stu-id="fc7e7-108">This value of this attribute should be a bitmask of one or more values from the [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) enumeration.</span></span> <span data-ttu-id="fc7e7-109">Para admitir la compatibilidad con versiones anteriores, cuando este atributo no está definido para un tipo de medio, se supone que tiene el valor **MFFrameSourceTypes:: color**.</span><span class="sxs-lookup"><span data-stu-id="fc7e7-109">To support backward compatibility, when this attribute is not defined for a media type, it is assumed to have the value **MFFrameSourceTypes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc7e7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc7e7-110">Requirements</span></span>



| <span data-ttu-id="fc7e7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc7e7-111">Requirement</span></span> | <span data-ttu-id="fc7e7-112">Value</span><span class="sxs-lookup"><span data-stu-id="fc7e7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7e7-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc7e7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7e7-114">Solo aplicaciones de escritorio de Windows 10, versión 1607 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc7e7-114">Windows 10, version 1607 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fc7e7-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc7e7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7e7-116">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc7e7-116">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc7e7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc7e7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc7e7-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc7e7-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




