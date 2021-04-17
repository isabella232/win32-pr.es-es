---
description: Especifica el tipo MIME del contenido.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: MF_PD_MIME_TYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1893253af139a73555d3a4fd483e9f59c5ae1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659913"
---
# <a name="mf_pd_mime_type-attribute"></a><span data-ttu-id="b5bae-103">MF \_ PD \_ ( \_ atributo de tipo MIME)</span><span class="sxs-lookup"><span data-stu-id="b5bae-103">MF\_PD\_MIME\_TYPE attribute</span></span>

<span data-ttu-id="b5bae-104">Especifica el tipo MIME del contenido.</span><span class="sxs-lookup"><span data-stu-id="b5bae-104">Specifies the MIME type of the content.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5bae-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b5bae-105">Data type</span></span>

<span data-ttu-id="b5bae-106">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="b5bae-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="b5bae-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5bae-107">Remarks</span></span>

<span data-ttu-id="b5bae-108">Este atributo se aplica a los descriptores de presentación.</span><span class="sxs-lookup"><span data-stu-id="b5bae-108">This attribute applies to presentation descriptors.</span></span>

<span data-ttu-id="b5bae-109">El tipo MIME expuesto a través de [System. MIMEType](../properties/props-system-mimetype.md) para archivos multimedia puede tener una diferencia hacia elegir tipos MIME adecuados para la Alianza de redes digitales (DLNA).</span><span class="sxs-lookup"><span data-stu-id="b5bae-109">The MIME type exposed through [System.MIMEType](../properties/props-system-mimetype.md) for media files may have a bias towards choosing MIME types suitable for Digital Living Network Alliance (DLNA).</span></span>

<span data-ttu-id="b5bae-110">El \_ \_ tipo MIME \_ de MF PD y [System. MIMEType](../properties/props-system-mimetype.md) no siempre coinciden.</span><span class="sxs-lookup"><span data-stu-id="b5bae-110">MF\_PD\_MIME\_TYPE and [System.MIMEType](../properties/props-system-mimetype.md) may not always match.</span></span>

<span data-ttu-id="b5bae-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b5bae-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5bae-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5bae-112">Requirements</span></span>



| <span data-ttu-id="b5bae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5bae-113">Requirement</span></span> | <span data-ttu-id="b5bae-114">Value</span><span class="sxs-lookup"><span data-stu-id="b5bae-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5bae-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5bae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b5bae-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="b5bae-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b5bae-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5bae-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b5bae-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="b5bae-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b5bae-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5bae-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5bae-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5bae-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5bae-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5bae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5bae-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5bae-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5bae-123">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="b5bae-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="b5bae-124">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="b5bae-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="b5bae-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b5bae-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b5bae-126">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="b5bae-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
