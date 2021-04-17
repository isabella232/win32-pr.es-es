---
description: Identifica el nodo de la topología para un receptor de flujo.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: MF_EVENT_OUTPUT_NODE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659858"
---
# <a name="mf_event_output_node-attribute"></a><span data-ttu-id="91b3c-103">\_Atributo de \_ nodo de salida de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="91b3c-103">MF\_EVENT\_OUTPUT\_NODE attribute</span></span>

<span data-ttu-id="91b3c-104">Identifica el nodo de la topología para un receptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="91b3c-104">Identifies the topology node for a stream sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="91b3c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="91b3c-105">Data type</span></span>

<span data-ttu-id="91b3c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="91b3c-106">**UINT64**</span></span>

<span data-ttu-id="91b3c-107">Tratar como [**TOPOID**](topoid.md).</span><span class="sxs-lookup"><span data-stu-id="91b3c-107">Treat as [**TOPOID**](topoid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91b3c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91b3c-108">Remarks</span></span>

<span data-ttu-id="91b3c-109">El valor de este atributo es un identificador de nodo para un nodo de salida en la topología actual.</span><span class="sxs-lookup"><span data-stu-id="91b3c-109">The value of this attribute is a node identifier for an output node on the current topology.</span></span> <span data-ttu-id="91b3c-110">Para obtener un puntero al nodo asociado, llame a [**IMFTopology:: GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) en la topología.</span><span class="sxs-lookup"><span data-stu-id="91b3c-110">To get a pointer to the associated node, call [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) on the topology.</span></span>

<span data-ttu-id="91b3c-111">Este atributo se utiliza con los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="91b3c-111">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="91b3c-112">MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="91b3c-112">MESessionStreamSinkFormatChanged</span></span>](mesessionstreamsinkformatchanged.md)
-   [<span data-ttu-id="91b3c-113">MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="91b3c-113">MESinkInvalidated</span></span>](mesinkinvalidated.md)

<span data-ttu-id="91b3c-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="91b3c-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91b3c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91b3c-115">Requirements</span></span>



| <span data-ttu-id="91b3c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="91b3c-116">Requirement</span></span> | <span data-ttu-id="91b3c-117">Value</span><span class="sxs-lookup"><span data-stu-id="91b3c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91b3c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91b3c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91b3c-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91b3c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="91b3c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91b3c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91b3c-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="91b3c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91b3c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91b3c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91b3c-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="91b3c-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b3c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="91b3c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b3c-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91b3c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91b3c-126">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="91b3c-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="91b3c-127">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="91b3c-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="91b3c-128">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="91b3c-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




