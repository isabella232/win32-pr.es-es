---
description: En este tema se describe cómo implementar un método asincrónico en Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Escribir un método asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361246"
---
# <a name="writing-an-asynchronous-method"></a><span data-ttu-id="6a8e9-103">Escribir un método asincrónico</span><span class="sxs-lookup"><span data-stu-id="6a8e9-103">Writing an Asynchronous Method</span></span>

<span data-ttu-id="6a8e9-104">En este tema se describe cómo implementar un método asincrónico en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-104">This topic describes how to implement an asynchronous method in Microsoft Media Foundation.</span></span>

<span data-ttu-id="6a8e9-105">Los métodos asincrónicos están omnipresentes en la canalización de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-105">Asynchronous methods are ubiquitous in the Media Foundation pipeline.</span></span> <span data-ttu-id="6a8e9-106">Los métodos asincrónicos facilitan la distribución del trabajo entre varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-106">Asynchronous methods make it easier to distribute work among several threads.</span></span> <span data-ttu-id="6a8e9-107">Es especialmente importante realizar la e/s asincrónicamente, de modo que la lectura de un archivo o red no bloquee el resto de la canalización.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-107">It is particularly important to perform I/O asynchronously, so that reading from a file or network does not block the rest of the pipeline.</span></span>

<span data-ttu-id="6a8e9-108">Si está escribiendo un origen multimedia o un receptor multimedia, es fundamental controlar las operaciones asincrónicas correctamente, ya que el rendimiento del componente afecta a toda la canalización.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-108">If you are writing a media source or media sink, it is crucial to handle asynchronous operations correctly, because your component's performance has an impact on the entire pipeline.</span></span>

> [!Note]  
> <span data-ttu-id="6a8e9-109">De forma predeterminada, las transformaciones de Media Foundation (MFTs) usan métodos sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-109">Media Foundation transforms (MFTs) use synchronous methods by default.</span></span>

 

### <a name="work-queues-for-asynchronous-operations"></a><span data-ttu-id="6a8e9-110">Colas de trabajo para operaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="6a8e9-110">Work Queues For Asynchronous Operations</span></span>

