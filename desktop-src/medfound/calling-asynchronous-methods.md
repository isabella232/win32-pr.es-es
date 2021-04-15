---
description: Llamar a métodos asincrónicos
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Llamar a métodos asincrónicos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539634"
---
# <a name="calling-asynchronous-methods"></a><span data-ttu-id="628a9-103">Llamar a métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="628a9-103">Calling Asynchronous Methods</span></span>

<span data-ttu-id="628a9-104">En Media Foundation, muchas operaciones se realizan de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="628a9-104">In Media Foundation, many operations are performed asynchronously.</span></span> <span data-ttu-id="628a9-105">Las operaciones asincrónicas pueden mejorar el rendimiento, ya que no bloquean el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="628a9-105">Asynchronous operations can improve performance, because they do not block the calling thread.</span></span> <span data-ttu-id="628a9-106">Una operación asincrónica en Media Foundation se define mediante un par de métodos con la Convención de nomenclatura **Begin...** y **End....**.</span><span class="sxs-lookup"><span data-stu-id="628a9-106">An asynchronous operation in Media Foundation is defined by a pair of methods with the naming convention **Begin...** and **End....**.</span></span> <span data-ttu-id="628a9-107">Juntos, estos dos métodos definen una operación de lectura asincrónica en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="628a9-107">Together, these two methods define an asynchronous read operation on the stream.</span></span>

<span data-ttu-id="628a9-108">Para iniciar una operación asincrónica, llame al método **Begin** .</span><span class="sxs-lookup"><span data-stu-id="628a9-108">To start an asynchronous operation, call the **Begin** method.</span></span> <span data-ttu-id="628a9-109">El método **Begin** siempre contiene al menos dos parámetros:</span><span class="sxs-lookup"><span data-stu-id="628a9-109">The **Begin** method always contains at least two parameters:</span></span>

-   <span data-ttu-id="628a9-110">Puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="628a9-110">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="628a9-111">La aplicación debe implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="628a9-111">The application must implement this interface.</span></span>
-   <span data-ttu-id="628a9-112">Un puntero a un objeto de estado opcional.</span><span class="sxs-lookup"><span data-stu-id="628a9-112">A pointer to an optional state object.</span></span>

<span data-ttu-id="628a9-113">La interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) notifica a la aplicación cuando se completa la operación.</span><span class="sxs-lookup"><span data-stu-id="628a9-113">The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface notifies the application when the operation is completed.</span></span> <span data-ttu-id="628a9-114">Para obtener un ejemplo de cómo implementar esta interfaz, vea [implementación de la devolución de llamada asincrónica](implementing-the-asynchronous-callback.md).</span><span class="sxs-lookup"><span data-stu-id="628a9-114">For an example of how to implement this interface, see [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md).</span></span> <span data-ttu-id="628a9-115">El objeto de estado es opcional.</span><span class="sxs-lookup"><span data-stu-id="628a9-115">The state object is optional.</span></span> <span data-ttu-id="628a9-116">Si se especifica, debe implementar la interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="628a9-116">If specified, it must implement the **IUnknown** interface.</span></span> <span data-ttu-id="628a9-117">Puede usar el objeto de estado para almacenar cualquier información de estado que sea necesaria para la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="628a9-117">You can use the state object to store any state information that is needed by your callback.</span></span> <span data-ttu-id="628a9-118">Si no necesita información de estado, puede establecer este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="628a9-118">If you do not need state information, you can set this parameter to **NULL**.</span></span> <span data-ttu-id="628a9-119">El método **Begin** podría contener parámetros adicionales que son específicos de ese método.</span><span class="sxs-lookup"><span data-stu-id="628a9-119">The **Begin** method might contain additional parameters that are specific to that method.</span></span>

<span data-ttu-id="628a9-120">Si el método **Begin** devuelve un código de error, significa que la operación ha generado un error inmediatamente y no se invocará la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="628a9-120">If the **Begin** method returns a failure code, it means the operation has failed immediately, and the callback will not be invoked.</span></span> <span data-ttu-id="628a9-121">Si el método **Begin** se realiza correctamente, significa que la operación está pendiente y se invocará la devolución de llamada cuando se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="628a9-121">If the **Begin** method succeeds, it means the operation is pending, and the callback will be invoked when the operation completes.</span></span>

<span data-ttu-id="628a9-122">Por ejemplo, el método [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) inicia una operación de lectura asincrónica en una secuencia de bytes:</span><span class="sxs-lookup"><span data-stu-id="628a9-122">For example, the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) method starts an asynchronous read operation on a byte stream:</span></span>


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



