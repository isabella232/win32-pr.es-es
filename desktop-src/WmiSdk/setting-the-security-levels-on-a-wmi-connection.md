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
# <a name="setting-the-security-levels-on-a-wmi-connection"></a><span data-ttu-id="293fc-103">Establecer los niveles de seguridad en una conexión WMI</span><span class="sxs-lookup"><span data-stu-id="293fc-103">Setting the Security Levels on a WMI Connection</span></span>

<span data-ttu-id="293fc-104">Después de recuperar un puntero a un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , debe establecer la seguridad en el proxy para tener acceso a WMI a través del proxy.</span><span class="sxs-lookup"><span data-stu-id="293fc-104">After you retrieve a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI through the proxy.</span></span> <span data-ttu-id="293fc-105">Debe establecer la seguridad porque el proxy **IWbemServices** concede acceso a un objeto fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="293fc-105">You must set the security because the **IWbemServices** proxy grants access to an out-of-process object.</span></span> <span data-ttu-id="293fc-106">En general, la seguridad COM no permite que un proceso tenga acceso a otro proceso si no se establecen las propiedades de seguridad adecuadas.</span><span class="sxs-lookup"><span data-stu-id="293fc-106">In general, COM security does not allow one process to access another process if you do not set the proper security properties.</span></span> <span data-ttu-id="293fc-107">Para obtener más información, vea [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="293fc-107">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span> <span data-ttu-id="293fc-108">Las conexiones a diferentes sistemas operativos requieren distintos niveles de autenticación y suplantación.</span><span class="sxs-lookup"><span data-stu-id="293fc-108">Connections to different operating systems require varying levels of authentication and impersonation.</span></span> <span data-ttu-id="293fc-109">Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).</span><span class="sxs-lookup"><span data-stu-id="293fc-109">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="293fc-110">Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="293fc-110">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="293fc-111">En el procedimiento siguiente se describe cómo establecer los niveles de seguridad en una conexión WMI.</span><span class="sxs-lookup"><span data-stu-id="293fc-111">The following procedure describes how to set the security levels on a WMI connection.</span></span>

<span data-ttu-id="293fc-112">**Para establecer los niveles de seguridad en una conexión WMI**</span><span class="sxs-lookup"><span data-stu-id="293fc-112">**To set the security levels on a WMI connection**</span></span>

-   <span data-ttu-id="293fc-113">Establezca los niveles de seguridad en el proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="293fc-113">Set the security levels on the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="293fc-114">En el ejemplo de código siguiente se describe una manera común de llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="293fc-114">The following code example describes a common way of calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

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

    

<span data-ttu-id="293fc-115">Después de establecer los niveles de seguridad para el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , puede tener acceso a las diversas capacidades de WMI.</span><span class="sxs-lookup"><span data-stu-id="293fc-115">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="293fc-116">Cuando termine de usar WMI, debe cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="293fc-116">After you finish using WMI, you must shut down your application.</span></span> <span data-ttu-id="293fc-117">Para obtener más información, consulte [limpiar y apagar una aplicación WMI](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="293fc-117">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

 

 
