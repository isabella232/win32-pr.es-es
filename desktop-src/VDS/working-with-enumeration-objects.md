---
description: Trabajar con objetos de enumeración
ms.assetid: cb99e9fd-613c-4e38-9e0f-e1a23b72aa07
title: Trabajar con objetos de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df90548ef060d537faff206e45e0cf74630cdfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677973"
---
# <a name="working-with-enumeration-objects"></a>Trabajar con objetos de enumeración

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

En el ejemplo de código siguiente se muestra cómo un llamador trabaja con objetos de enumeración mediante la interfaz [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) . Tenga en cuenta que la información devuelta por un objeto de enumeración es estática. Debe consultar el objeto de nuevo para ver los nuevos cambios de configuración.

La función **GetControllerById** toma una interfaz [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) , especificada por el parámetro *pSubsystem* , y consulta los controladores del subsistema y, a continuación, recorre en iteración la enumeración devuelta buscando un controlador con un GUID que coincida con el GUID especificado por el parámetro *pControllerId* . Si se encuentra un controlador coincidente, lo devuelve el parámetro *ppController* junto con un \_ **HRESULT** S correcto.


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT GetControllerById(
         IN IVdsSubSystem       *pSubsystem,
         IN CONST VDS_OBJECT_ID *pControllerId,
         OUT IVdsController     **ppController)
{
    VDS_CONTROLLER_PROP vdsControllerProperties;
    IEnumVdsObject      *pEnumController = NULL;
    IVdsController      *pController     = NULL;
    IUnknown            *pUnknown        = NULL;
    HRESULT             hResult          = S_OK;
    ULONG               ulFetched        = 0;
    BOOL                bDone            = FALSE;

    ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));

    // Query for the enumeration of controllers belonging
    // to the given subsystem.
    hResult = pSubsystem->QueryControllers(&pEnumController);

    if (SUCCEEDED(hResult) && (!pEnumController)) 
    {
        hResult = E_UNEXPECTED; // Errant provider, 
        // returned S_OK 
        // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) 
    {
        // Enumerate through all the controllers this subsystem 
        // contains to find the controller of interest.
        while (!bDone) 
        {
            ulFetched = 0;
            hResult = pEnumController->Next(1, &pUnknown, &ulFetched);

            if (hResult == S_FALSE) 
            {
                hResult = E_INVALIDARG;
                break;
            }

            if (SUCCEEDED(hResult) && (!pUnknown)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK with
                // a NULL pointer 
            }

            // Use an IVdsController interface to get the controller 
            // properties and check for the desired GUID.
            if (SUCCEEDED(hResult)) 
            {
                hResult = pUnknown->QueryInterface(IID_IVdsController,  
                    (void **) &pController);
            }

            if (SUCCEEDED(hResult) && (!pController)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK 
                // with a NULL pointer
            }

            if (SUCCEEDED(hResult)) 
            {
                hResult = pController->  
                GetProperties( &vdsControllerProperties);
            }

            if (SUCCEEDED(hResult) 
                && IsEqualGUID(*pControllerId, vdsControllerProperties.id)) 
            {
                bDone = TRUE;
            } 
            else 
            {
                _SafeRelease(pController);
            }

            _SafeRelease(pUnknown);

            //Free the strings in the properties structure.
            if (NULL != vdsControllerProperties.pwszIdentification) 
            {
                CoTaskMemFree(vdsControllerProperties.pwszIdentification);
            }

            ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));
        }
    }

    if (SUCCEEDED(hResult)) 
    {
        *ppController = pController;
    }

    _SafeRelease(pEnumController);
    return hResult;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VDS](using-vds.md)
</dt> <dt>

[Objetos auxiliares](helper-objects.md)
</dt> <dt>

[**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)
</dt> <dt>

[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)
</dt> </dl>

 

 
