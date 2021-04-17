---
description: La clase CAMThread es una clase abstracta para la administración de subprocesos de trabajo.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Clase CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670739"
---
# <a name="camthread-class"></a><span data-ttu-id="a91f6-103">Clase CAMThread</span><span class="sxs-lookup"><span data-stu-id="a91f6-103">CAMThread class</span></span>

<span data-ttu-id="a91f6-104">La `CAMThread` clase es una clase abstracta para la administración de subprocesos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a91f6-104">The `CAMThread` class is an abstract class for managing worker threads.</span></span>



| <span data-ttu-id="a91f6-105">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="a91f6-105">Protected Member Variables</span></span>                                 | <span data-ttu-id="a91f6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a91f6-106">Description</span></span>                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="a91f6-107">**m \_ hThread**</span><span class="sxs-lookup"><span data-stu-id="a91f6-107">**m\_hThread**</span></span>](camthread-m-hthread.md)                  | <span data-ttu-id="a91f6-108">Identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-108">Handle to the thread.</span></span>                                                        |
| <span data-ttu-id="a91f6-109">Variables de miembro público</span><span class="sxs-lookup"><span data-stu-id="a91f6-109">Public Member Variables</span></span>                                    | <span data-ttu-id="a91f6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a91f6-110">Description</span></span>                                                                  |
| [<span data-ttu-id="a91f6-111">**m \_ AccessLock**</span><span class="sxs-lookup"><span data-stu-id="a91f6-111">**m\_AccessLock**</span></span>](camthread-m-accesslock.md)            | <span data-ttu-id="a91f6-112">Sección crítica que bloquea el subproceso para que no tenga acceso a otros subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a91f6-112">Critical section that locks the thread from being accessed by other threads.</span></span> |
| [<span data-ttu-id="a91f6-113">**m \_ WorkerLock**</span><span class="sxs-lookup"><span data-stu-id="a91f6-113">**m\_WorkerLock**</span></span>](camthread-m-workerlock.md)            | <span data-ttu-id="a91f6-114">Sección crítica que bloquea los datos compartidos entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a91f6-114">Critical section that locks data shared among threads.</span></span>                       |
| <span data-ttu-id="a91f6-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="a91f6-115">Public Methods</span></span>                                             | <span data-ttu-id="a91f6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a91f6-116">Description</span></span>                                                                  |
| [<span data-ttu-id="a91f6-117">**CAMThread**</span><span class="sxs-lookup"><span data-stu-id="a91f6-117">**CAMThread**</span></span>](camthread-camthread.md)                   | <span data-ttu-id="a91f6-118">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="a91f6-118">Constructor method.</span></span>                                                          |
| [<span data-ttu-id="a91f6-119">**~ CAMThread**</span><span class="sxs-lookup"><span data-stu-id="a91f6-119">**~ CAMThread**</span></span>](camthread--camthread.md)                | <span data-ttu-id="a91f6-120">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="a91f6-120">Destructor method.</span></span> <span data-ttu-id="a91f6-121">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="a91f6-121">Virtual.</span></span>                                                  |
| [<span data-ttu-id="a91f6-122">**InitialThreadProc**</span><span class="sxs-lookup"><span data-stu-id="a91f6-122">**InitialThreadProc**</span></span>](camthread-initialthreadproc.md)   | <span data-ttu-id="a91f6-123">Llama al método ThreadProc cuando se crea el subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-123">Calls the ThreadProc method when the thread is created.</span></span>                      |
| [<span data-ttu-id="a91f6-124">**A**</span><span class="sxs-lookup"><span data-stu-id="a91f6-124">**Create**</span></span>](camthread-create.md)                         | <span data-ttu-id="a91f6-125">Crea el subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-125">Creates the thread.</span></span>                                                          |
| [<span data-ttu-id="a91f6-126">**CallWorker**</span><span class="sxs-lookup"><span data-stu-id="a91f6-126">**CallWorker**</span></span>](camthread-callworker.md)                 | <span data-ttu-id="a91f6-127">Señala el subproceso con una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a91f6-127">Signals the thread with a request.</span></span>                                           |
| [<span data-ttu-id="a91f6-128">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="a91f6-128">**Close**</span></span>](camthread-close.md)                           | <span data-ttu-id="a91f6-129">Espera a que se cierre el subproceso y, a continuación, libera sus recursos.</span><span class="sxs-lookup"><span data-stu-id="a91f6-129">Waits for the thread to exit, then releases its resources.</span></span>                   |
| [<span data-ttu-id="a91f6-130">**ThreadExists**</span><span class="sxs-lookup"><span data-stu-id="a91f6-130">**ThreadExists**</span></span>](camthread-threadexists.md)             | <span data-ttu-id="a91f6-131">Consulta si el subproceso existe.</span><span class="sxs-lookup"><span data-stu-id="a91f6-131">Queries whether the thread exists.</span></span>                                           |
| [<span data-ttu-id="a91f6-132">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="a91f6-132">**GetRequest**</span></span>](camthread-getrequest.md)                 | <span data-ttu-id="a91f6-133">Espera la siguiente solicitud.</span><span class="sxs-lookup"><span data-stu-id="a91f6-133">Waits for the next request.</span></span>                                                  |
| [<span data-ttu-id="a91f6-134">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="a91f6-134">**CheckRequest**</span></span>](camthread-checkrequest.md)             | <span data-ttu-id="a91f6-135">Comprueba si hay una solicitud, sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="a91f6-135">Checks if there is a request, without blocking.</span></span>                              |
| [<span data-ttu-id="a91f6-136">**Responder**</span><span class="sxs-lookup"><span data-stu-id="a91f6-136">**Reply**</span></span>](camthread-reply.md)                           | <span data-ttu-id="a91f6-137">Responde a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a91f6-137">Replies to a request.</span></span>                                                        |
| [<span data-ttu-id="a91f6-138">**GetRequestHandle**</span><span class="sxs-lookup"><span data-stu-id="a91f6-138">**GetRequestHandle**</span></span>](camthread-getrequesthandle.md)     | <span data-ttu-id="a91f6-139">Recupera un identificador para el evento señalado por el método CallWorker.</span><span class="sxs-lookup"><span data-stu-id="a91f6-139">Retrieves a handle to the event signaled by the CallWorker method.</span></span>           |
| [<span data-ttu-id="a91f6-140">**GetRequestParam**</span><span class="sxs-lookup"><span data-stu-id="a91f6-140">**GetRequestParam**</span></span>](camthread-getrequestparam.md)       | <span data-ttu-id="a91f6-141">Recupera la solicitud más reciente.</span><span class="sxs-lookup"><span data-stu-id="a91f6-141">Retrieves the latest request.</span></span>                                                |
| [<span data-ttu-id="a91f6-142">**CoInitializeHelper**</span><span class="sxs-lookup"><span data-stu-id="a91f6-142">**CoInitializeHelper**</span></span>](camthread-coinitializehelper.md) | <span data-ttu-id="a91f6-143">Llama a CoInitializeEx al inicio del subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-143">Calls CoInitializeEx at the start of the thread.</span></span>                             |
| <span data-ttu-id="a91f6-144">Métodos virtuales puros</span><span class="sxs-lookup"><span data-stu-id="a91f6-144">Pure Virtual Methods</span></span>                                       | <span data-ttu-id="a91f6-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="a91f6-145">Description</span></span>                                                                  |
| [<span data-ttu-id="a91f6-146">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="a91f6-146">**ThreadProc**</span></span>](camthread-threadproc.md)                 | <span data-ttu-id="a91f6-147">Procedimiento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-147">Thread procedure.</span></span>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="a91f6-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a91f6-148">Remarks</span></span>

