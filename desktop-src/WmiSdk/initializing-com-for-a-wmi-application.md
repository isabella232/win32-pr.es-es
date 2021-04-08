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
# <a name="initializing-com-for-a-wmi-application"></a>Inicializar COM para una aplicación WMI

El primer paso para conectarse a WMI es configurar las llamadas COM a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



En el procedimiento siguiente se describe cómo inicializar COM desde una aplicación cliente.

**Para inicializar COM desde una aplicación cliente**

1.  Inicialice COM con una llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) es un procedimiento estándar para configurar una interfaz com. Por lo tanto, WMI no requiere que se respeten los procedimientos adicionales cuando se llama a **CoInitializeEx**. Para obtener más información, consulte [com](../com/component-object-model--com--portal.md).

    En el ejemplo de código siguiente se describe cómo llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Establezca los niveles de seguridad COM generales con una llamada a la interfaz [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) es una función estándar a la que se debe llamar al configurar una interfaz com para un proceso. Llame a **CoInitializeSecurity** si desea establecer la configuración de seguridad predeterminada para la autenticación, la suplantación o el servicio de autenticación para un proceso completo. Para obtener más información, vea [establecer la seguridad del proceso de aplicación cliente](setting-client-application-process-security.md). Si desea establecer o cambiar la seguridad de un proxy específico, debe llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Use **CoSetProxyBlanket** siempre que deba establecer o cambiar la seguridad com cuando se ejecute en otro proceso en el que no pueda controlar la configuración de seguridad predeterminada para la autenticación, la suplantación o el servicio de autenticación. Para obtener más información, vea [establecer los niveles de seguridad en una conexión WMI](setting-the-security-levels-on-a-wmi-connection.md) y [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

    WMI tiene varios problemas de seguridad que debe tener en cuenta al programar una aplicación cliente de WMI. Para obtener más información, vea [establecer la seguridad del proceso de aplicación cliente](setting-client-application-process-security.md).

    En el ejemplo de código siguiente se describe cómo llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de com en el proceso.

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

    

Después de inicializar COM, el paso siguiente consiste en crear una conexión a un espacio de nombres WMI. Para obtener más información, vea [crear una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
