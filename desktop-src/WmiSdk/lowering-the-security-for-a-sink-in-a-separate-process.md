---
description: Instrumental de administración de Windows (WMI) puede crear el receptor para recibir devoluciones de llamada asincrónicas para una aplicación cliente en un proceso independiente.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Reducir la seguridad de un receptor en un proceso independiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697366"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a><span data-ttu-id="7dbd2-103">Reducir la seguridad de un receptor en un proceso independiente</span><span class="sxs-lookup"><span data-stu-id="7dbd2-103">Lowering the Security for a Sink in a Separate Process</span></span>

<span data-ttu-id="7dbd2-104">Instrumental de administración de Windows (WMI) puede crear el receptor para recibir devoluciones de llamada asincrónicas para una aplicación cliente en un proceso independiente.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-104">Windows Management Instrumentation (WMI) can create the sink to receive asynchronous callbacks for a client application in a separate process.</span></span> <span data-ttu-id="7dbd2-105">El proceso independiente se Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-105">The separate process is Unsecapp.exe.</span></span> <span data-ttu-id="7dbd2-106">Use la interfaz [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="7dbd2-106">Use the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface.</span></span> <span data-ttu-id="7dbd2-107">**IWbemUnsecuredApartment** permite controlar si Unsecapp.exe autentica las devoluciones de llamada en el receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-107">**IWbemUnsecuredApartment** allows you to control whether Unsecapp.exe authenticates callbacks to the sink.</span></span> <span data-ttu-id="7dbd2-108">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="7dbd2-108">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="7dbd2-109">Después, puede reducir la seguridad en ese proceso y WMI puede tener acceso al receptor sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-109">You can then lower the security on that process and WMI can access the sink without restriction.</span></span> <span data-ttu-id="7dbd2-110">Para ayudar a esta técnica, WMI proporciona el proceso de Unsecapp.exe para que funcione como proceso independiente.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-110">To assist with this technique WMI provides the Unsecapp.exe process to function as the separate process.</span></span> <span data-ttu-id="7dbd2-111">Puede hospedar Unsecapp.exe con una llamada a la interfaz [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="7dbd2-111">You can host Unsecapp.exe with a call to the [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface.</span></span>

<span data-ttu-id="7dbd2-112">La interfaz [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) permite a una aplicación cliente crear un proceso dedicado independiente que ejecute Unsecapp.exe para hospedar una implementación de [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="7dbd2-112">The [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface allows a client application to create a separate dedicated process running Unsecapp.exe for hosting a [**IWbemObjectSink**](iwbemobjectsink.md) implementation.</span></span> <span data-ttu-id="7dbd2-113">El proceso dedicado puede llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para conceder acceso a WMI al proceso dedicado sin poner en peligro la seguridad del proceso principal.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-113">The dedicated process can call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to grant WMI access to the dedicated process without compromising the security of the main process.</span></span> <span data-ttu-id="7dbd2-114">Después de la inicialización, el proceso dedicado actúa como intermediario entre el proceso principal y WMI.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-114">After initialization, the dedicated process acts as an intermediary between the main process and WMI.</span></span>

<span data-ttu-id="7dbd2-115">En el procedimiento siguiente se describe cómo realizar una llamada asincrónica con [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="7dbd2-115">The following procedure describes how to perform an asynchronous call with [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span></span>

<span data-ttu-id="7dbd2-116">**Para realizar una llamada asincrónica con IUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="7dbd2-116">**To perform an asynchronous call with IUnsecuredApartment**</span></span>

1.  <span data-ttu-id="7dbd2-117">Cree un proceso dedicado con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7dbd2-117">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="7dbd2-118">En el ejemplo de código siguiente se llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un proceso dedicado.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-118">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="7dbd2-119">Cree una instancia del objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-119">Instantiate the sink object.</span></span>

    <span data-ttu-id="7dbd2-120">En el ejemplo de código siguiente se crea un nuevo objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-120">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="7dbd2-121">Cree un código auxiliar para el receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-121">Create a stub for the sink.</span></span>

    <span data-ttu-id="7dbd2-122">Un código auxiliar es una función contenedora generada a partir del receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-122">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="7dbd2-123">En el ejemplo de código siguiente se llama a [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) para crear un código auxiliar para el receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-123">The following code example calls [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) to create a stub for the sink.</span></span>

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  <span data-ttu-id="7dbd2-124">Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para el contenedor y solicite un puntero a la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="7dbd2-124">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the wrapper, and request a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="7dbd2-125">En el ejemplo de código siguiente se llama a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) y se solicita un puntero a la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="7dbd2-125">The following code example calls [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) and requests a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  <span data-ttu-id="7dbd2-126">Libere el puntero del objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-126">Release the sink object pointer.</span></span>

    <span data-ttu-id="7dbd2-127">Puede liberar el puntero de objeto porque el código auxiliar posee ahora el puntero.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-127">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="7dbd2-128">En el ejemplo de código siguiente se libera el puntero del objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-128">The following code example releases the sink object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

6.  <span data-ttu-id="7dbd2-129">Use el código auxiliar en cualquier llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-129">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="7dbd2-130">Cuando termine con la llamada, libere el recuento de referencias local.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-130">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="7dbd2-131">En el ejemplo de código siguiente se usa el código auxiliar en una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-131">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="7dbd2-132">En ocasiones, puede que tenga que cancelar una llamada asincrónica después de realizar la llamada.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-132">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="7dbd2-133">Si tiene que cancelar la llamada, cancele la llamada con el mismo puntero que originalmente realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-133">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="7dbd2-134">En el ejemplo de código siguiente se muestra cómo cancelar una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-134">The following code example shows how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  <span data-ttu-id="7dbd2-135">Libere el recuento de referencias local cuando haya terminado de usar la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-135">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="7dbd2-136">Asegúrese de liberar el puntero *pStubSink* solo después de confirmar que no es necesario cancelar la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-136">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not need to be canceled.</span></span> <span data-ttu-id="7dbd2-137">Además, no libere *pStubSink* después de que WMI libere el puntero de receptor *pSink* .</span><span class="sxs-lookup"><span data-stu-id="7dbd2-137">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="7dbd2-138">Al liberar *pStubSink* después de *pSink* , se crea un recuento de referencias circulares en el que tanto el receptor como el código auxiliar permanecen en memoria indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-138">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="7dbd2-139">En su lugar, una ubicación posible para liberar el puntero está en la llamada a [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , realizada por WMI para informar de que se ha completado la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-139">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

8.  <span data-ttu-id="7dbd2-140">Cuando termine, desinicialice COM con una llamada a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="7dbd2-140">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="7dbd2-141">En el ejemplo de código siguiente se muestra cómo llamar a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="7dbd2-141">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

    <span data-ttu-id="7dbd2-142">Los ejemplos de código de este tema requieren la siguiente referencia e \# instrucción include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-142">The code examples in this topic require the following reference and \#include statement to correctly compile.</span></span>

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

<span data-ttu-id="7dbd2-143">Para obtener más información sobre la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) y los parámetros, consulte la documentación de [com](../cossdk/component-services-portal.md) en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="7dbd2-143">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
