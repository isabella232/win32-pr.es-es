---
description: Identifica qué secuencia generó un evento de captura.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908464"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a><span data-ttu-id="05c4e-103">\_Atributo de \_ \_ Índice de \_ secuencia de eventos \_ MF del motor de captura</span><span class="sxs-lookup"><span data-stu-id="05c4e-103">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX attribute</span></span>

<span data-ttu-id="05c4e-104">Identifica qué secuencia generó un evento de captura.</span><span class="sxs-lookup"><span data-stu-id="05c4e-104">Identifies which stream generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="05c4e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="05c4e-105">Data type</span></span>

<span data-ttu-id="05c4e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="05c4e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="05c4e-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="05c4e-107">Get/set</span></span>

<span data-ttu-id="05c4e-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="05c4e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="05c4e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05c4e-109">Remarks</span></span>

<span data-ttu-id="05c4e-110">Este atributo aparece en algunos eventos del motor de captura.</span><span class="sxs-lookup"><span data-stu-id="05c4e-110">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="05c4e-111">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) en el objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="05c4e-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) on the event object.</span></span> <span data-ttu-id="05c4e-112">El objeto de evento se pasa a la aplicación a través del método [**IMFCaptureEngineOnEventCallback:: onEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="05c4e-112">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c4e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c4e-113">Requirements</span></span>



| <span data-ttu-id="05c4e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c4e-114">Requirement</span></span> | <span data-ttu-id="05c4e-115">Value</span><span class="sxs-lookup"><span data-stu-id="05c4e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c4e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05c4e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="05c4e-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="05c4e-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="05c4e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05c4e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="05c4e-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="05c4e-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="05c4e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05c4e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c4e-121"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c4e-121"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05c4e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="05c4e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c4e-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c4e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="05c4e-124">**IMFCaptureEngineOnEventCallback:: onEvent**</span><span class="sxs-lookup"><span data-stu-id="05c4e-124">**IMFCaptureEngineOnEventCallback::OnEvent**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




