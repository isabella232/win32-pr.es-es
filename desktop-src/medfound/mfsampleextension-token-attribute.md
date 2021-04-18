---
description: 'Contiene un puntero al token que se proporcionó al método IMFMediaStream:: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: MFSampleExtension_Token atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720444"
---
# <a name="mfsampleextension_token-attribute"></a><span data-ttu-id="fb275-103">Atributo de token de MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="fb275-103">MFSampleExtension\_Token attribute</span></span>

<span data-ttu-id="fb275-104">Contiene un puntero al token que se proporcionó al método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="fb275-104">Contains a pointer to the token that was provided to the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="fb275-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fb275-105">Data type</span></span>

<span data-ttu-id="fb275-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="fb275-106">\**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="fb275-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="fb275-107">Get/set</span></span>

<span data-ttu-id="fb275-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="fb275-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="fb275-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="fb275-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fb275-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="fb275-110">Applies to</span></span>

[<span data-ttu-id="fb275-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="fb275-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="fb275-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb275-112">Remarks</span></span>

<span data-ttu-id="fb275-113">Este atributo se aplica a los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="fb275-113">This attribute applies to media samples.</span></span> <span data-ttu-id="fb275-114">El valor del atributo es el puntero **IUnknown** que se pasa al parámetro *PToken* del método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="fb275-114">The value of the attribute is the **IUnknown** pointer that is passed to the *pToken* parameter of the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span> <span data-ttu-id="fb275-115">El autor de la llamada utiliza este atributo para realizar el seguimiento del estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb275-115">The caller uses this attribute to track the status of the request.</span></span>

<span data-ttu-id="fb275-116">Si está escribiendo un origen multimedia personalizado, establezca este atributo en el ejemplo cuando el flujo multimedia entregue un ejemplo en respuesta al método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , a menos que el valor de *pToken* sea **null**.</span><span class="sxs-lookup"><span data-stu-id="fb275-116">If you are writing a custom media source, set this attribute on the sample when the media stream delivers a sample in response to the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method, unless the value of *pToken* is **NULL**.</span></span>

<span data-ttu-id="fb275-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fb275-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb275-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb275-118">Requirements</span></span>



| <span data-ttu-id="fb275-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb275-119">Requirement</span></span> | <span data-ttu-id="fb275-120">Value</span><span class="sxs-lookup"><span data-stu-id="fb275-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb275-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb275-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fb275-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="fb275-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fb275-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb275-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fb275-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="fb275-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fb275-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb275-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb275-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb275-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb275-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb275-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb275-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb275-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fb275-129">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb275-129">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="fb275-130">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="fb275-130">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




