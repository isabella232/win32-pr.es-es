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
# <a name="creating-a-connection-to-a-wmi-namespace"></a><span data-ttu-id="042a1-103">Crear una conexión a un espacio de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="042a1-103">Creating a Connection to a WMI Namespace</span></span>

<span data-ttu-id="042a1-104">Después de haber establecido las llamadas estándar a COM, debe conectarse a WMI a través de una llamada al método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="042a1-104">After you have set the standard calls to COM, you must then connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span> <span data-ttu-id="042a1-105">El método **ConnectServer** devuelve un proxy de una interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="042a1-105">The **ConnectServer** method returns a proxy of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="042a1-106">A través de **IWbemServices**, puede tener acceso a las diferentes capacidades de WMI.</span><span class="sxs-lookup"><span data-stu-id="042a1-106">Through **IWbemServices**, you can access the different capabilities of WMI.</span></span>

<span data-ttu-id="042a1-107">Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="042a1-107">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="042a1-108">En el procedimiento siguiente se describe cómo crear una conexión a un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="042a1-108">The following procedure describes how to create a connection to a WMI namespace.</span></span>

<span data-ttu-id="042a1-109">**Para crear una conexión a un espacio de nombres WMI**</span><span class="sxs-lookup"><span data-stu-id="042a1-109">**To create a connection to a WMI namespace**</span></span>

-   <span data-ttu-id="042a1-110">Inicialice la interfaz [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) a través de una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="042a1-110">Initialize the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface through a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="042a1-111">WMI no requiere que realice ningún procedimiento adicional al llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="042a1-111">WMI does not require that you perform any additional procedures when calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    <span data-ttu-id="042a1-112">En el ejemplo de código siguiente se describe cómo inicializar [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="042a1-112">The following code example describes how to initialize [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

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

    

    -   <span data-ttu-id="042a1-113">Conéctese a WMI a través de una llamada al método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="042a1-113">Connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span>

        <span data-ttu-id="042a1-114">El método [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) devuelve un proxy a una interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que usa para tener acceso al espacio de nombres WMI local o remoto especificado en la llamada a **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="042a1-114">The [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method returns a proxy to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface that use to access the local or remote WMI namespace specified in your call to **ConnectServer**.</span></span>

        <span data-ttu-id="042a1-115">En el ejemplo de código siguiente se describe cómo llamar a [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="042a1-115">The following code example describes how to call [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

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

        

<span data-ttu-id="042a1-116">Una vez que haya recibido un puntero al proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , debe establecer la seguridad en el proxy para tener acceso a WMI.</span><span class="sxs-lookup"><span data-stu-id="042a1-116">After you have received a pointer to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI.</span></span> <span data-ttu-id="042a1-117">Para obtener más información, consulte [configuración de los niveles de seguridad en una conexión WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="042a1-117">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="042a1-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="042a1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="042a1-119">Crear una aplicación WMI con C++</span><span class="sxs-lookup"><span data-stu-id="042a1-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="042a1-120">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="042a1-120">IPv6 and IPv4 Support in WMI</span></span>](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
