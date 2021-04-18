---
description: Especifica cuándo se purga una transformación.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: MF_TOPONODE_DRAIN atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715390"
---
# <a name="mf_toponode_drain-attribute"></a><span data-ttu-id="7d390-103">\_Atributo de \_ purga MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="7d390-103">MF\_TOPONODE\_DRAIN attribute</span></span>

<span data-ttu-id="7d390-104">Especifica cuándo se purga una transformación.</span><span class="sxs-lookup"><span data-stu-id="7d390-104">Specifies when a transform is drained.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d390-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7d390-105">Data type</span></span>

<span data-ttu-id="7d390-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7d390-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7d390-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d390-107">Remarks</span></span>

<span data-ttu-id="7d390-108">Este atributo se aplica a los nodos de transformación (**\_ nodo de \_ transformación \_ de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="7d390-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="7d390-109">El valor del atributo es un miembro de la enumeración del [**\_ modo de \_ purga \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) .</span><span class="sxs-lookup"><span data-stu-id="7d390-109">The value of the attribute is a member of the [**MF\_TOPONODE\_DRAIN\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) enumeration.</span></span> <span data-ttu-id="7d390-110">Si no se establece este atributo, el valor predeterminado es **MF \_ TOPONODE \_ \_ valor predeterminado de Drain**.</span><span class="sxs-lookup"><span data-stu-id="7d390-110">If this attribute is not set, the default value is **MF\_TOPONODE\_DRAIN\_DEFAULT**.</span></span>

<span data-ttu-id="7d390-111">La purga se realiza mediante una llamada a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) en la transformación con el mensaje de [**\_ agotamiento del \_ comando \_ de mensaje MFT**](mft-message-command-drain.md) .</span><span class="sxs-lookup"><span data-stu-id="7d390-111">Draining is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span> <span data-ttu-id="7d390-112">Para obtener más información, consulte enumeración de [**\_ \_ tipo de mensaje de MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .</span><span class="sxs-lookup"><span data-stu-id="7d390-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="7d390-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7d390-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d390-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d390-114">Requirements</span></span>



| <span data-ttu-id="7d390-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d390-115">Requirement</span></span> | <span data-ttu-id="7d390-116">Value</span><span class="sxs-lookup"><span data-stu-id="7d390-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d390-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d390-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d390-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7d390-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7d390-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d390-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d390-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d390-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7d390-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d390-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d390-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d390-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d390-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d390-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d390-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7d390-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d390-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7d390-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7d390-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7d390-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7d390-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="7d390-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="7d390-128">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="7d390-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




