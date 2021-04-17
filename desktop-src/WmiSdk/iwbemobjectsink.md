---
description: La interfaz IWbemObjectSink crea una interfaz de receptor que puede recibir todos los tipos de notificaciones en el modelo de programación WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interfaz IWbemObjectSink (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687311"
---
# <a name="iwbemobjectsink-interface"></a><span data-ttu-id="599e3-103">Interfaz IWbemObjectSink</span><span class="sxs-lookup"><span data-stu-id="599e3-103">IWbemObjectSink interface</span></span>

<span data-ttu-id="599e3-104">La interfaz **IWbemObjectSink** crea una interfaz de receptor que puede recibir todos los tipos de notificaciones en el modelo de programación WMI.</span><span class="sxs-lookup"><span data-stu-id="599e3-104">The **IWbemObjectSink** interface creates a sink interface that can receive all types of notifications within the WMI programming model.</span></span> <span data-ttu-id="599e3-105">Los clientes deben implementar esta interfaz para recibir los resultados de los [métodos asincrónicos](making-an-asynchronous-call-with-c--.md) de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)y los tipos específicos de notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="599e3-105">Clients must implement this interface to receive both the results of the [asynchronous methods](making-an-asynchronous-call-with-c--.md) of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), and specific types of event notifications.</span></span> <span data-ttu-id="599e3-106">Los proveedores usan, pero no implementan esta interfaz para proporcionar eventos y objetos a WMI.</span><span class="sxs-lookup"><span data-stu-id="599e3-106">Providers use, but do not implement this interface to provide events and objects to WMI.</span></span>

