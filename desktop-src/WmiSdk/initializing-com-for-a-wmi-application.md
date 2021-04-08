---
description: El primer paso para conectarse a WMI es configurar las llamadas COM a CoInitializeEx y CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Inicializar COM para una aplicación WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003011"
---
# <a name="initializing-com-for-a-wmi-application"></a><span data-ttu-id="6d498-103">Inicializar COM para una aplicación WMI</span><span class="sxs-lookup"><span data-stu-id="6d498-103">Initializing COM for a WMI Application</span></span>

<span data-ttu-id="6d498-104">El primer paso para conectarse a WMI es configurar las llamadas COM a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="6d498-104">The first step in connecting to WMI is setting up the COM calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="6d498-105">Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="6d498-105">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="6d498-106">En el procedimiento siguiente se describe cómo inicializar COM desde una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="6d498-106">The following procedure describes how to initialize COM from a client application.</span></span>

<span data-ttu-id="6d498-107">**Para inicializar COM desde una aplicación cliente**</span><span class="sxs-lookup"><span data-stu-id="6d498-107">**To initialize COM from a client application**</span></span>

1.  <span data-ttu-id="6d498-108">Inicialice COM con una llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="6d498-108">Initialize COM with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="6d498-109">Llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) es un procedimiento estándar para configurar una interfaz com.</span><span class="sxs-lookup"><span data-stu-id="6d498-109">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) is a standard procedure for setting up a COM interface.</span></span> <span data-ttu-id="6d498-110">Por lo tanto, WMI no requiere que se respeten los procedimientos adicionales cuando se llama a **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="6d498-110">Therefore, WMI does not require that you observe any additional procedures when calling **CoInitializeEx**.</span></span> <span data-ttu-id="6d498-111">Para obtener más información, consulte [com](../com/component-object-model--com--portal.md).</span><span class="sxs-lookup"><span data-stu-id="6d498-111">For more information, see [COM](../com/component-object-model--com--portal.md).</span></span>

    <span data-ttu-id="6d498-112">En el ejemplo de código siguiente se describe cómo llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="6d498-112">The following code example describes how to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  <span data-ttu-id="6d498-113">Establezca los niveles de seguridad COM generales con una llamada a la interfaz [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="6d498-113">Set the general COM security levels with a call to the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interface.</span></span>

    <span data-ttu-id="6d498-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) es una función estándar a la que se debe llamar al configurar una interfaz com para un proceso.</span><span class="sxs-lookup"><span data-stu-id="6d498-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a standard function you must call when setting up a COM interface for a process.</span></span> <span data-ttu-id="6d498-115">Llame a **CoInitializeSecurity** si desea establecer la configuración de seguridad predeterminada para la autenticación, la suplantación o el servicio de autenticación para un proceso completo.</span><span class="sxs-lookup"><span data-stu-id="6d498-115">Call **CoInitializeSecurity** if you want to set the default security settings for authentication, impersonation, or authentication service for an entire process.</span></span> <span data-ttu-id="6d498-116">Para obtener más información, vea [establecer la seguridad del proceso de aplicación cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="6d498-116">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="6d498-117">Si desea establecer o cambiar la seguridad de un proxy específico, debe llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="6d498-117">If you want to set or change the security for a specific proxy, you must call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="6d498-118">Use **CoSetProxyBlanket** siempre que deba establecer o cambiar la seguridad com cuando se ejecute en otro proceso en el que no pueda controlar la configuración de seguridad predeterminada para la autenticación, la suplantación o el servicio de autenticación.</span><span class="sxs-lookup"><span data-stu-id="6d498-118">Use **CoSetProxyBlanket** whenever you must set or change COM security when running inside another process where you cannot control the default security settings for authentication, impersonation, or authentication service.</span></span> <span data-ttu-id="6d498-119">Para obtener más información, vea [establecer los niveles de seguridad en una conexión WMI](setting-the-security-levels-on-a-wmi-connection.md) y [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="6d498-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

    <span data-ttu-id="6d498-120">WMI tiene varios problemas de seguridad que debe tener en cuenta al programar una aplicación cliente de WMI.</span><span class="sxs-lookup"><span data-stu-id="6d498-120">WMI has several security issues you should be aware of when programming a WMI client application.</span></span> <span data-ttu-id="6d498-121">Para obtener más información, vea [establecer la seguridad del proceso de aplicación cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="6d498-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

    <span data-ttu-id="6d498-122">En el ejemplo de código siguiente se describe cómo llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de com en el proceso.</span><span class="sxs-lookup"><span data-stu-id="6d498-122">The following code example describes how to call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set COM security on the process.</span></span>

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

<span data-ttu-id="6d498-123">Después de inicializar COM, el paso siguiente consiste en crear una conexión a un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="6d498-123">After you initialize COM, your next step is to create a connection to a WMI namespace.</span></span> <span data-ttu-id="6d498-124">Para obtener más información, vea [crear una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="6d498-124">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d498-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d498-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d498-126">Crear una aplicación WMI con C++</span><span class="sxs-lookup"><span data-stu-id="6d498-126">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="6d498-127">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="6d498-127">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
