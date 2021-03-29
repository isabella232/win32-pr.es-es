---
title: Almacenes de texto
description: Almacenes de texto
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Text Services Framework (TSF), almacenes de texto
- TSF (marco de trabajo de servicios de texto), almacenes de texto
- Aplicaciones habilitadas para TSF, almacenes de texto
- almacenes de texto
- Marco de trabajo de servicios de texto (TSF), posición de caracteres de aplicación (ACP)
- TSF (marco de trabajo de servicios de texto), posición de carácter de aplicación (ACP)
- Aplicaciones habilitadas para TSF, posición de caracteres de aplicación (ACP)
- Posición de carácter de aplicación (ACP)
- ACP (posición de carácter de aplicación)
- Text Services Framework (TSF), delimitadores
- TSF (marco de trabajo de servicios de texto), delimitadores
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
- Marco de trabajo de servicios de texto (TSF), bloqueos de documento
- TSF (marco de trabajo de servicios de texto), bloqueos de documento
- Aplicaciones habilitadas para TSF, bloqueos de documentos
- bloqueos de documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077942"
---
# <a name="text-stores"></a><span data-ttu-id="50c82-120">Almacenes de texto</span><span class="sxs-lookup"><span data-stu-id="50c82-120">Text Stores</span></span>

## <a name="application-character-position-acp"></a><span data-ttu-id="50c82-121">Posición de carácter de aplicación (ACP)</span><span class="sxs-lookup"><span data-stu-id="50c82-121">Application Character Position (ACP)</span></span>

<span data-ttu-id="50c82-122">Un ACP es la ubicación de un carácter o caracteres en una secuencia de texto que se expresa como el número de caracteres desde el inicio de la secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="50c82-122">An ACP is the location of a character, or characters, in a text stream that is expressed as the number of characters from the start of the text stream.</span></span> <span data-ttu-id="50c82-123">Dado que el modelo ACP es de base cero, el primer carácter de una secuencia de texto tiene un ACP de cero.</span><span class="sxs-lookup"><span data-stu-id="50c82-123">Because the ACP model is zero-based, the first character in a text stream has an ACP of zero.</span></span> <span data-ttu-id="50c82-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="50c82-124">For example:</span></span>


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



<span data-ttu-id="50c82-125">Un almacén de texto implementa un objeto que admite la interfaz [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , lo que permite expresar el flujo de texto en un ACP.</span><span class="sxs-lookup"><span data-stu-id="50c82-125">A text store implements an object that supports the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) interface, which enables the text stream to be expressed in an ACP.</span></span> <span data-ttu-id="50c82-126">Los métodos de interfaz **ITextStoreACP** usan el intervalo ACP de la secuencia de texto para modificar el texto.</span><span class="sxs-lookup"><span data-stu-id="50c82-126">The **ITextStoreACP** interface methods use the ACP range of the text stream to modify the text.</span></span>

## <a name="anchor-based-applications"></a><span data-ttu-id="50c82-127">Aplicaciones Anchor-Based</span><span class="sxs-lookup"><span data-stu-id="50c82-127">Anchor-Based Applications</span></span>

<span data-ttu-id="50c82-128">El administrador usa los métodos basados en ACP de forma nativa para manipular el texto.</span><span class="sxs-lookup"><span data-stu-id="50c82-128">The manager uses the ACP-based methods natively to manipulate text.</span></span> <span data-ttu-id="50c82-129">Sin embargo, un enfoque basado en anclaje está disponible para los clientes de [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) que admiten [delimitadores](ranges.md), por lo que el administrador usa los métodos [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) y [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) para encapsular los métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) y [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .</span><span class="sxs-lookup"><span data-stu-id="50c82-129">However, an anchor-based approach is available for [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) clients that support [anchors](ranges.md), whereby the manager uses [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) and [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) methods to wrap the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) methods.</span></span>

## <a name="document-access-control"></a><span data-ttu-id="50c82-130">Access Control de documento</span><span class="sxs-lookup"><span data-stu-id="50c82-130">Document Access Control</span></span>

