---
description: Especifica si el cargador de topología cambiará los tipos de medios en una transformación de Media Foundation (MFT). Normalmente, las aplicaciones no usan este atributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: MF_ACTIVATE_MFT_LOCKED atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155572"
---
# <a name="mf_activate_mft_locked-attribute"></a><span data-ttu-id="96925-104">MF \_ activar \_ atributo de MFT \_ bloqueado</span><span class="sxs-lookup"><span data-stu-id="96925-104">MF\_ACTIVATE\_MFT\_LOCKED attribute</span></span>

<span data-ttu-id="96925-105">Especifica si el cargador de topología cambiará los tipos de medios en una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="96925-105">Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT).</span></span> <span data-ttu-id="96925-106">Normalmente, las aplicaciones no usan este atributo.</span><span class="sxs-lookup"><span data-stu-id="96925-106">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="96925-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="96925-107">Data type</span></span>

<span data-ttu-id="96925-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="96925-108">**UINT32**</span></span>

<span data-ttu-id="96925-109">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="96925-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96925-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96925-110">Remarks</span></span>

<span data-ttu-id="96925-111">Si el valor de este atributo es distinto de cero, el cargador de topología no cambiará los tipos de medios en la MFT.</span><span class="sxs-lookup"><span data-stu-id="96925-111">If value of this attribute is nonzero, the topology loader will not change the media types on the MFT.</span></span> <span data-ttu-id="96925-112">El cargador de topología establece este atributo después de cargar la topología.</span><span class="sxs-lookup"><span data-stu-id="96925-112">The topology loader sets this attribute after it loads the topology.</span></span>

<span data-ttu-id="96925-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="96925-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="96925-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96925-114">Requirements</span></span>



| <span data-ttu-id="96925-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96925-115">Requirement</span></span> | <span data-ttu-id="96925-116">Value</span><span class="sxs-lookup"><span data-stu-id="96925-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96925-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96925-117">Minimum supported client</span></span><br/> | <span data-ttu-id="96925-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96925-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="96925-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96925-119">Minimum supported server</span></span><br/> | <span data-ttu-id="96925-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96925-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="96925-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96925-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="96925-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96925-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96925-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="96925-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96925-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96925-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="96925-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="96925-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="96925-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="96925-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="96925-127">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="96925-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




