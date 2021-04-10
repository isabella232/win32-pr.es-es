---
title: Bloqueos de documento
description: Bloqueos de documento
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Marco de trabajo de servicios de texto (TSF), bloqueos de documento
- TSF (marco de trabajo de servicios de texto), bloqueos de documento
- Aplicaciones habilitadas para TSF, bloqueos de documentos
- bloqueos de documento
- Marco de trabajo de servicios de texto (TSF), posición de caracteres de aplicación (ACP)
- TSF (marco de trabajo de servicios de texto), posición de carácter de aplicación (ACP)
- Aplicaciones habilitadas para TSF, posición de caracteres de aplicación (ACP)
- Posición de carácter de aplicación (ACP)
- ACP (posición de carácter de aplicación)
- Text Services Framework (TSF), delimitadores
- TSF (marco de trabajo de servicios de texto), delimitadores
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268529"
---
# <a name="document-locks"></a><span data-ttu-id="c6b1e-116">Bloqueos de documento</span><span class="sxs-lookup"><span data-stu-id="c6b1e-116">Document Locks</span></span>

## <a name="the-document-lock-protocol"></a><span data-ttu-id="c6b1e-117">Protocolo de bloqueo de documento</span><span class="sxs-lookup"><span data-stu-id="c6b1e-117">The Document Lock Protocol</span></span>

