---
description: Un programa de configuración de servicio utiliza la función OpenService para obtener un identificador de un objeto de servicio instalado. A continuación, el programa puede utilizar el identificador de objeto de servicio en la función actividades para eliminar el servicio de la base de datos SCM.
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: Eliminación de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b1e0e95e0ea943487a0d3fa513afa2c0563d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002656"
---
# <a name="deleting-a-service"></a><span data-ttu-id="84c8f-104">Eliminación de un servicio</span><span class="sxs-lookup"><span data-stu-id="84c8f-104">Deleting a Service</span></span>

<span data-ttu-id="84c8f-105">Un [programa de configuración de servicio](service-configuration-programs.md) utiliza la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) para obtener un identificador de un objeto de servicio instalado.</span><span class="sxs-lookup"><span data-stu-id="84c8f-105">A [service configuration program](service-configuration-programs.md) uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function to get a handle to an installed service object.</span></span> <span data-ttu-id="84c8f-106">A continuación, el programa puede utilizar el identificador de objeto de servicio en la función [**actividades**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para eliminar el servicio de la base de datos SCM.</span><span class="sxs-lookup"><span data-stu-id="84c8f-106">The program can then use the service object handle in the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service from the SCM database.</span></span>

<span data-ttu-id="84c8f-107">La función DoDeleteSvc del ejemplo siguiente muestra cómo eliminar un servicio de la base de datos SCM.</span><span class="sxs-lookup"><span data-stu-id="84c8f-107">The DoDeleteSvc function in the following example shows how to delete a service from the SCM database.</span></span> <span data-ttu-id="84c8f-108">La variable szSvcName es una variable global que contiene el nombre del servicio que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="84c8f-108">The szSvcName variable is a global variable that contains the name of the service to be deleted.</span></span> <span data-ttu-id="84c8f-109">Para obtener el ejemplo completo en el que se establece esta variable, vea [SvcConfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="84c8f-109">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="84c8f-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84c8f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84c8f-111">Instalación, eliminación y enumeración del servicio</span><span class="sxs-lookup"><span data-stu-id="84c8f-111">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> <dt>

[<span data-ttu-id="84c8f-112">El ejemplo de servicio completo</span><span class="sxs-lookup"><span data-stu-id="84c8f-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



