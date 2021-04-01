---
description: Especifica el estado de un intento de resolver una topología.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: MF_TOPOLOGY_RESOLUTION_STATUS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908455"
---
# <a name="mf_topology_resolution_status-attribute"></a><span data-ttu-id="8ed2b-103">Atributo de estado de resolución de \_ topología MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ed2b-103">MF\_TOPOLOGY\_RESOLUTION\_STATUS attribute</span></span>

<span data-ttu-id="8ed2b-104">Especifica el estado de un intento de resolver una topología.</span><span class="sxs-lookup"><span data-stu-id="8ed2b-104">Specifies the status of an attempt to resolve a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="8ed2b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8ed2b-105">Data type</span></span>

<span data-ttu-id="8ed2b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8ed2b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed2b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ed2b-107">Remarks</span></span>

<span data-ttu-id="8ed2b-108">El cargador de topologías o la sesión multimedia podrían establecer este atributo en una topología.</span><span class="sxs-lookup"><span data-stu-id="8ed2b-108">The topology loader or the Media Session might set this attribute on a topology.</span></span> <span data-ttu-id="8ed2b-109">El valor de este atributo es **una operación OR** bit a bit de marcas de la enumeración de [**marcas de estado de \_ resolución de topología \_ \_ \_ MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .</span><span class="sxs-lookup"><span data-stu-id="8ed2b-109">The value of this attribute is a bitwise **OR** of flags from the [**MF\_TOPOLOGY\_RESOLUTION\_STATUS\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) enumeration.</span></span>

<span data-ttu-id="8ed2b-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8ed2b-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed2b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ed2b-111">Requirements</span></span>



| <span data-ttu-id="8ed2b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed2b-112">Requirement</span></span> | <span data-ttu-id="8ed2b-113">Value</span><span class="sxs-lookup"><span data-stu-id="8ed2b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed2b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ed2b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed2b-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8ed2b-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ed2b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ed2b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed2b-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ed2b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ed2b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ed2b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ed2b-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed2b-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ed2b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ed2b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed2b-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ed2b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ed2b-122">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8ed2b-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8ed2b-123">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8ed2b-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8ed2b-124">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="8ed2b-124">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="8ed2b-125">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="8ed2b-125">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




