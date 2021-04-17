---
title: Modelo asincrónico
description: La mayoría de las operaciones en la API de servicios Web de Windows se pueden realizar de forma sincrónica o asincrónica.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Servicios Web de modelo asincrónicos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704677"
---
# <a name="asynchronous-model"></a><span data-ttu-id="b8fdd-106">Modelo asincrónico</span><span class="sxs-lookup"><span data-stu-id="b8fdd-106">Asynchronous Model</span></span>

<span data-ttu-id="b8fdd-107">La mayoría de las operaciones en la API de servicios Web de Windows se pueden realizar de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-107">Most operations in Windows Web Services API can be performed synchronously or asynchronously.</span></span> <span data-ttu-id="b8fdd-108">Para llamar a una función sincrónicamente, pase un valor null para la estructura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="b8fdd-108">To call a function synchronously, pass a null value for the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="b8fdd-109">Para especificar que una función se puede realizar de forma asincrónica, pase un **contexto WS \_ Async \_** que no sea NULL a la función.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-109">To specify that a function may be performed asynchronously, pass a non-null **WS\_ASYNC\_CONTEXT** to the function.</span></span>

<span data-ttu-id="b8fdd-110">Cuando se llama de forma asincrónica, una función puede completarse de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-110">When called asynchronously, a function can nevertheless complete synchronously or asynchronously.</span></span> <span data-ttu-id="b8fdd-111">Si la función se completa sincrónicamente, devuelve un valor que indica el éxito o el error final, y este valor siempre es algo distinto de **WS \_ S \_ Async** (vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="b8fdd-111">If the function completes synchronously, it returns a value that indicates the final success or error, and this value is always something other than **WS\_S\_ASYNC** (See [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span> <span data-ttu-id="b8fdd-112">Sin embargo, un valor devuelto de **WS \_ S \_ Async** indica que la función se completará de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-112">A return value of **WS\_S\_ASYNC**, however, indicates that the function will complete asynchronously.</span></span> <span data-ttu-id="b8fdd-113">Cuando la función se completa de forma asincrónica, se invoca una devolución de llamada para indicar la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-113">When the function completes asynchronously, a callback is invoked to signal completion of the operation.</span></span> <span data-ttu-id="b8fdd-114">Esta devolución de llamada indica el valor final correcto o error.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-114">This callback indicates the final success or error value.</span></span> <span data-ttu-id="b8fdd-115">No se llama a la devolución de llamada si la operación se completa de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-115">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="b8fdd-116">Para crear un contexto asincrónico, inicialice los campos de **devolución de llamada** y **callbackState** de la estructura de [**contexto de WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="b8fdd-116">To create an asynchronous context, initialize the **callback** and **callbackState** fields of the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="b8fdd-117">El campo **callbackState** se usa para especificar un puntero a datos definidos por el usuario que se pasa a la función de [**devolución de \_ \_ llamada de WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="b8fdd-117">The **callbackState** field is used to specify a pointer to user-defined data which is passed to the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) function.</span></span>

<span data-ttu-id="b8fdd-118">En el ejemplo siguiente se muestra cómo llamar a una función de forma asincrónica pasando un puntero a una estructura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) que contiene la devolución de llamada y un puntero a los datos de estado.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-118">The following example shows calling a function asynchronously by passing a pointer to a [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure that contains the callback and a pointer to the state data.</span></span>

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

<span data-ttu-id="b8fdd-119">La función asincrónica utiliza la estructura de [**\_ \_ contexto de WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) solo mientras dure la llamada de función (no mientras dure la operación asincrónica), por lo que puede declararla de forma segura en la pila.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-119">The [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure is used by the asynchronous function only for the duration of the function call (not for the duration of the asynchronous operation), so you can safely declare it on the stack.</span></span>