<span data-ttu-id="50c82-131">El almacén de texto controla el acceso a la secuencia de texto mediante [bloqueos de documento](document-locks.md).</span><span class="sxs-lookup"><span data-stu-id="50c82-131">The text store controls access to the text stream by using [document locks](document-locks.md).</span></span> <span data-ttu-id="50c82-132">Para leer o modificar el almacén de texto, el administrador debe instalar primero un receptor de notificaciones que admita la interfaz [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) llamando al método [ITextStoreACP:: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) y pasando un puntero a un receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="50c82-132">To read or modify the text store, the manager must first install an advise sink that supports the [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) interface by calling the [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) method and passing a pointer to an advise sink.</span></span> <span data-ttu-id="50c82-133">El receptor de notificaciones permite al administrador obtener un bloqueo de documento en el almacén de texto y recibir notificaciones cuando el almacén de texto se modifica con otro elemento que no sea el administrador, como la entrada del usuario a través de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50c82-133">The advise sink enables the manager to obtain a document locks on the text store and receive notifications when the text store is modified by something other than the manager, such as user input through the application.</span></span> <span data-ttu-id="50c82-134">Los receptores de notificaciones se tratan más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="50c82-134">Advise sinks are discussed later in this topic.</span></span>

## <a name="how-to-initialize-the-text-store"></a><span data-ttu-id="50c82-135">Cómo inicializar el almacén de texto</span><span class="sxs-lookup"><span data-stu-id="50c82-135">How To Initialize the Text Store</span></span>

<span data-ttu-id="50c82-136">Una aplicación Inicializa un almacén de texto completando los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="50c82-136">An application initializes a text store by completing the following steps:</span></span>

1.  <span data-ttu-id="50c82-137">Cree un objeto de administrador de subprocesos basado en la interfaz [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) llamando a la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un puntero a un objeto de administrador de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="50c82-137">Create a thread manager object based on the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function with a pointer to a thread manager object.</span></span> <span data-ttu-id="50c82-138">El siguiente es un ejemplo de código de la implementación de un objeto de administrador de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="50c82-138">The following is a code example of implementing a thread manager object.</span></span>
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  <span data-ttu-id="50c82-139">Active el objeto de administrador de subprocesos llamando al método [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) .</span><span class="sxs-lookup"><span data-stu-id="50c82-139">Activate the thread manager object by calling the [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) method.</span></span> <span data-ttu-id="50c82-140">Este método proporciona un puntero a un [identificador de cliente](tfclientid.md) que se usa para crear un objeto de contexto.</span><span class="sxs-lookup"><span data-stu-id="50c82-140">This method supplies a pointer to a [client identifier](tfclientid.md) used to create a context object.</span></span> <span data-ttu-id="50c82-141">El administrador de subprocesos se usa para implementar un objeto de administrador de documentos.</span><span class="sxs-lookup"><span data-stu-id="50c82-141">The thread manager is used to implement a document manager object.</span></span>
3.  <span data-ttu-id="50c82-142">Cree un objeto de administrador de documentos basado en la interfaz [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) llamando al método [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) con un puntero al objeto de administrador de documentos.</span><span class="sxs-lookup"><span data-stu-id="50c82-142">Create a document manager object based on the [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) interface by calling the [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) method with a pointer to the document manager object.</span></span> <span data-ttu-id="50c82-143">El objeto de administrador de documentos se usa para implementar un objeto de contexto que es el almacén de texto.</span><span class="sxs-lookup"><span data-stu-id="50c82-143">The document manager object is used to implement a context object that is the text store.</span></span>
4.  <span data-ttu-id="50c82-144">Cree un objeto de contexto desde el administrador de documentos mediante una llamada al método [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) con el puntero al objeto de almacén de texto y un puntero al identificador de cliente para activar el administrador de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="50c82-144">Create a context object from the document manager by calling the [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) method with the pointer to the text store object and a pointer to the client identifier from activating the thread manager.</span></span> <span data-ttu-id="50c82-145">El siguiente es un ejemplo de cómo crear un objeto de contexto:</span><span class="sxs-lookup"><span data-stu-id="50c82-145">The following is an example of creating a context object:</span></span>
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  <span data-ttu-id="50c82-146">Inserte el objeto de contexto en la pila con el método [ITfDocumentMgr::P uscripción](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) .</span><span class="sxs-lookup"><span data-stu-id="50c82-146">Push the context object onto the stack with the [ITfDocumentMgr::Push](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) method.</span></span> <span data-ttu-id="50c82-147">El siguiente es un ejemplo de cómo insertar el objeto de contexto en la pila:</span><span class="sxs-lookup"><span data-stu-id="50c82-147">The following is an example of pushing the context object onto the stack:</span></span>
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a><span data-ttu-id="50c82-148">Cómo modificar el almacén de texto</span><span class="sxs-lookup"><span data-stu-id="50c82-148">How To Modify the Text Store</span></span>

