---
description: El identificador de flujo del receptor de flujo asociado a este nodo de topología.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: MF_TOPONODE_STREAMID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2377183927cf75c6e0a7436384426dcab94680c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715377"
---
# <a name="mf_toponode_streamid-attribute"></a><span data-ttu-id="375f6-103">\_ \_ Atributo STREAMID de MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="375f6-103">MF\_TOPONODE\_STREAMID attribute</span></span>

<span data-ttu-id="375f6-104">El identificador de flujo del receptor de flujo asociado a este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="375f6-104">The stream identifier of the stream sink associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="375f6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="375f6-105">Data type</span></span>

<span data-ttu-id="375f6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="375f6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="375f6-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="375f6-107">Remarks</span></span>

<span data-ttu-id="375f6-108">Este atributo se aplica a los nodos de salida (**\_ nodo de \_ salida \_ de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="375f6-108">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="375f6-109">Cuando la sesión multimedia carga la topología, consulta el receptor de medios para obtener un receptor de flujo con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="375f6-109">When the Media Session loads the topology, it queries the media sink for a stream sink with the specified identifier.</span></span> <span data-ttu-id="375f6-110">Si se produce un error, intenta agregar un nuevo receptor de la secuencia al receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="375f6-110">If that fails, it attempts to add a new stream sink to the media sink.</span></span>

<span data-ttu-id="375f6-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="375f6-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="375f6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="375f6-112">Requirements</span></span>



| <span data-ttu-id="375f6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="375f6-113">Requirement</span></span> | <span data-ttu-id="375f6-114">Value</span><span class="sxs-lookup"><span data-stu-id="375f6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="375f6-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="375f6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="375f6-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="375f6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="375f6-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="375f6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="375f6-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="375f6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="375f6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="375f6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="375f6-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="375f6-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="375f6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="375f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375f6-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="375f6-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="375f6-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="375f6-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="375f6-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="375f6-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="375f6-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="375f6-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="375f6-126">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="375f6-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




