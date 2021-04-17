---
description: Puede usar el procedimiento y el ejemplo de código de este tema para completar la aplicación cliente WMI que realiza la inicialización COM, se conecta a WMI en el equipo local, recibe una notificación de eventos y, a continuación, se limpia.
ms.assetid: 4d581965-e22a-4205-908c-661eeeec88cf
ms.tgt_platform: multiple
title: 'Ejemplo: recibir notificaciones de eventos a través de WMI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6380d306783f8b547d0d93df0275fd36e17e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497914"
---
# <a name="example-receiving-event-notifications-through-wmi"></a><span data-ttu-id="7700e-103">Ejemplo: recibir notificaciones de eventos a través de WMI</span><span class="sxs-lookup"><span data-stu-id="7700e-103">Example: Receiving Event Notifications Through WMI</span></span>

<span data-ttu-id="7700e-104">Puede usar el procedimiento y el ejemplo de código de este tema para completar la aplicación cliente WMI que realiza la inicialización COM, se conecta a WMI en el equipo local, recibe una notificación de eventos y, a continuación, se limpia.</span><span class="sxs-lookup"><span data-stu-id="7700e-104">You can use the procedure and code example in this topic to complete WMI client application that performs COM initialization, connects to WMI on the local computer, receives an event notification, and then cleans up.</span></span> <span data-ttu-id="7700e-105">En el ejemplo se notifica al usuario sobre un evento cuando se crea un nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="7700e-105">The example notifies the user of an event when a new process is created.</span></span> <span data-ttu-id="7700e-106">Los eventos se reciben de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7700e-106">The events are received asynchronously.</span></span>

<span data-ttu-id="7700e-107">El siguiente procedimiento se utiliza para ejecutar la aplicación WMI.</span><span class="sxs-lookup"><span data-stu-id="7700e-107">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="7700e-108">Los pasos 1 a 5 contienen todos los pasos necesarios para configurar y conectarse a WMI, y el paso 6 es donde se reciben las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="7700e-108">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and step 6 is where the event notifications are received.</span></span>

<span data-ttu-id="7700e-109">**Para recibir una notificación de eventos a través de WMI**</span><span class="sxs-lookup"><span data-stu-id="7700e-109">**To receive a event notification through WMI**</span></span>

