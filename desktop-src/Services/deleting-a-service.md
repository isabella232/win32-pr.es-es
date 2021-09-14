---
description: Un programa de configuración de servicio usa la función OpenService para obtener un identificador para un objeto de servicio instalado. A continuación, el programa puede usar el identificador de objeto de servicio en la función DeleteService para eliminar el servicio de la base de datos de SCM.
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: Eliminación de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b1e0e95e0ea943487a0d3fa513afa2c0563d3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265060"
---
# <a name="deleting-a-service"></a>Eliminación de un servicio

Un [programa de configuración de](service-configuration-programs.md) servicio usa la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) para obtener un identificador para un objeto de servicio instalado. A continuación, el programa puede usar el identificador de objeto de servicio en la [**función DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para eliminar el servicio de la base de datos de SCM.

La función DoDeleteSvc del ejemplo siguiente muestra cómo eliminar un servicio de la base de datos de SCM. La variable szSvcName es una variable global que contiene el nombre del servicio que se va a eliminar. Para obtener el ejemplo completo que establece esta variable, vea [SvcConfig.cpp](svcconfig-cpp.md).


```C++
//
// Purpose: 
//   Deletes a service from the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDeleteSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_STATUS ssStatus; 

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,       // SCM database 
        szSvcName,          // name of service 
        DELETE);            // need delete access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Delete the service.
 
    if (! DeleteService(schService) ) 
    {
        printf("DeleteService failed (%d)\n", GetLastError()); 
    }
    else printf("Service deleted successfully\n"); 
 
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalación, eliminación y enumeración de servicios](service-installation-removal-and-enumeration.md)
</dt> <dt>

[Ejemplo de servicio completo](the-complete-service-sample.md)
</dt> </dl>

 

 