<span data-ttu-id="a91f6-149">Esta clase proporciona métodos para crear un subproceso de trabajo, pasar solicitudes al subproceso y esperar a que el subproceso salga.</span><span class="sxs-lookup"><span data-stu-id="a91f6-149">This class provides methods for creating a worker thread, passing requests to the thread, and waiting for the thread to exit.</span></span> <span data-ttu-id="a91f6-150">Para usar esta clase, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a91f6-150">To use this class, do the following:</span></span>

-   <span data-ttu-id="a91f6-151">Derive una clase de `CAMThread` e invalide el método virtual puro [**CAMThread:: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="a91f6-151">Derive a class from `CAMThread` and override the pure virtual method [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="a91f6-152">Este método es el procedimiento de subproceso al que se llama al principio del subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-152">This method is the thread procedure that gets called at the start of the thread.</span></span>
-   <span data-ttu-id="a91f6-153">En la aplicación, cree una instancia de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="a91f6-153">In your application, create an instance of your derived class.</span></span> <span data-ttu-id="a91f6-154">Al crear el objeto, no se crea el subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-154">Creating the object does not create the thread.</span></span> <span data-ttu-id="a91f6-155">Para crear el subproceso, llame al método [**CAMThread:: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="a91f6-155">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>
-   <span data-ttu-id="a91f6-156">Para enviar solicitudes al subproceso, llame al método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="a91f6-156">To send requests to the thread, call the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="a91f6-157">Este método toma un parámetro DWORD, cuyo significado está definido por la clase.</span><span class="sxs-lookup"><span data-stu-id="a91f6-157">This method takes a DWORD parameter, whose meaning is defined by your class.</span></span> <span data-ttu-id="a91f6-158">El método se bloquea hasta que el subproceso responde (consulte a continuación).</span><span class="sxs-lookup"><span data-stu-id="a91f6-158">The method blocks until the thread responds (see below).</span></span>
-   <span data-ttu-id="a91f6-159">En el procedimiento de subproceso, responda a las solicitudes llamando a [**CAMThread:: GetRequest**](camthread-getrequest.md) o [**CAMThread:: CheckRequest**](camthread-checkrequest.md).</span><span class="sxs-lookup"><span data-stu-id="a91f6-159">In your thread procedure, respond to requests by calling either [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md).</span></span> <span data-ttu-id="a91f6-160">El método GetRequest se bloquea hasta que otro subproceso llama a CallWorker.</span><span class="sxs-lookup"><span data-stu-id="a91f6-160">The GetRequest method blocks until another thread calls CallWorker.</span></span> <span data-ttu-id="a91f6-161">El método CheckRequest no es de bloqueo, lo que permite al subproceso comprobar si hay nuevas solicitudes mientras se trabaja de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a91f6-161">The CheckRequest method is non-blocking, which enables the thread to check for new requests while working asynchronously.</span></span>
-   <span data-ttu-id="a91f6-162">Cuando el subproceso recibe una solicitud, llame a [**CAMThread:: reply**](camthread-reply.md) para desbloquear el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="a91f6-162">When the thread receives a request, call [**CAMThread::Reply**](camthread-reply.md) to unblock the calling thread.</span></span> <span data-ttu-id="a91f6-163">El método reply toma un parámetro DWORD, que se pasa al subproceso que realiza la llamada como el valor devuelto para CallWorker.</span><span class="sxs-lookup"><span data-stu-id="a91f6-163">The Reply method takes a DWORD parameter, which is passed to the calling thread as the return value for CallWorker.</span></span>

<span data-ttu-id="a91f6-164">Cuando haya terminado con el subproceso, llame al método [**CAMThread:: Close**](camthread-close.md) .</span><span class="sxs-lookup"><span data-stu-id="a91f6-164">When you are done with the thread, call the [**CAMThread::Close**](camthread-close.md) method.</span></span> <span data-ttu-id="a91f6-165">Este método espera a que se cierre el subproceso y, a continuación, cierra el identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-165">This method waits for the thread to exit, and then closes the thread handle.</span></span> <span data-ttu-id="a91f6-166">Se debe garantizar que el mensaje ThreadProc se cierre, ya sea por sí mismo o en respuesta a una solicitud CallWorker.</span><span class="sxs-lookup"><span data-stu-id="a91f6-166">Your ThreadProc message must be guaranteed to exit, either on its own or in response to a CallWorker request.</span></span> <span data-ttu-id="a91f6-167">El método de destructor también llama a Close.</span><span class="sxs-lookup"><span data-stu-id="a91f6-167">The destructor method also calls Close.</span></span>

<span data-ttu-id="a91f6-168">En el ejemplo siguiente se muestran estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a91f6-168">The following example illustrates these steps:</span></span>


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



<span data-ttu-id="a91f6-169">En la clase derivada, también puede definir funciones miembro que validan los parámetros en CallWorker.</span><span class="sxs-lookup"><span data-stu-id="a91f6-169">In your derived class, you can also define member functions that validate the parameters to CallWorker.</span></span> <span data-ttu-id="a91f6-170">En el ejemplo siguiente se muestra una forma típica de hacerlo:</span><span class="sxs-lookup"><span data-stu-id="a91f6-170">The following example shows a typical way to do this:</span></span>


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



<span data-ttu-id="a91f6-171">La `CAMThread` clase proporciona dos secciones críticas como variables de miembro público.</span><span class="sxs-lookup"><span data-stu-id="a91f6-171">The `CAMThread` class provides two critical sections as public member variables.</span></span> <span data-ttu-id="a91f6-172">Use `CAMThread::m_AccessLock` para impedir que otros subprocesos accedan al subproceso.</span><span class="sxs-lookup"><span data-stu-id="a91f6-172">Use `CAMThread::m_AccessLock` to lock the thread from being accessed by other threads.</span></span> <span data-ttu-id="a91f6-173">(Por ejemplo, los métodos Create y CallWorker contienen este bloqueo para serializar las operaciones en el subproceso). Use [**CAMThread:: m \_ WorkerLock**](camthread-m-workerlock.md) para bloquear los datos que se comparten entre los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a91f6-173">(For example, the Create and CallWorker methods hold this lock, to serialize operations on the thread.) Use [**CAMThread::m\_WorkerLock**](camthread-m-workerlock.md) to lock data that is shared among threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="a91f6-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a91f6-174">Requirements</span></span>



| <span data-ttu-id="a91f6-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="a91f6-175">Requirement</span></span> | <span data-ttu-id="a91f6-176">Value</span><span class="sxs-lookup"><span data-stu-id="a91f6-176">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a91f6-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a91f6-177">Header</span></span><br/>  | <dl> <span data-ttu-id="a91f6-178"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a91f6-178"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a91f6-179">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a91f6-179">Library</span></span><br/> | <dl> <span data-ttu-id="a91f6-180"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a91f6-180"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




