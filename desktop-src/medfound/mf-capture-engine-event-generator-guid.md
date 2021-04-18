---
description: Identifica el componente que generó un evento de captura.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705749"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a><span data-ttu-id="8f620-103">\_ \_ \_ \_ Atributo GUID del generador de eventos MF del motor de captura \_</span><span class="sxs-lookup"><span data-stu-id="8f620-103">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID attribute</span></span>

<span data-ttu-id="8f620-104">Identifica el componente que generó un evento de captura.</span><span class="sxs-lookup"><span data-stu-id="8f620-104">Identifies the component that generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="8f620-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8f620-105">Data type</span></span>

<span data-ttu-id="8f620-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8f620-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8f620-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f620-107">Remarks</span></span>

<span data-ttu-id="8f620-108">Este atributo aparece en algunos eventos del motor de captura.</span><span class="sxs-lookup"><span data-stu-id="8f620-108">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="8f620-109">Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) en el objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="8f620-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) on the event object.</span></span> <span data-ttu-id="8f620-110">El objeto de evento se pasa a la aplicación a través del método [**IMFCaptureEngineOnEventCallback:: onEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="8f620-110">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

<span data-ttu-id="8f620-111">El valor es un identificador de interfaz para el componente que generó el evento.</span><span class="sxs-lookup"><span data-stu-id="8f620-111">The value is an interface identifier for the component that generated the event.</span></span> <span data-ttu-id="8f620-112">Por ejemplo, el IID de valor **\_ IMFCapturePreviewSink** indica el receptor de versión preliminar ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span><span class="sxs-lookup"><span data-stu-id="8f620-112">For example, the value **IID\_IMFCapturePreviewSink** indicates the preview sink ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span></span> <span data-ttu-id="8f620-113">No todos los eventos de captura contienen este atributo.</span><span class="sxs-lookup"><span data-stu-id="8f620-113">Not every capture event contains this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f620-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f620-114">Requirements</span></span>



| <span data-ttu-id="8f620-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f620-115">Requirement</span></span> | <span data-ttu-id="8f620-116">Value</span><span class="sxs-lookup"><span data-stu-id="8f620-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f620-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f620-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f620-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f620-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8f620-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f620-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f620-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f620-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8f620-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f620-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f620-122"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f620-122"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f620-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f620-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f620-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f620-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f620-125">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="8f620-125">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f620-126">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="8f620-126">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




