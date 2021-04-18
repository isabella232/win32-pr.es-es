---
description: Cargando VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Cargando VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697372"
---
# <a name="loading-vds"></a>Cargando VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

**Para cargar e inicializar VDS**

1.  Liberar interfaces que no sean null.
2.  Llame a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)o [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) para obtener un puntero al objeto de cargador de servicios.

    **CLSCTX \_ No \_** se puede especificar AAA en esta llamada. Si se llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , no se puede especificar **EOAC \_ Disable \_ AAA** en el parámetro *dwCapabilities* .

3.  Llame al método [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para cargar Vds.

    Pasar **null** como primer parámetro carga e inicializa VDS en el host local.

4.  Llame al método [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) para esperar a que se complete la inicialización de Vds.

En el ejemplo de código siguiente se inicializa el servicio que devuelve un puntero al objeto de servicio.


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VDS](using-vds.md)
</dt> <dt>

[**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Configuración y objetos de servicio](startup-and-service-objects.md)
</dt> </dl>

 

 
