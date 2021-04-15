---
description: 'Las llamadas semisincrónica son el medio recomendado para llamar a métodos WMI, como IWbemServices:: ExecMethod y métodos de proveedor, como el método CHKDSK de la \_ clase Win32 LogicalDisk.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Realización de una llamada semisincrónica con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546179"
---
# <a name="making-a-semisynchronous-call-with-c"></a><span data-ttu-id="fa47a-103">Realización de una llamada semisincrónica con C++</span><span class="sxs-lookup"><span data-stu-id="fa47a-103">Making a Semisynchronous Call with C++</span></span>

<span data-ttu-id="fa47a-104">Las llamadas semisincrónica son el medio recomendado para llamar a métodos WMI, como [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) y métodos de proveedor, como el [**método CHKDSK de la \_ clase Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="fa47a-104">Semisynchronous calls are the recommended means to call WMI methods, such as [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) and provider methods, such as the [**Chkdsk Method of the Win32\_LogicalDisk Class**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span></span>

<span data-ttu-id="fa47a-105">Una desventaja del procesamiento sincrónico es que el subproceso del llamador se bloquea hasta que se completa la llamada.</span><span class="sxs-lookup"><span data-stu-id="fa47a-105">One disadvantage of synchronous processing is that the caller thread is blocked until the call completes.</span></span> <span data-ttu-id="fa47a-106">El bloqueo puede producir un retraso en el tiempo de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="fa47a-106">The blockage can cause a delay in processing time.</span></span> <span data-ttu-id="fa47a-107">En cambio, una llamada asincrónica debe implementar [**SWbemSink**](swbemsink.md) en el script.</span><span class="sxs-lookup"><span data-stu-id="fa47a-107">In contrast, an asynchronous call must implement [**SWbemSink**](swbemsink.md) in script.</span></span> <span data-ttu-id="fa47a-108">En C++, el código asincrónico debe implementar la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) , usar varios subprocesos y controlar el flujo de información de vuelta al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="fa47a-108">In C++, asynchronous code must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface, use multiple threads, and control the flow of information back to the caller.</span></span> <span data-ttu-id="fa47a-109">Los grandes conjuntos de resultados de las consultas, por ejemplo, pueden tardar una cantidad considerable de tiempo en entregar y obligar a que el autor de la llamada dedique bastantes recursos del sistema para controlar la entrega.</span><span class="sxs-lookup"><span data-stu-id="fa47a-109">Large result sets from queries, for example, can take a considerable amount of time to deliver and forces the caller to spend significant system resources to handle the delivery.</span></span>

<span data-ttu-id="fa47a-110">El procesamiento semisincrónico resuelve el bloqueo de subprocesos y los problemas de entrega no controlada mediante el sondeo de un objeto de estado especial que implementa la interfaz [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .</span><span class="sxs-lookup"><span data-stu-id="fa47a-110">Semisynchronous processing solves both the thread blockage and uncontrolled delivery problems by polling a special status object that implements the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) interface.</span></span> <span data-ttu-id="fa47a-111">A través de **IWbemCallResult**, puede mejorar la velocidad y la eficacia de las consultas, las enumeraciones y las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="fa47a-111">Through **IWbemCallResult**, you can improve the speed and efficiency of queries, enumerations, and event notifications.</span></span>

<span data-ttu-id="fa47a-112">En el procedimiento siguiente se describe cómo crear una llamada semisincrónica con la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="fa47a-112">The following procedure describes how to make a semisynchronous call with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="fa47a-113">**Para hacer una llamada semisincrónica con la interfaz IWbemServices**</span><span class="sxs-lookup"><span data-stu-id="fa47a-113">**To make a semisynchronous call with the IWbemServices interface**</span></span>

1.  <span data-ttu-id="fa47a-114">Realice la llamada de la forma habitual, pero con la **marca WBEM devolver la marca \_ \_ \_ inmediatamente** establecida en el parámetro *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="fa47a-114">Make your call as normal, but with the **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag set in the *IFlags* parameter.</span></span>

    <span data-ttu-id="fa47a-115">Puede combinar la **devolución de la marca WBEM de \_ \_ \_ inmediato** con otras marcas válidas para el método concreto.</span><span class="sxs-lookup"><span data-stu-id="fa47a-115">You can combine **WBEM\_FLAG\_RETURN\_IMMEDIATELY** with other flags that are valid for the specific method.</span></span> <span data-ttu-id="fa47a-116">Por ejemplo, use la **marca \_ WBEM \_ marcar \_ solo hacia delante** para todas las llamadas que devuelven enumeradores.</span><span class="sxs-lookup"><span data-stu-id="fa47a-116">For example, use the **WBEM\_FLAG\_FORWARD\_ONLY** flag for all calls that return enumerators.</span></span> <span data-ttu-id="fa47a-117">Si se establecen estas marcas en combinación, se ahorra tiempo y espacio, y mejora la capacidad de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa47a-117">Setting these flags in combination saves time and space, and improves responsiveness.</span></span>

2.  <span data-ttu-id="fa47a-118">Sondear los resultados.</span><span class="sxs-lookup"><span data-stu-id="fa47a-118">Poll for your results.</span></span>

    <span data-ttu-id="fa47a-119">Si llama a un método que devuelve un enumerador, como [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) o [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), puede sondear los enumeradores con los métodos [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) .</span><span class="sxs-lookup"><span data-stu-id="fa47a-119">If you call a method that returns an enumerator, such as [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) or [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), you can poll the enumerators with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) methods.</span></span> <span data-ttu-id="fa47a-120">La llamada a **IEnumWbemClassObject:: NextAsync** es de no bloqueo y vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fa47a-120">The **IEnumWbemClassObject::NextAsync** call is nonblocking and returns immediately.</span></span> <span data-ttu-id="fa47a-121">En segundo plano, WMI comienza a ofrecer el número solicitado de objetos mediante una llamada a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="fa47a-121">In the background, WMI begins to deliver the requested number of objects by calling [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span> <span data-ttu-id="fa47a-122">WMI se detiene entonces y espera otra llamada **NextAsync** .</span><span class="sxs-lookup"><span data-stu-id="fa47a-122">WMI then stops and waits for another **NextAsync** call.</span></span>

    <span data-ttu-id="fa47a-123">Si llama a un método que no devuelve un enumerador, como [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), debe establecer el parámetro *ppCallResult* en un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="fa47a-123">If you call a method that does not return an enumerator, such as [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), you must set the *ppCallResult* parameter to a valid pointer.</span></span> <span data-ttu-id="fa47a-124">Use [**IWbemCallResult:: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) en el puntero devuelto para recuperar **WBEM \_ S \_ no \_ error**.</span><span class="sxs-lookup"><span data-stu-id="fa47a-124">Use the [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) on the returned pointer to retrieve **WBEM\_S\_NO\_ERROR**.</span></span>

