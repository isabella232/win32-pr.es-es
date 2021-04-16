---
description: Especifica si IMFTransform usa DRM de hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497764"
---
# <a name="mft_using_hardware_drm-attribute"></a><span data-ttu-id="315de-103">MFT \_ con \_ el \_ atributo DRM de hardware</span><span class="sxs-lookup"><span data-stu-id="315de-103">MFT\_USING\_HARDWARE\_DRM attribute</span></span>

<span data-ttu-id="315de-104">Especifica si IMFTransform usa DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="315de-104">Specifies whether the IMFTransform is using hardware DRM.</span></span>

## <a name="data-type"></a><span data-ttu-id="315de-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="315de-105">Data type</span></span>

<span data-ttu-id="315de-106">**UINT32** (se trata como **bool**)</span><span class="sxs-lookup"><span data-stu-id="315de-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="315de-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="315de-107">Get/set</span></span>

<span data-ttu-id="315de-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="315de-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="315de-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="315de-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="315de-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="315de-110">Applies to</span></span>

[<span data-ttu-id="315de-111">**IMTransfrom**</span><span class="sxs-lookup"><span data-stu-id="315de-111">**IMTransfrom**</span></span>](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a><span data-ttu-id="315de-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="315de-112">Remarks</span></span>

<span data-ttu-id="315de-113">Si un Decrypter de MFT especifica este atributo establecido en 1, se usa DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="315de-113">If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM.</span></span> <span data-ttu-id="315de-114">Si un Decrypter de MFT especifica este atributo establecido en 0, no utiliza DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="315de-114">If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM.</span></span> <span data-ttu-id="315de-115">Si un Decrypter de MFT no especifica este atributo o lo especifica con un valor diferente, no (o no puede) indicar si está usando DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="315de-115">If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM.</span></span>


<span data-ttu-id="315de-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="315de-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="315de-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="315de-117">Requirements</span></span>



| <span data-ttu-id="315de-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="315de-118">Requirement</span></span> | <span data-ttu-id="315de-119">Value</span><span class="sxs-lookup"><span data-stu-id="315de-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="315de-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="315de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="315de-121">Actualización 2020 de abril de Windows 10</span><span class="sxs-lookup"><span data-stu-id="315de-121">Windows 10 April 2020 Update</span></span>   <br/>                                       |
| <span data-ttu-id="315de-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="315de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="315de-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="315de-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="315de-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="315de-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="315de-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="315de-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315de-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="315de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315de-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="315de-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="315de-128">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="315de-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




