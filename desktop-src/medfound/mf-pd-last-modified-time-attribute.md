---
description: Especifica cuándo se modificó por última vez una presentación.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: MF_PD_LAST_MODIFIED_TIME atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002305"
---
# <a name="mf_pd_last_modified_time-attribute"></a><span data-ttu-id="c62f5-103">\_Atributo de \_ hora de última \_ modificación \_ de MF PD</span><span class="sxs-lookup"><span data-stu-id="c62f5-103">MF\_PD\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="c62f5-104">Especifica cuándo se modificó por última vez una presentación.</span><span class="sxs-lookup"><span data-stu-id="c62f5-104">Specifies when a presentation was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="c62f5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c62f5-105">Data type</span></span>

<span data-ttu-id="c62f5-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="c62f5-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="c62f5-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c62f5-107">Remarks</span></span>

<span data-ttu-id="c62f5-108">Los orígenes multimedia pueden establecer este atributo en un descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="c62f5-108">Media sources can set this attribute on a presentation descriptor.</span></span> <span data-ttu-id="c62f5-109">El valor del atributo es una estructura **FILETIME** , que se documenta en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c62f5-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="c62f5-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c62f5-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c62f5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c62f5-111">Requirements</span></span>



| <span data-ttu-id="c62f5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c62f5-112">Requirement</span></span> | <span data-ttu-id="c62f5-113">Value</span><span class="sxs-lookup"><span data-stu-id="c62f5-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c62f5-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c62f5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c62f5-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c62f5-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c62f5-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c62f5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c62f5-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c62f5-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c62f5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c62f5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c62f5-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c62f5-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62f5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c62f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62f5-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c62f5-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c62f5-122">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="c62f5-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="c62f5-123">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="c62f5-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="c62f5-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c62f5-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c62f5-125">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="c62f5-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




