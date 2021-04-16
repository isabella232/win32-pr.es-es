---
description: Fuerza al representador de vídeo mejorado (EVR) a llamar por lotes a IDirect3D9Device::P método reenviado.
ms.assetid: d7523000-baa0-4011-97e1-d1ffe7263d01
title: EVRConfig_ForceBatching atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6dff5d7a5e90377c8749519033b6a66ef7663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539543"
---
# <a name="evrconfig_forcebatching-attribute"></a><span data-ttu-id="9e5f2-103">\_Atributo ForceBatching de EVRConfig</span><span class="sxs-lookup"><span data-stu-id="9e5f2-103">EVRConfig\_ForceBatching attribute</span></span>

<span data-ttu-id="9e5f2-104">Fuerza al representador de vídeo mejorado (EVR) a llamar por lotes a [**IDirect3D9Device::P método reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) .</span><span class="sxs-lookup"><span data-stu-id="9e5f2-104">Forces the Enhanced Video Renderer (EVR) to batch calls to the [**IDirect3D9Device::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="9e5f2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9e5f2-105">Data type</span></span>

<span data-ttu-id="9e5f2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9e5f2-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9e5f2-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="9e5f2-107">Get/set</span></span>

<span data-ttu-id="9e5f2-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9e5f2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9e5f2-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9e5f2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5f2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e5f2-110">Remarks</span></span>

<span data-ttu-id="9e5f2-111">Este atributo se puede establecer en el receptor de medios EVR.</span><span class="sxs-lookup"><span data-stu-id="9e5f2-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="9e5f2-112">Para establecer el atributo, utilice **QueryInterface** para consultar el receptor de medios EVR de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="9e5f2-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="9e5f2-113">Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoRenderPrefs \_ FORCEBATCHING** en EVR.</span><span class="sxs-lookup"><span data-stu-id="9e5f2-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceBatching** flag on the EVR.</span></span> <span data-ttu-id="9e5f2-114">Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obtener una descripción de esta marca.</span><span class="sxs-lookup"><span data-stu-id="9e5f2-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="9e5f2-115">La constante GUID para este atributo se exporta desde strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="9e5f2-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5f2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e5f2-116">Requirements</span></span>



| <span data-ttu-id="9e5f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e5f2-117">Requirement</span></span> | <span data-ttu-id="9e5f2-118">Value</span><span class="sxs-lookup"><span data-stu-id="9e5f2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5f2-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e5f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5f2-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e5f2-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e5f2-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e5f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5f2-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e5f2-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9e5f2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e5f2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e5f2-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e5f2-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e5f2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e5f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5f2-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e5f2-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e5f2-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="9e5f2-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e5f2-128">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="9e5f2-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 