<span data-ttu-id="6a8e9-111">En Media Foundation, hay una relación de cierre entre [los métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md) y las [colas de trabajos](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-111">In Media Foundation, there is a close relationship between [Asynchronous Callback Methods](asynchronous-callback-methods.md) and [Work Queues](work-queues.md).</span></span> <span data-ttu-id="6a8e9-112">Una cola de trabajo es una abstracción para mover el trabajo del subproceso del llamador a un subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-112">A work queue is an abstraction for moving work from the caller's thread to a worker thread.</span></span> <span data-ttu-id="6a8e9-113">Para realizar el trabajo en una cola de trabajo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-113">To perform work on a work queue, do the following:</span></span>

1.  <span data-ttu-id="6a8e9-114">Implemente la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-114">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="6a8e9-115">Llame a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear un objeto de *resultado* .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-115">Call [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a *result* object.</span></span> <span data-ttu-id="6a8e9-116">El objeto de resultado expone [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-116">The result object exposes the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span></span> <span data-ttu-id="6a8e9-117">El objeto de resultado contiene tres punteros:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-117">The result object contains three pointers:</span></span>

    -   <span data-ttu-id="6a8e9-118">Puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del llamador.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-118">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="6a8e9-119">Un puntero opcional a un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-119">An optional pointer to a state object.</span></span> <span data-ttu-id="6a8e9-120">Si se especifica, el objeto de Estado debe implementar **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-120">If specified, the state object must implement **IUnknown**.</span></span>
    -   <span data-ttu-id="6a8e9-121">Un puntero opcional a un objeto privado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-121">An optional pointer to a private object.</span></span> <span data-ttu-id="6a8e9-122">Si se especifica, este objeto también debe implementar **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-122">If specified, this object also must implement **IUnknown**.</span></span>

    <span data-ttu-id="6a8e9-123">Los dos últimos punteros pueden ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-123">The last two pointers can be **NULL**.</span></span> <span data-ttu-id="6a8e9-124">En caso contrario, úselos para almacenar información sobre la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-124">Otherwise, use them to hold information about the asynchronous operation.</span></span>

3.  <span data-ttu-id="6a8e9-125">Llame a [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para poner en cola el elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-125">Call [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue to the work item.</span></span>
4.  <span data-ttu-id="6a8e9-126">El subproceso de cola de trabajo llama al método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-126">The work-queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
5.  <span data-ttu-id="6a8e9-127">Realice el trabajo en el método de [**invocación**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-127">Do the work inside your [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="6a8e9-128">El parámetro *pAsyncResult* de este método es el puntero [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) del paso 2.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-128">The *pAsyncResult* parameter of this method is the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointer from step 2.</span></span> <span data-ttu-id="6a8e9-129">Use este puntero para obtener el objeto de estado y el objeto privado:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-129">Use this pointer to get the state object and private object:</span></span>
    -   <span data-ttu-id="6a8e9-130">Para obtener el objeto de estado, llame a [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-130">To get the state object, call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>
    -   <span data-ttu-id="6a8e9-131">Para obtener el objeto privado, llame a [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-131">To get the private object, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span></span>

<span data-ttu-id="6a8e9-132">Como alternativa, puede combinar los pasos 2 y 3 llamando a la función [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-132">As an alternative, you can combine steps 2 and 3 by calling the [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) function.</span></span> <span data-ttu-id="6a8e9-133">Internamente, esta función llama a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear el objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-133">Internally, this function calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create the result object.</span></span>

<span data-ttu-id="6a8e9-134">En el diagrama siguiente se muestran las relaciones entre el autor de la llamada, el objeto de resultado, el objeto de estado y el objeto privado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-134">The following diagram shows the relationships between the caller, the result object, the state object, and the private object.</span></span>

![diagrama que muestra un objeto de resultado asincrónico](images/workqueues01.png)

<span data-ttu-id="6a8e9-136">En el diagrama de secuencia siguiente se muestra cómo un objeto pone en cola un elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-136">The following sequence diagram shows how an object queues a work item.</span></span> <span data-ttu-id="6a8e9-137">Cuando el subproceso de cola de trabajo llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), el objeto realiza la operación asincrónica en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-137">When the work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), the object performs the asynchronous operation on that thread.</span></span>

![diagrama que muestra cómo un objeto pone en cola un elemento de trabajo](images/workqueues02.png)

<span data-ttu-id="6a8e9-139">Es importante recordar que se llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) desde un subproceso que pertenece a la cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-139">It is important to remember [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from a thread that is owned by the work queue.</span></span> <span data-ttu-id="6a8e9-140">La implementación de **Invoke** debe ser segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-140">Your implementation of **Invoke** must be thread safe.</span></span> <span data-ttu-id="6a8e9-141">Además, si usa la cola de trabajo de plataforma (**\_ estándar de \_ cola \_ de devolución de llamada de MFASYNC**), es fundamental que nunca bloquee el subproceso, ya que esto puede impedir que la canalización de Media Foundation completa procese los datos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-141">In addition, if you use the platform work queue (**MFASYNC\_CALLBACK\_QUEUE\_STANDARD**), it is critical that you never block the thread, because that can block the entire Media Foundation pipeline from processing data.</span></span> <span data-ttu-id="6a8e9-142">Si necesita realizar una operación que se bloqueará o tardará mucho tiempo en completarse, utilice una cola de trabajo privada.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-142">If you need to perform an operation that will block or take a long time to complete, use a private work queue.</span></span> <span data-ttu-id="6a8e9-143">Para crear una cola de trabajo privada, llame a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-143">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="6a8e9-144">Cualquier componente de canalización que realice operaciones de e/s debe evitar el bloqueo de las llamadas de e/s por el mismo motivo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-144">Any pipeline component that performs I/O operations should avoid blocking I/O calls for the same reason.</span></span> <span data-ttu-id="6a8e9-145">La interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) proporciona una abstracción útil para la e/s asincrónica de archivos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-145">The [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface provides a useful abstraction for asynchronous file I/O.</span></span>

### <a name="implementing-the-beginend-pattern"></a><span data-ttu-id="6a8e9-146">Implementar el ../end... Begin. Ajedrez</span><span class="sxs-lookup"><span data-stu-id="6a8e9-146">Implementing the Begin.../End... Pattern</span></span>

<span data-ttu-id="6a8e9-147">Como se describe en [llamar a métodos asincrónicos](calling-asynchronous-methods.md), los métodos asincrónicos de Media Foundation suelen usar la instrucción **Begin...** / **Finalizar.** ... ajedrez.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-147">As described in [Calling Asynchronous Methods](calling-asynchronous-methods.md), asynchronous methods in Media Foundation often use the **Begin...**/**End....** pattern.</span></span> <span data-ttu-id="6a8e9-148">En este patrón, una operación asincrónica utiliza dos métodos con firmas similares a las siguientes:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-148">In this pattern, an asynchronous operation uses two methods with signatures similar to the following:</span></span>

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

<span data-ttu-id="6a8e9-149">Para que el método sea realmente asincrónico, la implementación de **BeginX** debe realizar el trabajo real en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-149">To make the method truly asynchronous, the implementation of **BeginX** must perform the actual work on another thread.</span></span> <span data-ttu-id="6a8e9-150">Aquí es donde entran en la imagen las colas de trabajos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-150">This is where work queues come into the picture.</span></span> <span data-ttu-id="6a8e9-151">En los pasos siguientes, el autor de la *llamada* es el código que llama a **BeginX** y **EndX**.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-151">In the steps that follow, the *caller* is the code that calls **BeginX** and **EndX**.</span></span> <span data-ttu-id="6a8e9-152">Puede tratarse de una aplicación o de la canalización Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-152">This might be an application or the Media Foundation pipeline.</span></span> <span data-ttu-id="6a8e9-153">El *componente* es el código que implementa **BeginX** y **EndX**.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-153">The *component* is the code that implements **BeginX** and **EndX**.</span></span>

1.  <span data-ttu-id="6a8e9-154">El llamador llama a **Begin...**, pasando un puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del llamador.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-154">The caller calls **Begin...**, passing in a pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="6a8e9-155">El componente crea un nuevo objeto de resultado asincrónico.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-155">The component creates a new asynchronous result object.</span></span> <span data-ttu-id="6a8e9-156">Este objeto almacena la interfaz de devolución de llamada y el objeto de estado del llamador.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-156">This object stores the caller's callback interface and state object.</span></span> <span data-ttu-id="6a8e9-157">Normalmente, también almacena información de estado privado que el componente necesita para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-157">Typically, it also stores any private state information that the component needs to complete the operation.</span></span> <span data-ttu-id="6a8e9-158">El objeto de resultado de este paso tiene la etiqueta "resultado 1" en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-158">The result object from this step is labeled "Result 1" in the next diagram.</span></span>
3.  <span data-ttu-id="6a8e9-159">El componente crea un segundo objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-159">The component creates a second result object.</span></span> <span data-ttu-id="6a8e9-160">Este objeto de resultado almacena dos punteros: el primer objeto de resultado y la interfaz de devolución de llamada del destinatario.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-160">This result object stores two pointers: The first result object, and the callback interface of the callee.</span></span> <span data-ttu-id="6a8e9-161">Este objeto de resultado tiene la etiqueta "resultado 2" en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-161">This result object is labeled "Result 2" in the next diagram.</span></span>
4.  <span data-ttu-id="6a8e9-162">El componente llama a [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para poner en cola un nuevo elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-162">The component calls [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue a new work item.</span></span>
5.  <span data-ttu-id="6a8e9-163">En el método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , el componente realiza el trabajo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-163">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the component does the asynchronous work.</span></span>
6.  <span data-ttu-id="6a8e9-164">El componente llama a [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar el método de devolución de llamada del llamador.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-164">The component calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>
7.  <span data-ttu-id="6a8e9-165">El llamador llama al método **EndX** .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-165">The caller calls the **EndX** method.</span></span>

![diagrama que muestra cómo un objeto implementa el patrón Begin/end](images/workqueues03.png)

## <a name="asynchronous-method-example"></a><span data-ttu-id="6a8e9-167">Ejemplo de método asincrónico</span><span class="sxs-lookup"><span data-stu-id="6a8e9-167">Asynchronous Method Example</span></span>

<span data-ttu-id="6a8e9-168">Para ilustrar este debate, usaremos un ejemplo de inventado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-168">To illustrate this discussion, we will use a contrived example.</span></span> <span data-ttu-id="6a8e9-169">Considere un método asincrónico para calcular una raíz cuadrada:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-169">Consider an asynchronous method for computing a square root:</span></span>


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



<span data-ttu-id="6a8e9-170">El parámetro *x* de `BeginSquareRoot` es el valor cuya raíz cuadrada se va a calcular.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-170">The *x* parameter of `BeginSquareRoot` is the value whose square root will be calculated.</span></span> <span data-ttu-id="6a8e9-171">La raíz cuadrada se devuelve en el parámetro *pval* de `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-171">The square root is returned in the *pVal* parameter of `EndSquareRoot`.</span></span>

<span data-ttu-id="6a8e9-172">Esta es la declaración de una clase que implementa estos dos métodos:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-172">Here is the declaration of a class that implements these two methods:</span></span>


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="6a8e9-173">La `SqrRoot` clase implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) para que pueda colocar la operación de raíz cuadrada en una cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-173">The `SqrRoot` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) so that it can put the square root operation on a work queue.</span></span> <span data-ttu-id="6a8e9-174">El `DoCalculateSquareRoot` método es el método de clase privada que calcula la raíz cuadrada.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-174">The `DoCalculateSquareRoot` method is the private class method that calculates the square root.</span></span> <span data-ttu-id="6a8e9-175">Se llamará a este método desde el subproceso de cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-175">This method will be called from the work queue thread.</span></span>

<span data-ttu-id="6a8e9-176">En primer lugar, necesitamos una manera de almacenar el valor de *x*, de modo que se pueda recuperar cuando el subproceso de cola de trabajo llame a `SqrRoot::Invoke` .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-176">First, we need a way to store the value of *x*, so that it can be retrieved when the work queue thread calls `SqrRoot::Invoke`.</span></span> <span data-ttu-id="6a8e9-177">A continuación se muestra una clase simple que almacena la información:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-177">Here is a simple class that stores the information:</span></span>


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="6a8e9-178">Esta clase implementa **IUnknown** para que se pueda almacenar en un objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-178">This class implements **IUnknown** so that it can be stored in a result object.</span></span>

<span data-ttu-id="6a8e9-179">El código siguiente implementa el `BeginSquareRoot` método:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-179">The following code implements the `BeginSquareRoot` method:</span></span>


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



<span data-ttu-id="6a8e9-180">Este código hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-180">This code does the following:</span></span>

1.  <span data-ttu-id="6a8e9-181">Crea una nueva instancia de la `AsyncOp` clase para contener el valor de *x*.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-181">Creates a new instance of the `AsyncOp` class to hold the value of *x*.</span></span>
2.  <span data-ttu-id="6a8e9-182">Llama a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear un objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-182">Calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a result object.</span></span> <span data-ttu-id="6a8e9-183">Este objeto contiene varios punteros:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-183">This object holds several pointers:</span></span>
    -   <span data-ttu-id="6a8e9-184">Puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del llamador.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-184">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="6a8e9-185">Puntero al objeto de estado del llamador (*pState*).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-185">A pointer to the caller's state object (*pState*).</span></span>
    -   <span data-ttu-id="6a8e9-186">Un puntero al objeto `AsyncOp`.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-186">A pointer to the `AsyncOp` object.</span></span>
3.  <span data-ttu-id="6a8e9-187">Llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) para poner en cola un nuevo elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-187">Calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item.</span></span> <span data-ttu-id="6a8e9-188">Esta llamada crea implícitamente un objeto de resultado externo, que contiene los siguientes punteros:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-188">This call implicitly creates an outer result object, which holds the following pointers:</span></span>
    -   <span data-ttu-id="6a8e9-189">Puntero a la `SqrRoot` interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del objeto.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-189">A pointer to the `SqrRoot` object's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="6a8e9-190">Un puntero al objeto de resultado interno del paso 2.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-190">A pointer to the inner result object from step 2.</span></span>

<span data-ttu-id="6a8e9-191">El código siguiente implementa el `SqrRoot::Invoke` método:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-191">The following code implements the `SqrRoot::Invoke` method:</span></span>


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



<span data-ttu-id="6a8e9-192">Este método obtiene el objeto de resultado interno y el `AsyncOp` objeto.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-192">This method gets the inner result object and the `AsyncOp` object.</span></span> <span data-ttu-id="6a8e9-193">A continuación, pasa el `AsyncOp` objeto a `DoCalculateSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-193">Then it passes the `AsyncOp` object to `DoCalculateSquareRoot`.</span></span> <span data-ttu-id="6a8e9-194">Finalmente, llama a [**IMFAsyncResult:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) para establecer el código de estado y [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar el método de devolución de llamada del llamador.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-194">Finally, it calls [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) to set the status code and [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>

<span data-ttu-id="6a8e9-195">El `DoCalculateSquareRoot` método hace exactamente lo que cabría esperar:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-195">The `DoCalculateSquareRoot` method does exactly what you would expect:</span></span>


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



<span data-ttu-id="6a8e9-196">Cuando se invoca el método de devolución de llamada del llamador, es responsabilidad del llamador llamar al método **End...** (en este caso,) `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-196">When the caller's callback method is invoked, it is the caller's responsibility to call the **End...** method—in this case, `EndSquareRoot`.</span></span> <span data-ttu-id="6a8e9-197">`EndSquareRoot`Es cómo el autor de la llamada recupera el resultado de la operación asincrónica, que en este ejemplo es la raíz cuadrada calculada.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-197">The `EndSquareRoot` is how the caller retrieves the result of the asynchronous operation, which in this example is the computed square root.</span></span> <span data-ttu-id="6a8e9-198">Esta información se almacena en el objeto de resultado:</span><span class="sxs-lookup"><span data-stu-id="6a8e9-198">This information is stored in the result object:</span></span>


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a><span data-ttu-id="6a8e9-199">Colas de operaciones</span><span class="sxs-lookup"><span data-stu-id="6a8e9-199">Operation Queues</span></span>

<span data-ttu-id="6a8e9-200">Hasta ahora, se ha asumido tácitamente que una operación asincrónica podría realizarse en cualquier momento, independientemente del estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-200">So far, it has been tacitly assumed that an asynchronous operation could be done at any time, regardless of the object's current state.</span></span> <span data-ttu-id="6a8e9-201">Por ejemplo, tenga en cuenta lo que sucede si una aplicación llama a `BeginSquareRoot` mientras una llamada anterior al mismo método todavía está pendiente.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-201">For example, consider what happens if an application calls `BeginSquareRoot` while an earlier call to the same method is still pending.</span></span> <span data-ttu-id="6a8e9-202">La `SqrRoot` clase puede poner en cola el nuevo elemento de trabajo antes de que se realice el elemento de trabajo anterior.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-202">The `SqrRoot` class might queue the new work item before the previous work item is done.</span></span> <span data-ttu-id="6a8e9-203">Sin embargo, no se garantiza que las colas de trabajo serialicen los elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-203">However, work queues are not guaranteed to serialize work items.</span></span> <span data-ttu-id="6a8e9-204">Recuerde que una cola de trabajo puede utilizar más de un subproceso para enviar elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-204">Recall that a work queue can use more than one thread to dispatch work items.</span></span> <span data-ttu-id="6a8e9-205">En un entorno multiproceso, se podría invocar un elemento de trabajo antes de que se completase el anterior.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-205">In a multithreaded environment, a work item might be invoked before the previous one has completed.</span></span> <span data-ttu-id="6a8e9-206">Los elementos de trabajo incluso se pueden invocar sin orden, si se produce un cambio de contexto justo antes de que se invoque la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-206">Work items can even be invoked out of order, if a context switch happens to occur just before the callback is invoked.</span></span>

<span data-ttu-id="6a8e9-207">Por esta razón, es responsabilidad del objeto serializar las operaciones en sí misma, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-207">For this reason, it is the object's responsibility to serialize operations on itself, if required.</span></span> <span data-ttu-id="6a8e9-208">En otras palabras, si el objeto requiere la operación a para finalizar antes de que se pueda iniciar la operación *B* , el objeto no debe *poner en cola* un elemento de trabajo para *B* hasta que se haya completado la operación *A* .</span><span class="sxs-lookup"><span data-stu-id="6a8e9-208">In other words, if the object requires operation *A* to finish before operation *B* can start, the object must not queue a work item for *B* until operation *A* has completed.</span></span> <span data-ttu-id="6a8e9-209">Un objeto puede cumplir este requisito si tiene su propia cola de operaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-209">An object can meet this requirement by having its own queue of pending operations.</span></span> <span data-ttu-id="6a8e9-210">Cuando se llama a un método asincrónico en el objeto, el objeto coloca la solicitud en su propia cola.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-210">When an asynchronous method is called on the object, the object puts the request on its own queue.</span></span> <span data-ttu-id="6a8e9-211">A medida que se completa cada operación asincrónica, el objeto extrae la siguiente solicitud de la cola.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-211">As each asynchronous operation is completed, the object pulls the next request from the queue.</span></span> <span data-ttu-id="6a8e9-212">En el [ejemplo MPEG1Source](mpeg1source-sample.md) se muestra un ejemplo de cómo implementar este tipo de cola.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-212">The [MPEG1Source Sample](mpeg1source-sample.md) shows an example of how to implement such a queue.</span></span>

<span data-ttu-id="6a8e9-213">Un único método puede implicar varias operaciones asincrónicas, especialmente cuando se usan llamadas de e/s.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-213">A single method might involve several asynchronous operations, particularly when I/O calls are used.</span></span> <span data-ttu-id="6a8e9-214">Cuando implemente métodos asincrónicos, piense detenidamente los requisitos de serialización.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-214">When you implement asynchronous methods, think carefully about serialization requirements.</span></span> <span data-ttu-id="6a8e9-215">Por ejemplo, ¿es válido para el objeto iniciar una nueva operación mientras una solicitud de e/s anterior todavía está pendiente?</span><span class="sxs-lookup"><span data-stu-id="6a8e9-215">For example, is it valid for the object to start a new operation while a previous I/O request is still pending?</span></span> <span data-ttu-id="6a8e9-216">Si la nueva operación cambia el estado interno del objeto, ¿qué ocurre cuando se completa una solicitud de e/s anterior y devuelve datos que ahora pueden estar obsoletos?</span><span class="sxs-lookup"><span data-stu-id="6a8e9-216">If the new operation changes the object's internal state, what happens when a previous I/O request completes and returns data that might now be stale?</span></span> <span data-ttu-id="6a8e9-217">Un buen diagrama de estado puede ayudar a identificar las transiciones de estado válidas.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-217">A good state diagram can help to identify the valid state transitions.</span></span>

## <a name="cross-thread-and-cross-process-considerations"></a><span data-ttu-id="6a8e9-218">Consideraciones entre subprocesos y entre procesos</span><span class="sxs-lookup"><span data-stu-id="6a8e9-218">Cross-Thread and Cross-Process Considerations</span></span>

<span data-ttu-id="6a8e9-219">Las colas de trabajo no utilizan el cálculo de referencias COM para calcular las referencias de punteros de interfaz a través de los límites de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-219">Work queues do not use COM marshaling to marshal interface pointers across thread boundaries.</span></span> <span data-ttu-id="6a8e9-220">Por lo tanto, aunque un objeto se registre como subproceso controlado por apartamento o el subproceso de aplicación haya entrado en un contenedor uniproceso (STA), las devoluciones de llamada de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) se invocarán desde un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-220">Therefore, even if an object is registered as apartment-threaded or the application thread has entered a single-threaded apartment (STA), [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callbacks will be invoked from a different thread.</span></span> <span data-ttu-id="6a8e9-221">En cualquier caso, todos los componentes de canalización de Media Foundation deben usar el modelo de subprocesos "ambos".</span><span class="sxs-lookup"><span data-stu-id="6a8e9-221">In any case, all Media Foundation pipeline components should use the "Both" threading model.</span></span>

<span data-ttu-id="6a8e9-222">Algunas interfaces de Media Foundation definen versiones remotas de algunos métodos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-222">Some interfaces in Media Foundation define remote versions of some asynchronous methods.</span></span> <span data-ttu-id="6a8e9-223">Cuando se llama a uno de estos métodos a través de los límites del proceso, la Media Foundation DLL de proxy/código auxiliar llama a la versión remota del método, que realiza el cálculo de referencias personalizado de los parámetros del método.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-223">When one of these methods is called across process boundaries, the Media Foundation proxy/stub DLL calls the remote version of the method, which performs custom marshaling of the method parameters.</span></span> <span data-ttu-id="6a8e9-224">En el proceso remoto, el código auxiliar vuelve a trasladar la llamada al método local en el objeto.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-224">In the remote process, the stub translates the call back into the local method on the object.</span></span> <span data-ttu-id="6a8e9-225">Este proceso es transparente para la aplicación y el objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="6a8e9-225">This process is transparent to both the application and the remote object.</span></span> <span data-ttu-id="6a8e9-226">Estos métodos de serialización personalizados se proporcionan principalmente para los objetos que se cargan en la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-226">These custom marshaling methods are provided primarily for objects that are loaded in the protected media path (PMP).</span></span> <span data-ttu-id="6a8e9-227">Para obtener más información sobre el PMP, vea [ruta de acceso a medios protegidos](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="6a8e9-227">For more information about the PMP, see [Protected Media Path](protected-media-path.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a8e9-228">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a8e9-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a8e9-229">Métodos de devolución de llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="6a8e9-229">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> <dt>

[<span data-ttu-id="6a8e9-230">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="6a8e9-230">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 



