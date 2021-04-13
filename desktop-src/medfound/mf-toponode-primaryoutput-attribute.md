---
description: Indica qué salida es la salida principal en un nodo tee.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: MF_TOPONODE_PRIMARYOUTPUT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360432"
---
# <a name="mf_toponode_primaryoutput-attribute"></a><span data-ttu-id="5961b-103">\_ \_ Atributo PRIMARYOUTPUT de MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="5961b-103">MF\_TOPONODE\_PRIMARYOUTPUT attribute</span></span>

<span data-ttu-id="5961b-104">Indica qué salida es la salida principal en un nodo tee.</span><span class="sxs-lookup"><span data-stu-id="5961b-104">Indicates which output is the primary output on a tee node.</span></span>

## <a name="data-type"></a><span data-ttu-id="5961b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5961b-105">Data type</span></span>

<span data-ttu-id="5961b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5961b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5961b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5961b-107">Remarks</span></span>

<span data-ttu-id="5961b-108">Este atributo se aplica a los nodos Tee (nodo de la **\_ topología MF \_ Tee \_**).</span><span class="sxs-lookup"><span data-stu-id="5961b-108">This attribute applies to tee nodes (**MF\_TOPOLOGY\_TEE\_NODE**).</span></span>

<span data-ttu-id="5961b-109">El valor de este atributo es el índice de base cero de una conexión de salida en este nodo tee.</span><span class="sxs-lookup"><span data-stu-id="5961b-109">The value of this attribute is the zero-based index of an output connection on this tee node.</span></span> <span data-ttu-id="5961b-110">Este valor indica qué salida es el flujo de salida principal.</span><span class="sxs-lookup"><span data-stu-id="5961b-110">This value indicates which output is the primary output stream.</span></span> <span data-ttu-id="5961b-111">La canalización espera una solicitud de la salida principal antes de procesar las solicitudes de las demás salidas.</span><span class="sxs-lookup"><span data-stu-id="5961b-111">The pipeline waits for a request from the primary output before processing requests from the other outputs.</span></span>

<span data-ttu-id="5961b-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5961b-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5961b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5961b-113">Requirements</span></span>



| <span data-ttu-id="5961b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5961b-114">Requirement</span></span> | <span data-ttu-id="5961b-115">Value</span><span class="sxs-lookup"><span data-stu-id="5961b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5961b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5961b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5961b-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5961b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5961b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5961b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5961b-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5961b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5961b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5961b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5961b-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5961b-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5961b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5961b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5961b-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5961b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5961b-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5961b-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5961b-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5961b-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5961b-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="5961b-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="5961b-127">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="5961b-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




