---
description: Contiene un valor definido por el autor de la llamada para un evento METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: MF_EVENT_MFT_CONTEXT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082348"
---
# <a name="mf_event_mft_context-attribute"></a><span data-ttu-id="c050e-103">\_Atributo de \_ contexto de MFT de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="c050e-103">MF\_EVENT\_MFT\_CONTEXT attribute</span></span>

<span data-ttu-id="c050e-104">Contiene un valor definido por el autor de la llamada para un evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="c050e-104">Contains a caller-defined value for an [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="data-type"></a><span data-ttu-id="c050e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c050e-105">Data type</span></span>

<span data-ttu-id="c050e-106">**ULong \_ PTR** almacenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="c050e-106">**ULONG\_PTR** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="c050e-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="c050e-107">Get/set</span></span>

<span data-ttu-id="c050e-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="c050e-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="c050e-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="c050e-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c050e-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c050e-110">Applies to</span></span>

[<span data-ttu-id="c050e-111">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="c050e-111">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="c050e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c050e-112">Remarks</span></span>

<span data-ttu-id="c050e-113">Este atributo se usa con el evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="c050e-113">This attribute is used with the [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="c050e-114">El valor del atributo se toma del parámetro *ulParam* del método [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .</span><span class="sxs-lookup"><span data-stu-id="c050e-114">The value of the attribute is taken from the *ulParam* parameter of the [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) method.</span></span>

<span data-ttu-id="c050e-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c050e-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c050e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c050e-116">Requirements</span></span>



| <span data-ttu-id="c050e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c050e-117">Requirement</span></span> | <span data-ttu-id="c050e-118">Value</span><span class="sxs-lookup"><span data-stu-id="c050e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c050e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c050e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c050e-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="c050e-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c050e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c050e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c050e-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c050e-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c050e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c050e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c050e-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c050e-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c050e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c050e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c050e-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c050e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c050e-127">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="c050e-127">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="c050e-128">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="c050e-128">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