<span data-ttu-id="b8fdd-120">Si cualquier otro parámetro, además de la estructura de [**\_ \_ contexto de WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , se pasa a una función asincrónica como punteros y la función se completa de forma asincrónica, es responsabilidad del llamador mantener activos los valores a los que apuntan estos parámetros (no liberado) hasta que se invoque la devolución de llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-120">If any other parameters, besides the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure, are passed to an asynchronous function as pointers and the function completes asynchronously, it is the responsibility of the caller to keep the values pointed to by these parameters alive (not freed) until the asynchronous callback is invoked.</span></span>

<span data-ttu-id="b8fdd-121">Existen limitaciones en cuanto a las operaciones que puede realizar una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-121">There are limitations on what operations a callback may perform.</span></span> <span data-ttu-id="b8fdd-122">Para obtener más información sobre las operaciones posibles, vea el [**\_ \_ modelo de devolución de llamada WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span><span class="sxs-lookup"><span data-stu-id="b8fdd-122">For more information on possible operations , see the [**WS\_CALLBACK\_MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span></span>

<span data-ttu-id="b8fdd-123">Cuando implemente una función asincrónica, no invoque la devolución de llamada en el mismo subproceso que llamó a la función asincrónica antes de que la función asincrónica haya devuelto al autor de la llamada, ya que esto interrumpe el modelo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-123">When you implement an asynchronous function, do not invoke the callback on the same thread that called the asynchronous function before the asynchronous function has returned to the caller, as this disrupts the asynchronous model.</span></span>

<span data-ttu-id="b8fdd-124">Al implementar una función que necesita ejecutar una serie de operaciones asincrónicas, considere la posibilidad de usar la función auxiliar [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .</span><span class="sxs-lookup"><span data-stu-id="b8fdd-124">When implementing a function that needs to execute a series of asynchronous operations, consider using the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper function.</span></span>

<span data-ttu-id="b8fdd-125">En el ejemplo de la [función asincrónica](asyncmodelexample.md) se muestra cómo implementar y consumir funciones que siguen el modelo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-125">The [Asynchronous Function Example](asyncmodelexample.md) shows how to implement and consume functions that follow the asynchronous model.</span></span>

<span data-ttu-id="b8fdd-126">Al iniciar una operación de e/s asincrónica, se consumen recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-126">Starting an asynchronous IO operation consumes system resources.</span></span> <span data-ttu-id="b8fdd-127">Si se inician suficientes operaciones de e/s, el sistema puede dejar de responder.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-127">If enough IO operations are started, the system can become unresponsive.</span></span> <span data-ttu-id="b8fdd-128">Para evitar esto, una aplicación debe limitar el número de operaciones asincrónicas que se inician.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-128">To prevent this, an application needs to limit the number of asynchronous operations that it starts.</span></span>

<span data-ttu-id="b8fdd-129">El modelo asincrónico usa los siguientes elementos de la API.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-129">The asynchronous model uses the following API elements.</span></span>

| <span data-ttu-id="b8fdd-130">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="b8fdd-130">Callback</span></span>                                         | <span data-ttu-id="b8fdd-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8fdd-131">Description</span></span>                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8fdd-132">**devolución de llamada de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-132">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | <span data-ttu-id="b8fdd-133">Parámetro de la función de devolución de llamada que se usa con el modelo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-133">The callback function parameter used with the asynchronous model.</span></span>                                                                     |
| [<span data-ttu-id="b8fdd-134">**función de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-134">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | <span data-ttu-id="b8fdd-135">Se usa con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar la función siguiente que se va a invocar en una serie de operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-135">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |



 



| <span data-ttu-id="b8fdd-136">Enumeración</span><span class="sxs-lookup"><span data-stu-id="b8fdd-136">Enumeration</span></span>                                      | <span data-ttu-id="b8fdd-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8fdd-137">Description</span></span>                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8fdd-138">**\_modelo de devolución de llamada WS \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-138">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | <span data-ttu-id="b8fdd-139">Especifica el comportamiento de subprocesos de una devolución de llamada (por ejemplo, una [**\_ devolución de \_ llamada de WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span><span class="sxs-lookup"><span data-stu-id="b8fdd-139">Specifies the threading behavior of a callback (for example, a [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span></span> |



 



| <span data-ttu-id="b8fdd-140">Función</span><span class="sxs-lookup"><span data-stu-id="b8fdd-140">Function</span></span>                                 | <span data-ttu-id="b8fdd-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8fdd-141">Description</span></span>                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8fdd-142">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-142">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | <span data-ttu-id="b8fdd-143">Invoca una devolución de llamada definida por el usuario que puede iniciar una operación asincrónica e indicar una función a la que se debe llamar cuando se haya completado la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-143">Invokes a user-defined callback which can initiate an asynchronous operation and indicate a function that should be called when the asynchronous operation has been completed.</span></span> |



 



| <span data-ttu-id="b8fdd-144">Estructura</span><span class="sxs-lookup"><span data-stu-id="b8fdd-144">Structure</span></span>                                          | <span data-ttu-id="b8fdd-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8fdd-145">Description</span></span>                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8fdd-146">**contexto de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-146">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | <span data-ttu-id="b8fdd-147">Especifica la devolución de llamada asincrónica y un puntero a los datos definidos por el usuario, que se pasarán a la devolución de llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-147">Specifies the asynchronous callback and a pointer to user-defined data, which will be passed to the asynchronous callback.</span></span>            |
| [<span data-ttu-id="b8fdd-148">**operación de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-148">**WS\_ASYNC\_OPERATION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | <span data-ttu-id="b8fdd-149">Se usa con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar la función siguiente que se va a invocar en una serie de operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-149">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |
| [<span data-ttu-id="b8fdd-150">**Estado de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-150">**WS\_ASYNC\_STATE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | <span data-ttu-id="b8fdd-151">Usado por [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para administrar el estado de una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-151">Used by [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to manage the state of an asynchronous operation.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b8fdd-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8fdd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8fdd-153">Ejemplo de función asincrónica</span><span class="sxs-lookup"><span data-stu-id="b8fdd-153">Asynchronous Function Example</span></span>](asyncmodelexample.md)
</dt> <dt>

[<span data-ttu-id="b8fdd-154">**devolución de llamada de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-154">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[<span data-ttu-id="b8fdd-155">**contexto de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-155">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[<span data-ttu-id="b8fdd-156">**\_modelo de devolución de llamada WS \_**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-156">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[<span data-ttu-id="b8fdd-157">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="b8fdd-157">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




