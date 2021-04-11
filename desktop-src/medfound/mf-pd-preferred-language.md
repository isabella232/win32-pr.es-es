---
description: Contiene el idioma RFC 1766 preferido del origen multimedia.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: MF_PD_PREFERRED_LANGUAGE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279048"
---
# <a name="mf_pd_preferred_language-attribute"></a><span data-ttu-id="c3490-103">MF \_ PD \_ \_ atributo de idioma preferido</span><span class="sxs-lookup"><span data-stu-id="c3490-103">MF\_PD\_PREFERRED\_LANGUAGE attribute</span></span>

<span data-ttu-id="c3490-104">Contiene el idioma RFC 1766 preferido del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="c3490-104">Contains the preferred RFC 1766 language of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3490-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c3490-105">Data type</span></span>

<span data-ttu-id="c3490-106">**WCHAR**</span><span class="sxs-lookup"><span data-stu-id="c3490-106">**WCHAR**</span></span>

## <a name="getset"></a><span data-ttu-id="c3490-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="c3490-107">Get/set</span></span>

<span data-ttu-id="c3490-108">Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="c3490-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="c3490-109">Para establecer este atributo, llame a [**IMFAttributes:: Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="c3490-109">To set this attribute, call [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c3490-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c3490-110">Applies to</span></span>

[<span data-ttu-id="c3490-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c3490-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="c3490-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3490-112">Remarks</span></span>

<span data-ttu-id="c3490-113">El \_ atributo de \_ idioma preferido MF PD \_ es opcional.</span><span class="sxs-lookup"><span data-stu-id="c3490-113">The MF\_PD\_PREFERRED\_LANGUAGE attribute is optional.</span></span> <span data-ttu-id="c3490-114">Una aplicación puede establecer este atributo en un origen de medios (como un origen de red) para especificar su idioma preferido.</span><span class="sxs-lookup"><span data-stu-id="c3490-114">An application can set this attribute on a media source (such as a network source) to specify its preferred language.</span></span>

<span data-ttu-id="c3490-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c3490-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3490-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3490-116">Requirements</span></span>



| <span data-ttu-id="c3490-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3490-117">Requirement</span></span> | <span data-ttu-id="c3490-118">Value</span><span class="sxs-lookup"><span data-stu-id="c3490-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3490-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3490-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3490-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="c3490-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c3490-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3490-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3490-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c3490-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c3490-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3490-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3490-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3490-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3490-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3490-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3490-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3490-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3490-127">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="c3490-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




