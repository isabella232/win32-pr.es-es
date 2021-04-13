---
description: Fuerza al representador de vídeo mejorado (EVR) a limitar su salida para que coincida con el ancho de banda de GPU.
ms.assetid: e81e67d6-aa72-44c1-90e9-72ab18bca1c9
title: EVRConfig_ForceThrottle atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39cef0bd032eeaf84129e74274b59dbafadbc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360095"
---
# <a name="evrconfig_forcethrottle-attribute"></a><span data-ttu-id="4554b-103">\_Atributo ForceThrottle de EVRConfig</span><span class="sxs-lookup"><span data-stu-id="4554b-103">EVRConfig\_ForceThrottle attribute</span></span>

<span data-ttu-id="4554b-104">Fuerza al representador de vídeo mejorado (EVR) a limitar su salida para que coincida con el ancho de banda de GPU.</span><span class="sxs-lookup"><span data-stu-id="4554b-104">Forces the Enhanced Video Renderer (EVR) to limit its output to match GPU bandwidth.</span></span>

## <a name="data-type"></a><span data-ttu-id="4554b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4554b-105">Data type</span></span>

<span data-ttu-id="4554b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4554b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4554b-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="4554b-107">Get/set</span></span>

<span data-ttu-id="4554b-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4554b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4554b-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4554b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="4554b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4554b-110">Remarks</span></span>

<span data-ttu-id="4554b-111">Este atributo se puede establecer en el receptor de medios EVR.</span><span class="sxs-lookup"><span data-stu-id="4554b-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="4554b-112">Para establecer el atributo, use **IUnknown:: QueryInterface** para consultar el receptor de medios EVR de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="4554b-112">To set the attribute, use **IUnknown::QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="4554b-113">Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoRenderPrefs \_ FORCEOUTPUTTHROTTLING** en EVR.</span><span class="sxs-lookup"><span data-stu-id="4554b-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceOutputThrottling** flag on the EVR.</span></span> <span data-ttu-id="4554b-114">Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obtener una descripción de esta marca.</span><span class="sxs-lookup"><span data-stu-id="4554b-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="4554b-115">La constante GUID para este atributo se exporta desde strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="4554b-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4554b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4554b-116">Requirements</span></span>



| <span data-ttu-id="4554b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4554b-117">Requirement</span></span> | <span data-ttu-id="4554b-118">Value</span><span class="sxs-lookup"><span data-stu-id="4554b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4554b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4554b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4554b-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4554b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4554b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4554b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4554b-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4554b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4554b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4554b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4554b-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="4554b-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4554b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4554b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4554b-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4554b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4554b-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="4554b-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="4554b-128">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="4554b-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




