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
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Limpieza y cierre de una aplicación WMI

Después de establecer los niveles de seguridad para el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , puede tener acceso a las diversas capacidades de WMI. Cuando termine de usar WMI, debe cerrar la aplicación.

En el procedimiento siguiente se describe cómo limpiar y cerrar una aplicación WMI.

**Para limpiar y cerrar una aplicación WMI**

1.  Libere cualquier interfaz COM abierta.

    Las dos interfaces principales que debe recordar para liberar son [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) y [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

2.  Llame a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

    Al igual que con todas las aplicaciones COM, debe llamar a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) al final de la aplicación.

3.  Salga de la aplicación.

    En el ejemplo de código siguiente se muestra cómo salir de una aplicación cliente de WMI.

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
    > La `pSvc` variable es de tipo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* y la variable PLoc es de tipo [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .

     

Ha inicializado correctamente COM, ha tenido acceso a WMI y ha salido de la aplicación. Para obtener más información, vea [ejemplo: crear una aplicación WMI](example-creating-a-wmi-application.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
