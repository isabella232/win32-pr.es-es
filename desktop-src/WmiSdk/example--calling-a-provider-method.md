---
description: Puede usar el procedimiento y los ejemplos de código de este tema para crear una aplicación cliente de WMI completa que realice la inicialización de COM, se conecte a WMI en el equipo local, llame a un método de proveedor y, a continuación, limpie.
ms.assetid: ee8faa14-74ec-49a2-88d6-187627c40071
ms.tgt_platform: multiple
title: 'Ejemplo: llamar a un método de proveedor'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa20d6e3a90b7d2f7826d7f62b4092bc18d2d917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360946"
---
# <a name="example-calling-a-provider-method"></a><span data-ttu-id="df5a2-103">Ejemplo: llamar a un método de proveedor</span><span class="sxs-lookup"><span data-stu-id="df5a2-103">Example: Calling a Provider Method</span></span>

<span data-ttu-id="df5a2-104">Puede usar el procedimiento y los ejemplos de código de este tema para crear una aplicación cliente de WMI completa que realice la inicialización de COM, se conecte a WMI en el equipo local, llame a un método de proveedor y, a continuación, limpie.</span><span class="sxs-lookup"><span data-stu-id="df5a2-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, calls a provider method, and then cleans up.</span></span> <span data-ttu-id="df5a2-105">El [**método \_ Process:: Create de Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) se usa para iniciar Notepad.exe en un nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="df5a2-105">The [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method is used to start Notepad.exe in a new process.</span></span>

<span data-ttu-id="df5a2-106">El siguiente procedimiento se utiliza para ejecutar la aplicación WMI.</span><span class="sxs-lookup"><span data-stu-id="df5a2-106">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="df5a2-107">Los pasos 1 a 5 contienen todos los pasos necesarios para configurar y conectarse a WMI, y 6 es donde se llama al método de proveedor.</span><span class="sxs-lookup"><span data-stu-id="df5a2-107">Steps 1 through 5 contain all of the steps needed to set up and connect to WMI, and 6 is where the provider method is called.</span></span>

<span data-ttu-id="df5a2-108">**Para llamar a un método de proveedor**</span><span class="sxs-lookup"><span data-stu-id="df5a2-108">**To call a provider method**</span></span>

1.  <span data-ttu-id="df5a2-109">Inicialice los parámetros COM con una llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="df5a2-109">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="df5a2-110">Para obtener más información, vea [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="df5a2-110">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="df5a2-111">Inicialice la seguridad del proceso COM llamando a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="df5a2-111">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="df5a2-112">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado mediante C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="df5a2-112">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="df5a2-113">Obtenga el localizador inicial de WMI llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="df5a2-113">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="df5a2-114">Para obtener más información, vea [crear una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="df5a2-114">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="df5a2-115">Obtenga un puntero a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para el espacio de nombres raíz de \\ cimv2 en el equipo local llamando a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="df5a2-115">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="df5a2-116">Para conectarse a un equipo remoto, vea [ejemplo: obtener datos WMI desde un equipo remoto](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="df5a2-116">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="df5a2-117">Para obtener más información, vea [crear una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="df5a2-117">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="df5a2-118">Establezca la seguridad de proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que el servicio WMI pueda suplantar al cliente mediante una llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="df5a2-118">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="df5a2-119">Para obtener más información, consulte [configuración de los niveles de seguridad en una conexión WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="df5a2-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="df5a2-120">Utilice el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para hacer solicitudes a WMI.</span><span class="sxs-lookup"><span data-stu-id="df5a2-120">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="df5a2-121">En este ejemplo se usa [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) para llamar al método de proveedor [**Win32 \_ Process:: Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="df5a2-121">This example uses [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to call the provider method [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span>

    <span data-ttu-id="df5a2-122">Para obtener más información sobre cómo realizar solicitudes a WMI, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md) y [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="df5a2-122">For more information about making requests to WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="df5a2-123">Si el método de proveedor tiene cualquier parámetro in-Parameters o out-Parameters, se deben asignar los valores de los parámetros a los punteros [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="df5a2-123">If the provider method has any in-parameters or out-parameters, then values of the parameters must be given to [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointers.</span></span> <span data-ttu-id="df5a2-124">En el caso de los parámetros in-, debe generar una instancia de las definiciones de los parámetros y, a continuación, establecer los valores de estas nuevas instancias.</span><span class="sxs-lookup"><span data-stu-id="df5a2-124">For in-parameters, you must spawn an instance of the in-parameter definitions, and then set the values of these new instances.</span></span> <span data-ttu-id="df5a2-125">El [**método \_ Process:: Create de Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) requiere un valor para que la *línea de comandos* en el parámetro se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="df5a2-125">The [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method requires a value for the *CommandLine* in-parameter to execute properly.</span></span>

    <span data-ttu-id="df5a2-126">En el ejemplo de código siguiente se crea un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , se genera una nueva instancia del [**proceso de Win32 \_ :: Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) en parámetros y, a continuación, se establece el valor de la *línea de comandos* en el parámetro en Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="df5a2-126">The following code example creates an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer, spawns a new instance of the [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) in-parameter definitions, and then sets the value of the *CommandLine* in-parameter to Notepad.exe.</span></span>

    ```C++
    // Set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in-parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in-parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));
    ```

    

    <span data-ttu-id="df5a2-127">En el ejemplo de código siguiente se muestra cómo se asignan a un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) el método [**\_ Process:: Create de Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) out-Parameters.</span><span class="sxs-lookup"><span data-stu-id="df5a2-127">The following code example shows how the [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method out-parameters are given to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer.</span></span> <span data-ttu-id="df5a2-128">El valor out-Parameter se obtiene con el método [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) y se almacena en una variable [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) para que se pueda mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="df5a2-128">The out-parameter value is obtained with the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method and stored in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable so that it can be displayed to the user.</span></span>

    ```C++
    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
        NULL, pClassInstance, &pOutParams, NULL);

    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);
    ```

    

<span data-ttu-id="df5a2-129">En el ejemplo de código siguiente se muestra cómo llamar a un método de proveedor mediante WMI.</span><span class="sxs-lookup"><span data-stu-id="df5a2-129">The following code example shows how to call a provider method using WMI.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

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
    // Set security levels for the proxy ------------------------

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

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));

    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
    NULL, pClassInstance, &pOutParams, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&varCommand);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pClassInstance->Release();
        pInParamsDefinition->Release();
        pOutParams->Release();
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // To see what the method returned,
    // use the following code.  The return value will
    // be in &varReturnValue
    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);


    // Clean up
    //--------------------------
    VariantClear(&varCommand);
    VariantClear(&varReturnValue);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pClassInstance->Release();
    pInParamsDefinition->Release();
    pOutParams->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



 

 
