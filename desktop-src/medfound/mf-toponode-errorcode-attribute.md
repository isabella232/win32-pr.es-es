---
description: Contiene el código de error del error de conexión más reciente de este nodo topología.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: MF_TOPONODE_ERRORCODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154989"
---
# <a name="mf_toponode_errorcode-attribute"></a><span data-ttu-id="66d83-103">\_TOPONODE el \_ atributo ERRORCODE de MF</span><span class="sxs-lookup"><span data-stu-id="66d83-103">MF\_TOPONODE\_ERRORCODE attribute</span></span>

<span data-ttu-id="66d83-104">Contiene el código de error del error de conexión más reciente de este nodo topología.</span><span class="sxs-lookup"><span data-stu-id="66d83-104">Contains the error code from the most recent connection failure for this toplogy node.</span></span>

## <a name="data-type"></a><span data-ttu-id="66d83-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="66d83-105">Data type</span></span>

<span data-ttu-id="66d83-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66d83-106">**UINT32**</span></span>

<span data-ttu-id="66d83-107">Ttreat como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66d83-107">Ttreat as an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d83-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d83-108">Remarks</span></span>

<span data-ttu-id="66d83-109">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="66d83-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="66d83-110">El valor de este atributo es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66d83-110">The value of this attribute is an **HRESULT** value.</span></span>

<span data-ttu-id="66d83-111">La sesión de medios o el cargador de topología podría establecer el atributo.</span><span class="sxs-lookup"><span data-stu-id="66d83-111">The Media Session or the topology loader might set the attribute.</span></span> <span data-ttu-id="66d83-112">Las aplicaciones normalmente leen este atributo pero no lo establecen.</span><span class="sxs-lookup"><span data-stu-id="66d83-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="66d83-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="66d83-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d83-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d83-114">Requirements</span></span>



| <span data-ttu-id="66d83-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d83-115">Requirement</span></span> | <span data-ttu-id="66d83-116">Value</span><span class="sxs-lookup"><span data-stu-id="66d83-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66d83-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="66d83-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66d83-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66d83-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="66d83-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="66d83-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66d83-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66d83-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d83-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d83-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d83-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="66d83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d83-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66d83-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66d83-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="66d83-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="66d83-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="66d83-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="66d83-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="66d83-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="66d83-128">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="66d83-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