<span data-ttu-id="628a9-123">El método de devolución de llamada es [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="628a9-123">The callback method is [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="628a9-124">Tiene un único parámetro, *pAsyncResult*, que es un puntero a la interfaz [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="628a9-124">It has a single parameter, *pAsyncResult*, which is a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="628a9-125">Para completar la operación asincrónica, llame al método **End** que coincida con el método **Begin** asincrónico.</span><span class="sxs-lookup"><span data-stu-id="628a9-125">To complete the asynchronous operation, call the **End** method that matches the asynchronous **Begin** method.</span></span> <span data-ttu-id="628a9-126">El método **End** siempre toma un puntero **IMFAsyncResult** .</span><span class="sxs-lookup"><span data-stu-id="628a9-126">The **End** method always takes an **IMFAsyncResult** pointer.</span></span> <span data-ttu-id="628a9-127">Pase siempre el mismo puntero que recibió en el método **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="628a9-127">Always pass in the same pointer that you received in the **Invoke** method.</span></span> <span data-ttu-id="628a9-128">La operación asincrónica no se completa hasta que se llama al método **End** .</span><span class="sxs-lookup"><span data-stu-id="628a9-128">The asynchronous operation is not complete until you call the **End** method.</span></span> <span data-ttu-id="628a9-129">Puede llamar al método **End** desde dentro del método **Invoke** o puede llamarlo desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="628a9-129">You may call the **End** method from inside the **Invoke** method, or you can call it from another thread.</span></span>

<span data-ttu-id="628a9-130">Por ejemplo, para completar [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) en una secuencia de bytes, llame a [**IMFByteStream:: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span><span class="sxs-lookup"><span data-stu-id="628a9-130">For example, to complete the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) on a byte stream, call [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span></span>


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



<span data-ttu-id="628a9-131">El valor devuelto del método **End** indica el estado de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="628a9-131">The return value of the **End** method indicates the status of the asynchronous operation.</span></span> <span data-ttu-id="628a9-132">En la mayoría de los casos, la aplicación realizará algún trabajo después de que se complete la operación asincrónica, tanto si se completa correctamente como si no.</span><span class="sxs-lookup"><span data-stu-id="628a9-132">In most cases, your application will perform some work after the asynchronous operation completes, whether it completes successfully or not.</span></span> <span data-ttu-id="628a9-133">Tiene varias opciones:</span><span class="sxs-lookup"><span data-stu-id="628a9-133">You have several options:</span></span>

-   <span data-ttu-id="628a9-134">Realice el trabajo en el método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="628a9-134">Do the work inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="628a9-135">Este enfoque es aceptable siempre y cuando la aplicación no bloquee nunca el subproceso que realiza la llamada o espere a que se encuentre todo en el método **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="628a9-135">This approach is acceptable as long as your application never blocks the calling thread or waits for anything inside the **Invoke** method.</span></span> <span data-ttu-id="628a9-136">Si bloquea el subproceso que realiza la llamada, podría bloquear la canalización de streaming.</span><span class="sxs-lookup"><span data-stu-id="628a9-136">If you block the calling thread, you might block the streaming pipeline.</span></span> <span data-ttu-id="628a9-137">Por ejemplo, puede actualizar algunas variables de estado, pero no realizar una operación de lectura sincrónica ni esperar en un objeto de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="628a9-137">For example, you might update some state variables, but do not perform a synchronous read operation or wait on a mutex object.</span></span>
-   <span data-ttu-id="628a9-138">En el método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , establezca un evento y vuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="628a9-138">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, set an event and return immediately.</span></span> <span data-ttu-id="628a9-139">El subproceso de llamada de la aplicación espera el evento y realiza el trabajo cuando se señala el evento.</span><span class="sxs-lookup"><span data-stu-id="628a9-139">The application's calling thread waits for the event and does the work when the event is signaled.</span></span>
-   <span data-ttu-id="628a9-140">En el método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , publique un mensaje de ventana privada en la ventana de la aplicación y vuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="628a9-140">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, post a private window message to your application window and return immediately.</span></span> <span data-ttu-id="628a9-141">La aplicación realiza el trabajo en su bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="628a9-141">The application does the work on its message loop.</span></span> <span data-ttu-id="628a9-142">(Asegúrese de publicar el mensaje mediante una llamada a **PostMessage**, no **SendMessage**, porque **SendMessage** puede bloquear el subproceso de devolución de llamada).</span><span class="sxs-lookup"><span data-stu-id="628a9-142">(Make sure to post the message by calling **PostMessage**, not **SendMessage**, because **SendMessage** can block the callback thread.)</span></span>

<span data-ttu-id="628a9-143">Es importante recordar que se llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="628a9-143">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from another thread.</span></span> <span data-ttu-id="628a9-144">La aplicación es responsable de garantizar que cualquier trabajo realizado dentro de **Invoke** sea seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="628a9-144">Your application is responsible for ensuring that any work performed inside **Invoke** is thread-safe.</span></span>

<span data-ttu-id="628a9-145">De forma predeterminada, el subproceso que llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) no realiza suposiciones sobre el comportamiento del objeto de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="628a9-145">By default, the thread that calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) makes no assumptions about the behavior of your callback object.</span></span> <span data-ttu-id="628a9-146">Opcionalmente, puede implementar el método [**IMFAsyncCallback:: GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) para devolver información sobre la implementación de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="628a9-146">Optionally, you can implement the [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) method to return information about your callback implementation.</span></span> <span data-ttu-id="628a9-147">De lo contrario, este método puede devolver **E \_ NOTIMPL**:</span><span class="sxs-lookup"><span data-stu-id="628a9-147">Otherwise, this method can return **E\_NOTIMPL**:</span></span>


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



<span data-ttu-id="628a9-148">Si especificó un objeto de estado en el método **Begin** , puede recuperarlo desde dentro del método de devolución de llamada llamando a [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="628a9-148">If you specified a state object in the **Begin** method, you can retrieve it from inside your callback method by calling [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>

## <a name="related-topics"></a><span data-ttu-id="628a9-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="628a9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="628a9-150">Métodos de devolución de llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="628a9-150">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



