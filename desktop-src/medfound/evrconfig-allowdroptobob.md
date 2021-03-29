---
description: Permite que el representador de vídeo mejorado (EVR) mejore el rendimiento mediante el desentrelazado de Bob.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: EVRConfig_AllowDropToBob atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423535"
---
# <a name="evrconfig_allowdroptobob-attribute"></a><span data-ttu-id="5246b-103">\_Atributo AllowDropToBob de EVRConfig</span><span class="sxs-lookup"><span data-stu-id="5246b-103">EVRConfig\_AllowDropToBob attribute</span></span>

<span data-ttu-id="5246b-104">Permite que el representador de vídeo mejorado (EVR) mejore el rendimiento mediante el desentrelazado de Bob.</span><span class="sxs-lookup"><span data-stu-id="5246b-104">Allows the Enhanced Video Renderer (EVR) to improve performance by using bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="5246b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5246b-105">Data type</span></span>

<span data-ttu-id="5246b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5246b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5246b-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="5246b-107">Get/set</span></span>

<span data-ttu-id="5246b-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5246b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5246b-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5246b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5246b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5246b-110">Remarks</span></span>

<span data-ttu-id="5246b-111">Este atributo se puede establecer en el receptor de EVRmedia.</span><span class="sxs-lookup"><span data-stu-id="5246b-111">This attribute can be set on the EVRmedia sink.</span></span> <span data-ttu-id="5246b-112">Para establecer el atributo, **QueryInterface** para consultar el receptor de medios EVR para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="5246b-112">To set the attribute, **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="5246b-113">Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoMixPrefs \_ ALLOWDROPTOBOB** en EVR.</span><span class="sxs-lookup"><span data-stu-id="5246b-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_AllowDropToBob** flag on the EVR.</span></span> <span data-ttu-id="5246b-114">Consulte [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) para obtener una descripción de esta marca.</span><span class="sxs-lookup"><span data-stu-id="5246b-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="5246b-115">La constante GUID para este atributo se exporta desde strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="5246b-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5246b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5246b-116">Requirements</span></span>



| <span data-ttu-id="5246b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5246b-117">Requirement</span></span> | <span data-ttu-id="5246b-118">Value</span><span class="sxs-lookup"><span data-stu-id="5246b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5246b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5246b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5246b-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5246b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5246b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5246b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5246b-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5246b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5246b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5246b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5246b-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="5246b-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5246b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5246b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5246b-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5246b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5246b-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="5246b-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5246b-128">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="5246b-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




