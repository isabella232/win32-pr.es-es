---
description: Después de establecer los niveles de seguridad para el puntero IWbemServices, puede acceder a las distintas funcionalidades de WMI. Cuando termine de usar WMI, debe apagar la aplicación.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Limpieza y apagado de una aplicación WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d2093b16491bcb600438d781fa833a09754fdc5d0cc8cc83feb710a6d2727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120915"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Limpieza y apagado de una aplicación WMI

Después de establecer los niveles de seguridad para el [**puntero IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) puede acceder a las distintas funcionalidades de WMI. Cuando termine de usar WMI, debe apagar la aplicación.

En el procedimiento siguiente se describe cómo limpiar y apagar una aplicación WMI.

**Para limpiar y apagar una aplicación WMI**

1.  Libere las interfaces COM abiertas.

    Las dos interfaces principales que debe recordar liberar son [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)

2.  Llame [**a CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

    Al igual que con todas las aplicaciones COM, debe llamar a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) al final de la aplicación.

3.  Salga de la aplicación.

    En el ejemplo de código siguiente se muestra cómo salir de una aplicación cliente WMI.

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
    > La `pSvc` variable es de tipo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* y la variable pLoc es de tipo [**IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \*

     

Ahora ha inicializado correctamente COM, ha accedido a WMI y ha salido de la aplicación. Para obtener más información, vea [Ejemplo: Crear una aplicación WMI.](example-creating-a-wmi-application.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una aplicación WMI mediante C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
