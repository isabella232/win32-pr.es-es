---
description: Las aplicaciones WMI escritas en C++ pueden realizar llamadas asincrónicas mediante muchos de los métodos de la interfaz COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Realización de una llamada asincrónica con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717127"
---
# <a name="making-an-asynchronous-call-with-c"></a><span data-ttu-id="efe1a-103">Realización de una llamada asincrónica con C++</span><span class="sxs-lookup"><span data-stu-id="efe1a-103">Making an Asynchronous Call with C++</span></span>

<span data-ttu-id="efe1a-104">Las aplicaciones WMI escritas en C++ pueden realizar llamadas asincrónicas mediante muchos de los métodos de la interfaz com [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="efe1a-104">WMI applications written in C++ can make asynchronous calls by using many of the methods of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM interface.</span></span> <span data-ttu-id="efe1a-105">Sin embargo, el procedimiento recomendado para llamar a un [*método WMI*](gloss-w.md) o a un [*método de proveedor*](gloss-p.md) es mediante llamadas semisincrónicas, ya que las llamadas sincrónicas son más seguras que las llamadas asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="efe1a-105">However, the recommended procedure for calling a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) is by using semisynchronous calls because semisynchronous calls are more secure than asynchronous calls.</span></span> <span data-ttu-id="efe1a-106">Para obtener más información, vea [crear una llamada semisincrónica con C++](making-a-semisynchronous-call-with-c--.md) y [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="efe1a-106">For more information, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="efe1a-107">En el procedimiento siguiente se describe cómo hacer una llamada asincrónica mediante el uso del receptor en el proceso.</span><span class="sxs-lookup"><span data-stu-id="efe1a-107">The following procedure describes how to make an asynchronous call by using the sink in your process.</span></span>

<span data-ttu-id="efe1a-108">**Para hacer una llamada asincrónica con C++**</span><span class="sxs-lookup"><span data-stu-id="efe1a-108">**To make an asynchronous call using C++**</span></span>

1.  <span data-ttu-id="efe1a-109">Implemente la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="efe1a-109">Implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="efe1a-110">Todas las aplicaciones que realizan llamadas asincrónicas deben implementar [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="efe1a-110">All applications that make asynchronous calls must implement [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="efe1a-111">Los consumidores de eventos temporales también implementan **IWbemObjectSink** para recibir notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="efe1a-111">Temporary event consumers also implement **IWbemObjectSink** to receive notification of events.</span></span>

2.  <span data-ttu-id="efe1a-112">Inicie sesión en el espacio de nombres WMI de destino.</span><span class="sxs-lookup"><span data-stu-id="efe1a-112">Log on to the target WMI namespace.</span></span>

    <span data-ttu-id="efe1a-113">Las aplicaciones siempre tienen que llamar a la función COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) durante la fase de inicialización.</span><span class="sxs-lookup"><span data-stu-id="efe1a-113">Applications always have to call the COM function [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) during the initialization phase.</span></span> <span data-ttu-id="efe1a-114">Si no lo hacen antes de realizar una llamada asincrónica, WMI libera el receptor de la aplicación sin completar la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="efe1a-114">If they do not do so before making an asynchronous call, WMI releases the application sink without completing the asynchronous call.</span></span> <span data-ttu-id="efe1a-115">Para obtener más información, vea [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="efe1a-115">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

3.  <span data-ttu-id="efe1a-116">Establezca la seguridad del receptor.</span><span class="sxs-lookup"><span data-stu-id="efe1a-116">Set the security for your sink.</span></span>

    <span data-ttu-id="efe1a-117">Las llamadas asincrónicas crean una variedad de problemas de seguridad que es posible que tenga que tratar, por ejemplo, para permitir el acceso de WMI a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="efe1a-117">Asynchronous calls create a variety of security issues that you may have to deal with, for example, allowing WMI access to your application.</span></span> <span data-ttu-id="efe1a-118">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="efe1a-118">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

4.  <span data-ttu-id="efe1a-119">Realice la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="efe1a-119">Make the asynchronous call.</span></span>

    <span data-ttu-id="efe1a-120">El método se devuelve inmediatamente con el código de **\_ \_ \_ error de WBEM S** .</span><span class="sxs-lookup"><span data-stu-id="efe1a-120">The method returns immediately with the **WBEM\_S\_NO\_ERROR** success code.</span></span> <span data-ttu-id="efe1a-121">La aplicación puede continuar con otras tareas mientras espera a que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="efe1a-121">The application can proceed with other tasks while waiting for the operation to complete.</span></span> <span data-ttu-id="efe1a-122">WMI informa de nuevo a la aplicación llamando a métodos en la implementación de [**IWbemObjectSink**](iwbemobjectsink.md) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="efe1a-122">WMI reports back to the application by calling methods in the [**IWbemObjectSink**](iwbemobjectsink.md) implementation of your application.</span></span>

5.  <span data-ttu-id="efe1a-123">Si es necesario, Compruebe la implementación periódicamente en busca de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="efe1a-123">If necessary, check your implementation periodically for updates.</span></span>

    <span data-ttu-id="efe1a-124">Las aplicaciones pueden recibir notificaciones de estado intermedio estableciendo el parámetro *lFlags* en la llamada asincrónica al **\_ \_ \_ Estado de envío de la marca WBEM**.</span><span class="sxs-lookup"><span data-stu-id="efe1a-124">Applications can receive notification of intermediate status by setting the *lFlags* parameter in the asynchronous call to **WBEM\_FLAG\_SEND\_STATUS**.</span></span> <span data-ttu-id="efe1a-125">WMI informa del estado de la llamada estableciendo el parámetro *lFlags* de [**IWbemObjectSink**](iwbemobjectsink.md) en el **\_ \_ progreso de estado de WBEM**.</span><span class="sxs-lookup"><span data-stu-id="efe1a-125">WMI reports the status of your call by setting the *lFlags* parameter of [**IWbemObjectSink**](iwbemobjectsink.md) to **WBEM\_STATUS\_PROGRESS**.</span></span>

6.  <span data-ttu-id="efe1a-126">Si es necesario, puede cancelar la llamada antes de que WMI finalice el procesamiento llamando al método [**IWbemServices:: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="efe1a-126">If necessary, you can cancel the call before WMI finishes processing by calling the [**IWbemServices::CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method.</span></span>

    <span data-ttu-id="efe1a-127">El método [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) cancela el procesamiento asincrónico liberando inmediatamente el puntero a la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) y garantiza que el puntero se libera antes de que **CancelAsyncCall** devuelva.</span><span class="sxs-lookup"><span data-stu-id="efe1a-127">The [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method cancels asynchronous processing by immediately releasing the pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface and guarantees that the pointer is released before **CancelAsyncCall** returns.</span></span>

    <span data-ttu-id="efe1a-128">Si usa un objeto contenedor que implementa la interfaz **IUnsecured** para hospedar [**IWbemObjectSink**](iwbemobjectsink.md), es posible que encuentre algunas complicaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="efe1a-128">If you are using a wrapper object implementing the **IUnsecured** interface to host [**IWbemObjectSink**](iwbemobjectsink.md), you may find some additional complications.</span></span> <span data-ttu-id="efe1a-129">Dado que la aplicación debe pasar el mismo puntero a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) que se pasó en la llamada asincrónica original, la aplicación debe mantener el objeto contenedor hasta que quede claro que no se requiere la cancelación.</span><span class="sxs-lookup"><span data-stu-id="efe1a-129">Because the application must pass the same pointer to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) that was passed in the original asynchronous call, the application must hold on to the wrapper object until it becomes clear that cancellation is not required.</span></span> <span data-ttu-id="efe1a-130">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="efe1a-130">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

7.  <span data-ttu-id="efe1a-131">Cuando termine, limpie los punteros y apague la aplicación.</span><span class="sxs-lookup"><span data-stu-id="efe1a-131">When finished, clean up pointers and shut down the application.</span></span>

    <span data-ttu-id="efe1a-132">WMI proporciona la llamada de estado final a través del método [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="efe1a-132">WMI provides the final status call through the [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="efe1a-133">Después de enviar la actualización de estado final, WMI libera el receptor del objeto llamando al método **Release** para la clase que implementa la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="efe1a-133">After sending the final status update, WMI releases the object sink by calling the **Release** method for the class that implements the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span> <span data-ttu-id="efe1a-134">En el ejemplo anterior, este es el método **QuerySink:: Release** .</span><span class="sxs-lookup"><span data-stu-id="efe1a-134">In the previous example, this is the **QuerySink::Release** method.</span></span> <span data-ttu-id="efe1a-135">Si desea tener control sobre la duración del objeto receptor, puede implementar el receptor con un recuento de referencias inicial de uno (1).</span><span class="sxs-lookup"><span data-stu-id="efe1a-135">If you want to have control over the lifetime of the sink object, you can implement the sink with an initial reference count of one (1).</span></span>

     

    <span data-ttu-id="efe1a-136">Si una aplicación cliente pasa la misma interfaz de receptor en dos llamadas asincrónicas diferentes que se superponen, WMI no garantiza el orden de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="efe1a-136">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="efe1a-137">Una aplicación cliente que realiza llamadas asincrónicas superpuestas debe pasar objetos receptores diferentes o serializar las llamadas.</span><span class="sxs-lookup"><span data-stu-id="efe1a-137">A client application making overlapping asynchronous calls should either pass different sink objects or serialize the calls.</span></span>

<span data-ttu-id="efe1a-138">El siguiente ejemplo requiere las siguientes instrucciones de referencia e \# inclusión.</span><span class="sxs-lookup"><span data-stu-id="efe1a-138">The following example requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



<span data-ttu-id="efe1a-139">En el ejemplo siguiente se describe cómo realizar una consulta asincrónica mediante el método [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , pero no se crea la configuración de seguridad ni se libera el objeto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="efe1a-139">The following example describes how to make an asynchronous query using the [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, but does not create security settings or release the [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span> <span data-ttu-id="efe1a-140">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="efe1a-140">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> <span data-ttu-id="efe1a-141">El código anterior no se compila sin errores porque no se ha definido la clase **QuerySink** .</span><span class="sxs-lookup"><span data-stu-id="efe1a-141">The code above does not compile without error because the **QuerySink** class has not been defined.</span></span> <span data-ttu-id="efe1a-142">Para obtener más información sobre **QuerySink**, consulte [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="efe1a-142">For more information about **QuerySink**, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="efe1a-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efe1a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efe1a-144">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="efe1a-144">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
