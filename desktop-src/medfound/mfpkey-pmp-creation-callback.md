---
description: Establece una devolución de llamada que crea la sesión de medios de PMP durante la resolución del origen.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Propiedad MFPKEY_PMP_Creation_Callback (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276308"
---
# <a name="mfpkey_pmp_creation_callback-property"></a><span data-ttu-id="2355e-103">\_Propiedad de \_ devolución de llamada de creación de MFPKEY PMP \_</span><span class="sxs-lookup"><span data-stu-id="2355e-103">MFPKEY\_PMP\_Creation\_Callback property</span></span>

<span data-ttu-id="2355e-104">Establece una devolución de llamada que crea la [sesión de medios de PMP](pmp-media-session.md) durante la resolución del origen.</span><span class="sxs-lookup"><span data-stu-id="2355e-104">Sets a callback that creates the [PMP Media Session](pmp-media-session.md) during source resolution.</span></span>



<span data-ttu-id="2355e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2355e-105">Data type</span></span>

<span data-ttu-id="2355e-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="2355e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2355e-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="2355e-107">PROPVARIANT member</span></span>

<span data-ttu-id="2355e-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="2355e-108">\**IUnknown\** _</span></span>

<span data-ttu-id="2355e-109">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="2355e-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="2355e-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="2355e-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="2355e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2355e-111">Remarks</span></span>

<span data-ttu-id="2355e-112">Algunos contenidos protegidos pueden requerir el uso de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2355e-112">Some protected content might require the use of this property.</span></span> <span data-ttu-id="2355e-113">Si es así, se produce un error en el proceso de resolución de origen con el código de error **MF \_ E la \_ resolución \_ requiere una devolución de llamada de \_ \_ creación \_ de PMP**.</span><span class="sxs-lookup"><span data-stu-id="2355e-113">If so, the source resolution process fails with the error code **MF\_E\_RESOLUTION\_REQUIRES\_PMP\_CREATION\_CALLBACK**.</span></span>

<span data-ttu-id="2355e-114">Para usar esta propiedad, haga lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2355e-114">To use this property, do the following.</span></span>

1.  <span data-ttu-id="2355e-115">Llame a [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para crear un almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2355e-115">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a property store.</span></span>
2.  <span data-ttu-id="2355e-116">Implemente la interfaz de devolución de llamada [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="2355e-116">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback interface.</span></span>
3.  <span data-ttu-id="2355e-117">Establezca la \_ \_ \_ propiedad de devolución de llamada de creación de MFPKEY PMP en el almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2355e-117">Set the MFPKEY\_PMP\_Creation\_Callback property on the property store.</span></span> <span data-ttu-id="2355e-118">El valor es un puntero a la implementación de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="2355e-118">The value is a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementation.</span></span>
4.  <span data-ttu-id="2355e-119">Llame a [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="2355e-119">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span> <span data-ttu-id="2355e-120">Pase un puntero al almacén de propiedades en el parámetro *pProps* .</span><span class="sxs-lookup"><span data-stu-id="2355e-120">Pass in a pointer to the property store in the *pProps* parameter.</span></span>

<span data-ttu-id="2355e-121">En el método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de la interfaz de devolución de llamada, haga lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2355e-121">In the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of your callback interface, do the following.</span></span>

1.  <span data-ttu-id="2355e-122">Llame a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para crear la [sesión de medios de PMP](pmp-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="2355e-122">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the [PMP Media Session](pmp-media-session.md).</span></span>
2.  <span data-ttu-id="2355e-123">Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en la sesión de medios de PMP a un puntero a la interfaz [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .</span><span class="sxs-lookup"><span data-stu-id="2355e-123">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the PMP Media Session to a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span>
3.  <span data-ttu-id="2355e-124">Llame a [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) en el objeto de resultado que se pasa en el parámetro *pAsyncResult* de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="2355e-124">Call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) on the result object that is passed in the *pAsyncResult* parameter of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="2355e-125">Consulte el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) devuelto para la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="2355e-125">Query the returned [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
4.  <span data-ttu-id="2355e-126">Llame a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) con los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="2355e-126">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) with the following parameters:</span></span>
    -   <span data-ttu-id="2355e-127">*dwQueue*: **\_ estándar de \_ cola \_ de devolución de llamada MFASYNC**</span><span class="sxs-lookup"><span data-stu-id="2355e-127">*dwQueue*: **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**</span></span>
    -   <span data-ttu-id="2355e-128">*pCallback*: el puntero [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) obtenido en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="2355e-128">*pCallback*: The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) pointer obtained in step 3.</span></span>
    -   <span data-ttu-id="2355e-129">*pState*: el puntero [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) obtenido en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="2355e-129">*pState*: The [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) pointer obtained in step 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="2355e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2355e-130">Requirements</span></span>



| <span data-ttu-id="2355e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2355e-131">Requirement</span></span> | <span data-ttu-id="2355e-132">Value</span><span class="sxs-lookup"><span data-stu-id="2355e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2355e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2355e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2355e-134">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="2355e-134">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2355e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2355e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2355e-136">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="2355e-136">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2355e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2355e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2355e-138"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2355e-138"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2355e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2355e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2355e-140">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2355e-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2355e-141">Sesión de medios de PMP</span><span class="sxs-lookup"><span data-stu-id="2355e-141">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="2355e-142">Ruta de acceso a medios protegidos</span><span class="sxs-lookup"><span data-stu-id="2355e-142">Protected Media Path</span></span>](protected-media-path.md)
</dt> <dt>

[<span data-ttu-id="2355e-143">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="2355e-143">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