<span data-ttu-id="599e3-107">Normalmente, los proveedores llaman a una implementación proporcionada por WMI.</span><span class="sxs-lookup"><span data-stu-id="599e3-107">Typically, providers call an implementation provided to them by WMI.</span></span> <span data-ttu-id="599e3-108">En estos casos, la llamada a [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) que se proporcionan objetos al servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="599e3-108">In these cases, call [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to provide objects to the WMI service.</span></span> <span data-ttu-id="599e3-109">Después, llame a [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para indicar el final de la secuencia de notificación.</span><span class="sxs-lookup"><span data-stu-id="599e3-109">After that, call [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to indicate the end of the notification sequence.</span></span> <span data-ttu-id="599e3-110">También puede llamar a **SetStatus** para indicar errores cuando el receptor no tiene ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="599e3-110">You can also call **SetStatus** to indicate errors when the sink does not have any objects.</span></span>

<span data-ttu-id="599e3-111">Al programar clientes asincrónicos de WMI, el usuario proporciona la implementación.</span><span class="sxs-lookup"><span data-stu-id="599e3-111">When programming asynchronous clients of WMI, the user provides the implementation.</span></span> <span data-ttu-id="599e3-112">WMI llama a los métodos para ofrecer objetos y establecer el estado del resultado.</span><span class="sxs-lookup"><span data-stu-id="599e3-112">WMI calls the methods to deliver objects and set the status of the result.</span></span>

> [!Note]  
> <span data-ttu-id="599e3-113">Si una aplicación cliente pasa la misma interfaz de receptor en dos llamadas asincrónicas diferentes que se superponen, WMI no garantiza el orden de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="599e3-113">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="599e3-114">Las aplicaciones cliente que realizan llamadas asincrónicas superpuestas deben pasar objetos receptores diferentes o serializar sus llamadas.</span><span class="sxs-lookup"><span data-stu-id="599e3-114">Client applications that make overlapping asynchronous calls should either pass different sink objects, or serialize their calls.</span></span>

 

> [!Note]  
> <span data-ttu-id="599e3-115">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="599e3-115">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="599e3-116">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="599e3-116">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="599e3-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="599e3-117">Members</span></span>

<span data-ttu-id="599e3-118">La interfaz **IWbemObjectSink** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="599e3-118">The **IWbemObjectSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="599e3-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="599e3-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="599e3-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="599e3-120">Methods</span></span>

<span data-ttu-id="599e3-121">La interfaz **IWbemObjectSink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="599e3-121">The **IWbemObjectSink** interface has these methods.</span></span>



| <span data-ttu-id="599e3-122">Método</span><span class="sxs-lookup"><span data-stu-id="599e3-122">Method</span></span>                                         | <span data-ttu-id="599e3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="599e3-123">Description</span></span>                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="599e3-124">**Indicar**</span><span class="sxs-lookup"><span data-stu-id="599e3-124">**Indicate**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | <span data-ttu-id="599e3-125">Recibe objetos de notificación.</span><span class="sxs-lookup"><span data-stu-id="599e3-125">Receives notification objects.</span></span><br/>                                                                               |
| [<span data-ttu-id="599e3-126">**SetStatus**</span><span class="sxs-lookup"><span data-stu-id="599e3-126">**SetStatus**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | <span data-ttu-id="599e3-127">Lo llaman los orígenes para indicar el final de una secuencia de notificación, o para enviar otros códigos de estado al receptor.</span><span class="sxs-lookup"><span data-stu-id="599e3-127">Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="599e3-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="599e3-128">Remarks</span></span>

<span data-ttu-id="599e3-129">Al implementar un receptor de suscripciones de eventos (**IWbemObjectSink** o [**IWbemEventSink**](iwbemeventsink.md)), no llame a WMI desde los métodos de [**indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) o [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) en el objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="599e3-129">When implementing an event subscription sink (**IWbemObjectSink** or [**IWbemEventSink**](iwbemeventsink.md)), do not call into WMI from within the [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) or [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) methods on the sink object.</span></span> <span data-ttu-id="599e3-130">Por ejemplo, la llamada a [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar el receptor desde una implementación de [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) que puede interferir con el estado de WMI.</span><span class="sxs-lookup"><span data-stu-id="599e3-130">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) can interfere with the WMI state.</span></span> <span data-ttu-id="599e3-131">Para cancelar una suscripción de eventos, establezca una marca y llame a **IWbemServices:: CancelAsyncCall** desde otro subproceso u objeto.</span><span class="sxs-lookup"><span data-stu-id="599e3-131">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="599e3-132">En el caso de las implementaciones que no están relacionadas con un receptor de eventos, como las recuperaciones de objetos, enumeraciones y consultas, puede volver a llamar a WMI.</span><span class="sxs-lookup"><span data-stu-id="599e3-132">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="599e3-133">Las implementaciones de receptores deben procesar la notificación de eventos en un plazo de 100 MS, ya que el subproceso de WMI que entrega la notificación de eventos no puede realizar otras tareas hasta que el objeto receptor haya completado el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="599e3-133">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="599e3-134">Si la notificación requiere una gran cantidad de procesamiento, el receptor puede utilizar una cola interna para que otro subproceso controle el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="599e3-134">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="examples"></a><span data-ttu-id="599e3-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="599e3-135">Examples</span></span>

<span data-ttu-id="599e3-136">El siguiente ejemplo de código es una implementación simple de un receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="599e3-136">The following code example is a simple implementation of an object sink.</span></span> <span data-ttu-id="599e3-137">Este ejemplo se puede usar con [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) para recibir las instancias devueltas:</span><span class="sxs-lookup"><span data-stu-id="599e3-137">This sample can be used with [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) to receive the returned instances:</span></span>


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a><span data-ttu-id="599e3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="599e3-138">Requirements</span></span>



| <span data-ttu-id="599e3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="599e3-139">Requirement</span></span> | <span data-ttu-id="599e3-140">Value</span><span class="sxs-lookup"><span data-stu-id="599e3-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="599e3-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="599e3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="599e3-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="599e3-142">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="599e3-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="599e3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="599e3-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="599e3-144">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="599e3-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="599e3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="599e3-146"><dt>Wbemcli. h (incluye Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="599e3-146"><dt>Wbemcli.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="599e3-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="599e3-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="599e3-148"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="599e3-148"><dt>Wbemuuid.lib</dt></span></span> </dl>                  |
| <span data-ttu-id="599e3-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="599e3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599e3-150"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599e3-150"><dt>Fastprox.dll</dt></span></span> </dl>                  |



## <a name="see-also"></a><span data-ttu-id="599e3-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="599e3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599e3-152">API COM para WMI</span><span class="sxs-lookup"><span data-stu-id="599e3-152">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="599e3-153">Realización de una llamada asincrónica con C++</span><span class="sxs-lookup"><span data-stu-id="599e3-153">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[<span data-ttu-id="599e3-154">Establecer la seguridad en una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="599e3-154">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="599e3-155">Recepción de eventos mientras dure la aplicación</span><span class="sxs-lookup"><span data-stu-id="599e3-155">Receiving Events for the Duration of your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




