---
title: Editar contextos
description: Editar contextos
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Marco de trabajo de servicios de texto (TSF), editar contextos
- TSF (marco de trabajo de servicios de texto), editar contextos
- servicios de texto, editar contextos
- Aplicaciones habilitadas para TSF, editar contextos
- Editar contextos
- Marco de trabajo de servicios de texto (TSF), editar cookies
- TSF (marco de trabajo de servicios de texto), editar cookies
- servicios de texto, editar cookies
- Aplicaciones habilitadas para TSF, editar cookies
- Editar cookies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903373"
---
# <a name="edit-contexts"></a><span data-ttu-id="ae41e-113">Editar contextos</span><span class="sxs-lookup"><span data-stu-id="ae41e-113">Edit Contexts</span></span>

## <a name="applications"></a><span data-ttu-id="ae41e-114">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="ae41e-114">Applications</span></span>

<span data-ttu-id="ae41e-115">Para crear un contexto de edición, una aplicación llama a [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="ae41e-115">To create an edit context, an application calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>

## <a name="text-services"></a><span data-ttu-id="ae41e-116">Servicios de texto</span><span class="sxs-lookup"><span data-stu-id="ae41e-116">Text Services</span></span>

<span data-ttu-id="ae41e-117">A menudo, un servicio de texto utiliza el contexto de edición actualmente activo.</span><span class="sxs-lookup"><span data-stu-id="ae41e-117">A text service often uses the currently active edit context.</span></span> <span data-ttu-id="ae41e-118">El contexto de edición actualmente activo es el contexto de edición situado en la parte superior de la pila del administrador de documentos activo.</span><span class="sxs-lookup"><span data-stu-id="ae41e-118">The currently active edit context is the edit context at the top of the stack of the active document manager.</span></span> <span data-ttu-id="ae41e-119">Para obtener el contexto activo actualmente, un servicio de texto llama a [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) para obtener el administrador de documentos activo y, a continuación, llama a [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) para obtener el contexto de edición en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="ae41e-119">To obtain the currently active context, a text service calls [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) to obtain the active document manager and then calls [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) to obtain the edit context at the top of the stack.</span></span>

<span data-ttu-id="ae41e-120">En algunos casos, un servicio de texto requiere su propio contexto de edición.</span><span class="sxs-lookup"><span data-stu-id="ae41e-120">In some cases, a text service requires its own edit context.</span></span> <span data-ttu-id="ae41e-121">Para crear un contexto de edición, un servicio de texto llama a **ITfDocumentMgr:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="ae41e-121">To create an edit context, a text service calls **ITfDocumentMgr::CreateContext**.</span></span>

## <a name="edit-cookies"></a><span data-ttu-id="ae41e-122">Editar cookies</span><span class="sxs-lookup"><span data-stu-id="ae41e-122">Edit Cookies</span></span>

<span data-ttu-id="ae41e-123">Muchos métodos, como [ITfRange:: setText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), requieren una manera de identificar un contexto de edición que tiene un [bloqueo de documento](document-locks.md)de solo lectura o de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ae41e-123">Many methods, such as [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), require a way to identify an edit context that has a read-only or read/write [document lock](document-locks.md).</span></span> <span data-ttu-id="ae41e-124">Se obtiene un bloqueo de documento a través de una negociación entre el administrador de TSF y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae41e-124">A document lock is obtained through a negotiation between the TSF manager and the application.</span></span> <span data-ttu-id="ae41e-125">Un servicio de texto no puede realizar esta negociación directamente.</span><span class="sxs-lookup"><span data-stu-id="ae41e-125">A text service cannot perform this negotiation directly.</span></span> <span data-ttu-id="ae41e-126">Un servicio de texto solo puede obtener un bloqueo solicitando una [sesión de edición](edit-sessions.md) con un contexto específico y acceso de solo lectura o de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ae41e-126">A text service can only obtain a lock by requesting an [edit session](edit-sessions.md) with a specific context and read-only or read/write access.</span></span> <span data-ttu-id="ae41e-127">Cuando se concede la sesión de edición, el servicio de texto se proporciona con una *cookie de edición* que identifica el contexto de edición con el acceso solicitado.</span><span class="sxs-lookup"><span data-stu-id="ae41e-127">When the edit session is granted, the text service is supplied with an *edit cookie* that identifies the edit context with the requested access.</span></span> <span data-ttu-id="ae41e-128">A continuación, esta cookie se pasa al método para identificar el contexto de edición con el acceso adecuado.</span><span class="sxs-lookup"><span data-stu-id="ae41e-128">This cookie is then passed to the method to identify the edit context with the proper access.</span></span>

<span data-ttu-id="ae41e-129">**ITfDocumentMgr:: CreateContext** también proporciona una cookie de edición para el creador del contexto.</span><span class="sxs-lookup"><span data-stu-id="ae41e-129">**ITfDocumentMgr::CreateContext** also supplies an edit cookie to the context creator.</span></span> <span data-ttu-id="ae41e-130">Esta cookie tiene acceso de solo lectura y no hay ninguna manera de modificar el nivel de acceso.</span><span class="sxs-lookup"><span data-stu-id="ae41e-130">This cookie has read-only access and there is no way to modify the access level.</span></span> <span data-ttu-id="ae41e-131">En realidad, el administrador de TSF no negocia un bloqueo de documento para esta cookie de edición.</span><span class="sxs-lookup"><span data-stu-id="ae41e-131">In truth, the TSF manager does not negotiate a document lock for this edit cookie.</span></span> <span data-ttu-id="ae41e-132">La cookie está marcada internamente como de solo lectura, pero el documento no está realmente bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ae41e-132">The cookie is internally marked read-only, but the document is not actually locked.</span></span> <span data-ttu-id="ae41e-133">Por ejemplo, si el creador de contexto llama a [ITfContext:: getSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) con la cookie de edición devuelta por **ITfDocumentMgr:: CreateContext** , esto da como resultado la llamada a [ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) o [ITextStoreAnchor:: getSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae41e-133">For example, if the context creator calls [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) with the edit cookie returned by **ITfDocumentMgr::CreateContext** , this results in the application's [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) or [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) being called.</span></span> <span data-ttu-id="ae41e-134">Antes de obtener la selección, la aplicación determinará si existe un bloqueo de documento.</span><span class="sxs-lookup"><span data-stu-id="ae41e-134">Before obtaining the selection, the application will determine if a document lock exists.</span></span> <span data-ttu-id="ae41e-135">Dado que no existe ningún bloqueo, se producirá un error en la aplicación con el bloqueo de TS \_ E \_ .</span><span class="sxs-lookup"><span data-stu-id="ae41e-135">Because no lock exists, the application will fail with TS\_E\_NOLOCK.</span></span> <span data-ttu-id="ae41e-136">Es decir, si una aplicación llama a un método con esta cookie que da como resultado la llamada a uno de los métodos del almacén de texto de la aplicación, debe tratar este caso internamente porque la aplicación no tendrá realmente un bloqueo del documento.</span><span class="sxs-lookup"><span data-stu-id="ae41e-136">That is, if an application calls a method with this cookie that results in one of the application's text store methods being called, it must handle this case internally because the application will not actually have a document lock.</span></span>

<span data-ttu-id="ae41e-137">Si el creador del contexto requiere una cookie de edición con acceso de lectura y escritura, debe establecer su propia sesión de edición.</span><span class="sxs-lookup"><span data-stu-id="ae41e-137">If the context creator requires an edit cookie with read/write access, it must establish its own edit session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae41e-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae41e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae41e-139">ITfContext</span><span class="sxs-lookup"><span data-stu-id="ae41e-139">ITfContext</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[<span data-ttu-id="ae41e-140">ITfDocumentMgr:: CreateContext</span><span class="sxs-lookup"><span data-stu-id="ae41e-140">ITfDocumentMgr::CreateContext</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="ae41e-141">ITfThreadMgr::GetFocus</span><span class="sxs-lookup"><span data-stu-id="ae41e-141">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[<span data-ttu-id="ae41e-142">ITfDocumentMgr:: GetTop</span><span class="sxs-lookup"><span data-stu-id="ae41e-142">ITfDocumentMgr::GetTop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[<span data-ttu-id="ae41e-143">ITfRange:: SetText</span><span class="sxs-lookup"><span data-stu-id="ae41e-143">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="ae41e-144">Bloqueos de documento</span><span class="sxs-lookup"><span data-stu-id="ae41e-144">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="ae41e-145">Sesiones de edición</span><span class="sxs-lookup"><span data-stu-id="ae41e-145">Edit Sessions</span></span>](edit-sessions.md)
</dt> <dt>

[<span data-ttu-id="ae41e-146">ITfContext::GetSelection</span><span class="sxs-lookup"><span data-stu-id="ae41e-146">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="ae41e-147">ITextStoreACP:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="ae41e-147">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="ae41e-148">ITextStoreAnchor::GetSelection</span><span class="sxs-lookup"><span data-stu-id="ae41e-148">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