<span data-ttu-id="c6b1e-118">Para solicitar un bloqueo de documento para aplicaciones basadas en ACP, el administrador de TSF llama a [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span><span class="sxs-lookup"><span data-stu-id="c6b1e-118">To request a document lock for ACP-based applications, the TSF manager calls [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span></span> <span data-ttu-id="c6b1e-119">En el caso de las aplicaciones basadas en delimitadores, el administrador de TSF llama a [ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span><span class="sxs-lookup"><span data-stu-id="c6b1e-119">For anchor-based applications, the TSF manager calls [ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span></span> <span data-ttu-id="c6b1e-120">La aplicación concede el bloqueo del documento mediante una llamada a [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (aplicaciones basadas en ACP) o [ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (aplicaciones basadas en delimitadores) dentro de **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-120">The application grants the document lock by calling [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-based applications) or [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (anchor-based applications) inside of **RequestLock**.</span></span> <span data-ttu-id="c6b1e-121">El bloqueo solo es válido durante la llamada a **OnLockGranted** .</span><span class="sxs-lookup"><span data-stu-id="c6b1e-121">The lock is only valid during the **OnLockGranted** call.</span></span> <span data-ttu-id="c6b1e-122">Cuando **OnLockGranted** devuelve, el documento se considera desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-122">When **OnLockGranted** returns, the document is considered unlocked.</span></span>

## <a name="types-of-document-locks"></a><span data-ttu-id="c6b1e-123">Tipos de bloqueos de documento</span><span class="sxs-lookup"><span data-stu-id="c6b1e-123">Types of Document Locks</span></span>

<span data-ttu-id="c6b1e-124">Hay dos tipos de bloqueos de documento, de solo lectura y de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-124">There are two types of document locks, read-only and read/write.</span></span> <span data-ttu-id="c6b1e-125">Un bloqueo de solo lectura permite al administrador leer el texto, pero no puede modificar ni insertar texto.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-125">A read-only lock enables the manager to read the text, but it cannot modify or insert text.</span></span> <span data-ttu-id="c6b1e-126">Un bloqueo de lectura/escritura permite al administrador leer, modificar e insertar texto.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-126">A read/write lock enables the manager to read, modify, and insert text.</span></span> <span data-ttu-id="c6b1e-127">Se solicita un bloqueo de solo lectura mediante la especificación \_ de la \_ lectura de LF de TS en *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-127">A read-only lock is requested by specifying TS\_LF\_READ in *dwFlags*.</span></span> <span data-ttu-id="c6b1e-128">Se solicita un bloqueo de lectura/escritura especificando TS \_ LF \_ ReadWrite en *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-128">A read/write lock is requested by specifying TS\_LF\_READWRITE in *dwFlags*.</span></span>

## <a name="asynchronous-and-synchronous-requests"></a><span data-ttu-id="c6b1e-129">Solicitudes asincrónicas y sincrónicas</span><span class="sxs-lookup"><span data-stu-id="c6b1e-129">Asynchronous and Synchronous Requests</span></span>

<span data-ttu-id="c6b1e-130">Una solicitud de bloqueo puede ser sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-130">A lock request can be either synchronous or asynchronous.</span></span> <span data-ttu-id="c6b1e-131">El administrador solicita un bloqueo sincrónico mediante el uso de la \_ \_ marca de sincronización LF de TS en *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-131">The manager requests a synchronous lock by using the TS\_LF\_SYNC flag in *dwFlags*.</span></span> <span data-ttu-id="c6b1e-132">Si este marcador no está presente, la solicitud es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-132">If this flag is not present, the request is asynchronous.</span></span>

## <a name="granting-the-lock"></a><span data-ttu-id="c6b1e-133">Concesión del bloqueo</span><span class="sxs-lookup"><span data-stu-id="c6b1e-133">Granting the Lock</span></span>

<span data-ttu-id="c6b1e-134">Cuando se llama a **RequestLock** , la aplicación debe determinar si el documento está bloqueado actualmente.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-134">When **RequestLock** is called, the application must determine if the document is currently locked.</span></span> <span data-ttu-id="c6b1e-135">Si el documento no está bloqueado y no existe ningún otro motivo para denegar el bloqueo, la aplicación debe establecer *phrSession* en S \_ OK y devolver S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-135">If the document is not locked, and no other reason to deny the lock exists, the application should set *phrSession* to S\_OK and return S\_OK.</span></span>

<span data-ttu-id="c6b1e-136">Si el documento está bloqueado y la solicitud de bloqueo es sincrónica, la aplicación debe establecer *phrSession* en TS \_ e \_ sincrónico y devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-136">If the document is locked and the lock request is synchronous, the application should set *phrSession* to TS\_E\_SYNCHRONOUS and return S\_OK.</span></span> <span data-ttu-id="c6b1e-137">Esto indica que no se puede conceder una solicitud sincrónica.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-137">This indicates that a synchronous request cannot be granted.</span></span>

<span data-ttu-id="c6b1e-138">Si el documento está bloqueado y la solicitud de bloqueo es asincrónica, la aplicación debe poner en cola la solicitud, establecer *phrSession* en TS \_ S \_ Async y devolver s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-138">If the document is locked and the lock request is asynchronous, the application should queue the request, set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="c6b1e-139">Cuando el documento esté disponible, la aplicación debe quitar la solicitud de la cola y llamar a **OnLockGranted**.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-139">When the document becomes available, the application should remove the request from the queue and call **OnLockGranted**.</span></span> <span data-ttu-id="c6b1e-140">Esta cola de solicitudes de bloqueo es opcional. hay un escenario que una aplicación debe admitir.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-140">This queuing of lock requests is optional; there is one scenario that an application must support.</span></span> <span data-ttu-id="c6b1e-141">Si el documento tiene un bloqueo de solo lectura, la nueva solicitud de bloqueo es de lectura y escritura y la solicitud es asincrónica, la aplicación ha llamado a **OnLockGranted** , lo que ha provocado una llamada reentrante a **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-141">If the document has a read-only lock, the new lock request is read/write and the request is asynchronous, the application has called into **OnLockGranted** , which has caused a reentrant call to **RequestLock**.</span></span> <span data-ttu-id="c6b1e-142">La aplicación debe establecer *phrSession* en TS \_ s \_ Async y devolver s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-142">The application should set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="c6b1e-143">Después de que la llamada a **OnLockGranted** devuelva, la aplicación debe procesar la solicitud de actualización mediante una llamada a **OnLockGranted** de nuevo con TS \_ LF \_ ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-143">After the call to **OnLockGranted** returns, the application should process the upgrade request by calling **OnLockGranted** again with TS\_LF\_READWRITE.</span></span>

## <a name="lock-enforcement"></a><span data-ttu-id="c6b1e-144">Aplicación de bloqueos</span><span class="sxs-lookup"><span data-stu-id="c6b1e-144">Lock Enforcement</span></span>

<span data-ttu-id="c6b1e-145">La aplicación debe asegurarse de que existe el tipo de bloqueo adecuado antes de permitir el acceso al documento.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-145">The application must ensure that the proper type of lock exists before allowing access to the document.</span></span> <span data-ttu-id="c6b1e-146">Por ejemplo, la aplicación debe comprobar que un documento tiene al menos un bloqueo de solo lectura antes de permitir [ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) para continuar.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-146">For example, the application should verify that a document has at least a read-only lock before allowing [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) to proceed.</span></span> <span data-ttu-id="c6b1e-147">Si el bloqueo adecuado no existe, la aplicación debe devolver TF \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="c6b1e-147">If the proper lock does not exist, the application should return TF\_E\_NOLOCK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6b1e-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6b1e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6b1e-149">Almacenes de texto</span><span class="sxs-lookup"><span data-stu-id="c6b1e-149">Text Stores</span></span>](text-stores.md)
</dt> <dt>

[<span data-ttu-id="c6b1e-150">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="c6b1e-150">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="c6b1e-151">ITextStoreACPSink::OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="c6b1e-151">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="c6b1e-152">ITextStoreACP:: GetText</span><span class="sxs-lookup"><span data-stu-id="c6b1e-152">ITextStoreACP::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[<span data-ttu-id="c6b1e-153">ITextStoreAnchor::RequestLock</span><span class="sxs-lookup"><span data-stu-id="c6b1e-153">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="c6b1e-154">ITextStoreAnchorSink::OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="c6b1e-154">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="c6b1e-155">ITextStoreAnchor:: GetText</span><span class="sxs-lookup"><span data-stu-id="c6b1e-155">ITextStoreAnchor::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




