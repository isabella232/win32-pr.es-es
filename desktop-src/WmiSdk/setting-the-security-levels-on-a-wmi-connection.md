---
description: Después de recuperar un puntero a un proxy IWbemServices, debe establecer la seguridad en el proxy para tener acceso a WMI a través del proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Establecer los niveles de seguridad en una conexión WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717039"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Establecer los niveles de seguridad en una conexión WMI

Después de recuperar un puntero a un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , debe establecer la seguridad en el proxy para tener acceso a WMI a través del proxy. Debe establecer la seguridad porque el proxy **IWbemServices** concede acceso a un objeto fuera de proceso. En general, la seguridad COM no permite que un proceso tenga acceso a otro proceso si no se establecen las propiedades de seguridad adecuadas. Para obtener más información, vea [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md). Las conexiones a diferentes sistemas operativos requieren distintos niveles de autenticación y suplantación. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



En el procedimiento siguiente se describe cómo establecer los niveles de seguridad en una conexión WMI.

**Para establecer los niveles de seguridad en una conexión WMI**

-   Establezca los niveles de seguridad en el proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    En el ejemplo de código siguiente se describe una manera común de llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

Después de establecer los niveles de seguridad para el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , puede tener acceso a las diversas capacidades de WMI. Cuando termine de usar WMI, debe cerrar la aplicación. Para obtener más información, consulte [limpiar y apagar una aplicación WMI](cleaning-up-and-shutting-down-a-wmi-application.md).

 

 
