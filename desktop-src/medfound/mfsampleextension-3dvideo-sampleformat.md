---
description: Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155973"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a><span data-ttu-id="23ef2-103">MFSampleExtension \_ 3DVideo \_ SampleFormat</span><span class="sxs-lookup"><span data-stu-id="23ef2-103">MFSampleExtension\_3DVideo\_SampleFormat attribute</span></span>

<span data-ttu-id="23ef2-104">Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="23ef2-104">Specifies how a 3D video frame is stored in a media sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="23ef2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="23ef2-105">Data type</span></span>

<span data-ttu-id="23ef2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="23ef2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="23ef2-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23ef2-107">Remarks</span></span>

<span data-ttu-id="23ef2-108">El valor de este atributo es un miembro de la enumeración [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .</span><span class="sxs-lookup"><span data-stu-id="23ef2-108">The value of this attribute is a member of the [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) enumeration.</span></span>

<span data-ttu-id="23ef2-109">Un componente que genera fotogramas de vídeo 3D debe establecer este atributo en **true** en cada ejemplo multimedia que contenga un fotograma 3D.</span><span class="sxs-lookup"><span data-stu-id="23ef2-109">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span> <span data-ttu-id="23ef2-110">El atributo se omite si el atributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) es **false** o no se establece.</span><span class="sxs-lookup"><span data-stu-id="23ef2-110">The attribute is ignored if the [MFSampleExtension\_3DVideo](mfsampleextension-3dvideo.md) attribute is **FALSE** or not set.</span></span>

## <a name="requirements"></a><span data-ttu-id="23ef2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23ef2-111">Requirements</span></span>



| <span data-ttu-id="23ef2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="23ef2-112">Requirement</span></span> | <span data-ttu-id="23ef2-113">Value</span><span class="sxs-lookup"><span data-stu-id="23ef2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23ef2-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23ef2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="23ef2-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="23ef2-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="23ef2-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23ef2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="23ef2-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="23ef2-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="23ef2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23ef2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="23ef2-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="23ef2-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ef2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="23ef2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ef2-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23ef2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="23ef2-122">MFSampleExtension \_ 3DVideo</span><span class="sxs-lookup"><span data-stu-id="23ef2-122">MFSampleExtension\_3DVideo</span></span>](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




