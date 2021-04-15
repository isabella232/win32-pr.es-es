---
description: Permite que el representador de vídeo mejorado (EVR) procese llamadas por lotes en el método reenviado de Microsoft Direct3D IDirect3DDevice9::P.
ms.assetid: 6dbb2839-97ea-4881-8f22-0f8e943a3071
title: EVRConfig_AllowBatching atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191c3c0f0ea4ad18e7bb711ae6d37c21f75cd478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539549"
---
# <a name="evrconfig_allowbatching-attribute"></a><span data-ttu-id="0192f-103">\_Atributo AllowBatching de EVRConfig</span><span class="sxs-lookup"><span data-stu-id="0192f-103">EVRConfig\_AllowBatching attribute</span></span>

<span data-ttu-id="0192f-104">Permite que el representador de vídeo mejorado (EVR) procese llamadas por lotes en el método reenviado de Microsoft Direct3D **IDirect3DDevice9::P** .</span><span class="sxs-lookup"><span data-stu-id="0192f-104">Allows the Enhanced Video Renderer (EVR) to batch calls to the Microsoft Direct3D **IDirect3DDevice9::Present** method.</span></span>

## <a name="data-type"></a><span data-ttu-id="0192f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0192f-105">Data type</span></span>

<span data-ttu-id="0192f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0192f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0192f-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="0192f-107">Get/set</span></span>

<span data-ttu-id="0192f-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0192f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0192f-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0192f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0192f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0192f-110">Remarks</span></span>

<span data-ttu-id="0192f-111">Este atributo se puede establecer en el receptor de medios EVR.</span><span class="sxs-lookup"><span data-stu-id="0192f-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="0192f-112">Para establecer el atributo, utilice **QueryInterface** para consultar el receptor de medios EVR de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="0192f-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="0192f-113">Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoRenderPrefs \_ ALLOWBATCHING** en EVR.</span><span class="sxs-lookup"><span data-stu-id="0192f-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowBatching** flag on the EVR.</span></span> <span data-ttu-id="0192f-114">Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obtener una descripción de esta marca.</span><span class="sxs-lookup"><span data-stu-id="0192f-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="0192f-115">La constante GUID para este atributo se exporta desde strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="0192f-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0192f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0192f-116">Requirements</span></span>



| <span data-ttu-id="0192f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0192f-117">Requirement</span></span> | <span data-ttu-id="0192f-118">Value</span><span class="sxs-lookup"><span data-stu-id="0192f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0192f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0192f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0192f-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0192f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0192f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0192f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0192f-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0192f-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0192f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0192f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0192f-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="0192f-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0192f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0192f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0192f-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0192f-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0192f-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="0192f-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="0192f-128">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="0192f-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




