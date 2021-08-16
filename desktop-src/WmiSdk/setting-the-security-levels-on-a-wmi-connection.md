---
description: Después de recuperar un puntero a un proxy IWbemServices, debe establecer la seguridad en el proxy para acceder a WMI a través del proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Establecer los niveles de seguridad en una conexión WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c2c4a492d4b40410b42fd9a94f22d346617a84d3baaa0679db325452a69c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315329"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Establecer los niveles de seguridad en una conexión WMI

Después de recuperar un puntero a un proxy [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) debe establecer la seguridad en el proxy para acceder a WMI a través del proxy. Debe establecer la seguridad porque el proxy **IWbemServices** concede acceso a un objeto fuera de proceso. En general, la seguridad COM no permite que un proceso acceda a otro proceso si no establece las propiedades de seguridad adecuadas. Para obtener más información, vea [Establecer la seguridad en IWbemServices y otros servidores proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md) Las conexiones a diferentes sistemas operativos requieren distintos niveles de autenticación y suplantación. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

Los ejemplos de código de este tema requieren las siguientes referencias e \# instrucciones include para compilarse correctamente.


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

    

Después de establecer los niveles de seguridad para el [**puntero IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) puede acceder a las distintas funcionalidades de WMI. Cuando termine de usar WMI, debe apagar la aplicación. Para obtener más información, vea [Limpieza y apagado de una aplicación WMI.](cleaning-up-and-shutting-down-a-wmi-application.md)

 

 
