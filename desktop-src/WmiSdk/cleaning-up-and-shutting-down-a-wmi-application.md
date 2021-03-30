---
description: Después de establecer los niveles de seguridad para el puntero IWbemServices, puede tener acceso a las diversas capacidades de WMI. Cuando termine de usar WMI, debe cerrar la aplicación.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Limpieza y cierre de una aplicación WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002437"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a><span data-ttu-id="aa95f-104">Limpieza y cierre de una aplicación WMI</span><span class="sxs-lookup"><span data-stu-id="aa95f-104">Cleaning up and Shutting Down a WMI Application</span></span>

<span data-ttu-id="aa95f-105">Después de establecer los niveles de seguridad para el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , puede tener acceso a las diversas capacidades de WMI.</span><span class="sxs-lookup"><span data-stu-id="aa95f-105">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="aa95f-106">Cuando termine de usar WMI, debe cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aa95f-106">After you finish using WMI, you must shut down your application.</span></span>

<span data-ttu-id="aa95f-107">En el procedimiento siguiente se describe cómo limpiar y cerrar una aplicación WMI.</span><span class="sxs-lookup"><span data-stu-id="aa95f-107">The following procedure describes how to clean up and shut down a WMI application.</span></span>

<span data-ttu-id="aa95f-108">**Para limpiar y cerrar una aplicación WMI**</span><span class="sxs-lookup"><span data-stu-id="aa95f-108">**To clean up and shut down a WMI application**</span></span>

1.  <span data-ttu-id="aa95f-109">Libere cualquier interfaz COM abierta.</span><span class="sxs-lookup"><span data-stu-id="aa95f-109">Release any open COM interfaces.</span></span>

    <span data-ttu-id="aa95f-110">Las dos interfaces principales que debe recordar para liberar son [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) y [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="aa95f-110">The two primary interfaces you must remember to release are [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

2.  <span data-ttu-id="aa95f-111">Llame a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="aa95f-111">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

    <span data-ttu-id="aa95f-112">Al igual que con todas las aplicaciones COM, debe llamar a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) al final de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aa95f-112">As with all COM applications, you must call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) at the end of your application.</span></span>

3.  <span data-ttu-id="aa95f-113">Salga de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aa95f-113">Exit your application.</span></span>

    <span data-ttu-id="aa95f-114">En el ejemplo de código siguiente se muestra cómo salir de una aplicación cliente de WMI.</span><span class="sxs-lookup"><span data-stu-id="aa95f-114">The following code example shows how to exit a WMI client application.</span></span>

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > <span data-ttu-id="aa95f-115">La `pSvc` variable es de tipo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* y la variable PLoc es de tipo [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .</span><span class="sxs-lookup"><span data-stu-id="aa95f-115">The `pSvc` variable is of type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)\*, and the pLoc variable is of type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)\*.</span></span>

     

<span data-ttu-id="aa95f-116">Ha inicializado correctamente COM, ha tenido acceso a WMI y ha salido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aa95f-116">You have now successfully initialized COM, accessed WMI, and exited your application.</span></span> <span data-ttu-id="aa95f-117">Para obtener más información, vea [ejemplo: crear una aplicación WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="aa95f-117">For more information, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa95f-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa95f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa95f-119">Crear una aplicación WMI con C++</span><span class="sxs-lookup"><span data-stu-id="aa95f-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