3.  <span data-ttu-id="fa47a-125">Finalice la llamada.</span><span class="sxs-lookup"><span data-stu-id="fa47a-125">Finish your call.</span></span>

    <span data-ttu-id="fa47a-126">En el caso de una llamada que devuelve un enumerador, WMI llama a [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para notificar la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="fa47a-126">For a call that returns an enumerator, WMI calls [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to report the completion of the operation.</span></span> <span data-ttu-id="fa47a-127">Si no necesita todo el resultado, libere el enumerador llamando al método [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="fa47a-127">If you do not need the entire result, release the enumerator by calling the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="fa47a-128">La llamada a los resultados de la **versión** en WMI cancela la entrega de todos los objetos que permanecen.</span><span class="sxs-lookup"><span data-stu-id="fa47a-128">Calling **Release** results in WMI canceling the delivery of all objects that remain.</span></span>

    <span data-ttu-id="fa47a-129">En el caso de una llamada que no use un enumerador, recupere el objeto [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) mediante el parámetro *plStatus* de su método.</span><span class="sxs-lookup"><span data-stu-id="fa47a-129">For a call that does not use an enumerator, retrieve the [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) object through the *plStatus* parameter of your method.</span></span>

<span data-ttu-id="fa47a-130">El ejemplo de código de C++ de este tema requiere las siguientes \# instrucciones include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa47a-130">The C++ code example in this topic requires the following \#include statements to compile correctly.</span></span>


```C++
#include <comdef.h>
#include <wbemidl.h>
```



<span data-ttu-id="fa47a-131">En el ejemplo de código siguiente se muestra cómo hacer una llamada semisincrónica a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="fa47a-131">The following code example shows how to make a semisynchronous call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a><span data-ttu-id="fa47a-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa47a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa47a-133">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="fa47a-133">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
