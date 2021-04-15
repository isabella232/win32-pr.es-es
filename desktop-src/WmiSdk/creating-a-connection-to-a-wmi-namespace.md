---
description: 'Después de haber establecido las llamadas estándar a COM, debe conectarse a WMI a través de una llamada al método IWbemLocator:: ConnectServer.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Crear una conexión a un espacio de nombres WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498059"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>Crear una conexión a un espacio de nombres WMI

Después de haber establecido las llamadas estándar a COM, debe conectarse a WMI a través de una llamada al método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . El método **ConnectServer** devuelve un proxy de una interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . A través de **IWbemServices**, puede tener acceso a las diferentes capacidades de WMI.

Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



En el procedimiento siguiente se describe cómo crear una conexión a un espacio de nombres WMI.

**Para crear una conexión a un espacio de nombres WMI**

-   Inicialice la interfaz [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) a través de una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    WMI no requiere que realice ningún procedimiento adicional al llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    En el ejemplo de código siguiente se describe cómo inicializar [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   Conéctese a WMI a través de una llamada al método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .

        El método [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) devuelve un proxy a una interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que usa para tener acceso al espacio de nombres WMI local o remoto especificado en la llamada a **ConnectServer**.

        En el ejemplo de código siguiente se describe cómo llamar a [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

Una vez que haya recibido un puntero al proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , debe establecer la seguridad en el proxy para tener acceso a WMI. Para obtener más información, consulte [configuración de los niveles de seguridad en una conexión WMI](setting-the-security-levels-on-a-wmi-connection.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