1.  <span data-ttu-id="7700e-110">Inicialice los parámetros COM con una llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="7700e-110">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="7700e-111">Para obtener más información, vea [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-111">Fore more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="7700e-112">Inicialice la seguridad del proceso COM llamando a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7700e-112">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="7700e-113">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado mediante C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-113">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="7700e-114">Obtenga el localizador inicial de WMI llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7700e-114">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="7700e-115">Para obtener más información, vea [crear una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-115">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="7700e-116">Obtenga un puntero a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para el espacio de nombres raíz de \\ cimv2 en el equipo local llamando a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="7700e-116">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="7700e-117">Para conectarse a un equipo remoto, vea [ejemplo: obtener datos WMI desde un equipo remoto](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-117">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="7700e-118">Para obtener más información, vea [crear una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-118">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="7700e-119">Establezca la seguridad de proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que el servicio WMI pueda suplantar al cliente mediante una llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="7700e-119">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="7700e-120">Para obtener más información, consulte [configuración de los niveles de seguridad en una conexión WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-120">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="7700e-121">Utilice el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para hacer solicitudes a WMI.</span><span class="sxs-lookup"><span data-stu-id="7700e-121">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="7700e-122">En este ejemplo se usa el método [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) para recibir eventos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="7700e-122">This example uses the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method to receive asynchronous events.</span></span> <span data-ttu-id="7700e-123">Cuando reciba eventos asincrónicos, debe proporcionar una implementación de [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-123">When you receive asynchronous events, you must provide an implementation of [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="7700e-124">En este ejemplo se proporciona la implementación en la clase EventSink.</span><span class="sxs-lookup"><span data-stu-id="7700e-124">This example provides the implementation in the EventSink class.</span></span> <span data-ttu-id="7700e-125">El código de implementación y el código de archivo de encabezado para esta clase se proporcionan debajo del ejemplo principal.</span><span class="sxs-lookup"><span data-stu-id="7700e-125">The implementation code and header file code for this class are provided below the main example.</span></span> <span data-ttu-id="7700e-126">El método **IWbemServices:: ExecNotificationQueryAsync** llama al método **EventSink:: indica** cada vez que se recibe un evento.</span><span class="sxs-lookup"><span data-stu-id="7700e-126">The **IWbemServices::ExecNotificationQueryAsync** method calls the **EventSink::Indicate** method whenever an event is received.</span></span> <span data-ttu-id="7700e-127">En este ejemplo, se llama al método **EventSink:: indica** el momento en que se crea un proceso.</span><span class="sxs-lookup"><span data-stu-id="7700e-127">For this example the **EventSink::Indicate** method is called whenever a process is created.</span></span> <span data-ttu-id="7700e-128">Para probar este ejemplo, ejecute el código e inicie un proceso como Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="7700e-128">To test this example, run the code and start a process such as Notepad.exe.</span></span> <span data-ttu-id="7700e-129">Esto desencadena una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="7700e-129">This triggers an event notification.</span></span>

    <span data-ttu-id="7700e-130">Para obtener más información sobre cómo realizar solicitudes de WMI, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md) y [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7700e-130">For more information about making requests of WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7700e-131">El código de ejemplo siguiente recibe notificaciones de eventos a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="7700e-131">The following example code receives event notifications through WMI.</span></span>


```C++
#include "eventsink.h"

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: -------------------------------------------------
    // Receive event notifications -----------------------------

    // Use an unsecured apartment for security
    IUnsecuredApartment* pUnsecApp = NULL;

    hres = CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
        CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
        (void**)&pUnsecApp);
 
    EventSink* pSink = new EventSink;
    pSink->AddRef();

    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);

    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink,
        (void **) &pStubSink);

    // The ExecNotificationQueryAsync method will call
    // The EventQuery::Indicate method when an event occurs
    hres = pSvc->ExecNotificationQueryAsync(
        _bstr_t("WQL"), 
        _bstr_t("SELECT * " 
            "FROM __InstanceCreationEvent WITHIN 1 "
            "WHERE TargetInstance ISA 'Win32_Process'"), 
        WBEM_FLAG_SEND_STATUS, 
        NULL, 
        pStubSink);

    // Check for errors.
    if (FAILED(hres))
    {
        printf("ExecNotificationQueryAsync failed "
            "with = 0x%X\n", hres);
        pSvc->Release();
        pLoc->Release();
        pUnsecApp->Release();
        pStubUnk->Release();
        pSink->Release();
        pStubSink->Release();
        CoUninitialize();    
        return 1;
    }

    // Wait for the event
    Sleep(10000);
         
    hres = pSvc->CancelAsyncCall(pStubSink);

    // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    pUnsecApp->Release();
    pStubUnk->Release();
    pSink->Release();
    pStubSink->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



<span data-ttu-id="7700e-132">El siguiente archivo de encabezado se usa para la clase EventSink.</span><span class="sxs-lookup"><span data-stu-id="7700e-132">The following header file is used for the class EventSink.</span></span> <span data-ttu-id="7700e-133">La clase EventSink se usa en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="7700e-133">The EventSink class is used in the previous code example.</span></span>


```C++
// EventSink.h
#ifndef EVENTSINK_H
#define EVENTSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class EventSink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;

public:
    EventSink() { m_lRef = 0; }
   ~EventSink() { bDone = true; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT 
        STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            LONG lObjectCount,
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};

#endif    // end of EventSink.h
```



<span data-ttu-id="7700e-134">El código de ejemplo siguiente es una implementación de la clase EventSink.</span><span class="sxs-lookup"><span data-stu-id="7700e-134">The following example code is an implementation of the EventSink class.</span></span>


```C++
// EventSink.cpp
#include "eventsink.h"

ULONG EventSink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG EventSink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT EventSink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT EventSink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        printf("Event occurred\n");
    }

    return WBEM_S_NO_ERROR;
}

HRESULT EventSink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    if(lFlags == WBEM_STATUS_COMPLETE)
    {
        printf("Call complete. hResult = 0x%X\n", hResult);
    }
    else if(lFlags == WBEM_STATUS_PROGRESS)
    {
        printf("Call in progress.\n");
    }

    return WBEM_S_NO_ERROR;
}    // end of EventSink.cpp
```



 

 