<span data-ttu-id="50c82-149">El método **ITfDocumentMgr::P uscripción** llama a **ITextStoreACP:: AdviseSink** con un puntero a la interfaz del receptor de notificaciones para instalar un nuevo receptor de notificaciones o modificar un receptor de notificaciones existente.</span><span class="sxs-lookup"><span data-stu-id="50c82-149">The **ITfDocumentMgr::Push** method calls **ITextStoreACP::AdviseSink** with a pointer to the advise sink interface to install a new advise sink or modify an existing advise sink.</span></span> <span data-ttu-id="50c82-150">El receptor de notificaciones recibe notificaciones cuando el almacén de texto se modifica con otro elemento que no sea el administrador, como la entrada del usuario en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50c82-150">The advise sink receives notifications when the text store is modified by something other than the manager, such as user input to the application.</span></span> <span data-ttu-id="50c82-151">Las aplicaciones deben llamar al método [ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) cuando el método de entrada obtiene el foco.</span><span class="sxs-lookup"><span data-stu-id="50c82-151">Applications must call the [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) method when the input method obtains the focus.</span></span> <span data-ttu-id="50c82-152">Otras notificaciones del administrador de subprocesos se proporcionan mediante una llamada a los métodos de interfaz **ITextStoreACPSink** adecuados.</span><span class="sxs-lookup"><span data-stu-id="50c82-152">Other notifications to the thread manager are provided by calling to the appropriate **ITextStoreACPSink** interface methods.</span></span>

<span data-ttu-id="50c82-153">Sin embargo, las aplicaciones no deben llamar a los métodos de la interfaz **ITextStoreACPSink** en respuesta a los métodos de interfaz **ITextStoreACP** .</span><span class="sxs-lookup"><span data-stu-id="50c82-153">However, applications should not call the **ITextStoreACPSink** interface methods in response to **ITextStoreACP** interface methods.</span></span> <span data-ttu-id="50c82-154">Las aplicaciones solo deben llamar a los métodos de la interfaz **ITextStoreACPSink** cuando el almacén de texto se modifique con otro elemento que no sea el administrador.</span><span class="sxs-lookup"><span data-stu-id="50c82-154">Applications should only call **ITextStoreACPSink** interface methods when the text store is modified by something other than the manager.</span></span>

<span data-ttu-id="50c82-155">El contenido del almacén de texto se puede modificar con un estado de entrada temporal denominado [composición](compositions.md).</span><span class="sxs-lookup"><span data-stu-id="50c82-155">The contents of the text store can be modified with a temporary input state called a [composition](compositions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50c82-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50c82-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c82-157">Delimitadores</span><span class="sxs-lookup"><span data-stu-id="50c82-157">Anchors</span></span>](ranges.md)
</dt> <dt>

[<span data-ttu-id="50c82-158">Composiciones</span><span class="sxs-lookup"><span data-stu-id="50c82-158">Compositions</span></span>](compositions.md)
</dt> <dt>

[<span data-ttu-id="50c82-159">Bloqueos de documento</span><span class="sxs-lookup"><span data-stu-id="50c82-159">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="50c82-160">ITextStoreACPSink</span><span class="sxs-lookup"><span data-stu-id="50c82-160">ITextStoreACPSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[<span data-ttu-id="50c82-161">ITextStoreACP</span><span class="sxs-lookup"><span data-stu-id="50c82-161">ITextStoreACP</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="50c82-162">ITextStoreAnchor</span><span class="sxs-lookup"><span data-stu-id="50c82-162">ITextStoreAnchor</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[<span data-ttu-id="50c82-163">ITextStoreAnchorSink</span><span class="sxs-lookup"><span data-stu-id="50c82-163">ITextStoreAnchorSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[<span data-ttu-id="50c82-164">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="50c82-164">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="50c82-165">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="50c82-165">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="50c82-166">ITfThreadMgrEventSink::OnSetFocus</span><span class="sxs-lookup"><span data-stu-id="50c82-166">ITfThreadMgrEventSink::OnSetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[<span data-ttu-id="50c82-167">TfClientId</span><span class="sxs-lookup"><span data-stu-id="50c82-167">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="50c82-168">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="50c82-168">Microsoft Active Accessibility</span></span>](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 