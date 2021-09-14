---
description: Carga de VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Carga de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071014"
---
# <a name="loading-vds"></a>Carga de VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se [reemplaza por el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

**Para cargar e inicializar VDS**

1.  Liberar interfaces que no son null.
2.  Llame a [**la función CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)o [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) para obtener un puntero al objeto del cargador de servicios.

    **CLSCTX \_ DISABLE \_ AAA** no se puede especificar en esta llamada. Si [**se llama a CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) no se puede especificar **EOAC \_ DISABLE \_ AAA** en el *parámetro dwCapabilities.*

3.  Llame al [**método IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para cargar VDS.

    Al **pasar NULL** como primer parámetro, se carga e inicializa VDS en el host local.

4.  Llame al [**método IVdsService::WaitForServiceReady para**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) esperar a que se complete la inicialización de VDS.

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

[Instalación y objetos de servicio](startup-and-service-objects.md)
</dt> </dl>

 

 
