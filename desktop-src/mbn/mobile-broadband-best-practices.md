---
description: Al trabajar con la API de banda ancha móvil, se debe usar el siguiente conjunto de prácticas recomendadas para lograr el mejor rendimiento posible.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Procedimientos recomendados de API de banda ancha móvil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275507"
---
# <a name="mobile-broadband-api-best-practices"></a>Procedimientos recomendados de API de banda ancha móvil

Al trabajar con la API de banda ancha móvil, se debe usar el siguiente conjunto de prácticas recomendadas para lograr el mejor rendimiento posible.

## <a name="do-not-cache-functional-objects"></a>No almacenar en caché objetos funcionales

Los objetos funcionales, como [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) y otros, se obtienen de los objetos de administrador, como [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), mediante el método de enumeración en el objeto de administrador correspondiente. No almacene en caché estos objetos funcionales, ya que los objetos funcionales almacenados en caché contienen datos obsoletos. Las operaciones sincrónicas realizadas en estos objetos funcionales devolverán los mismos datos hasta que se obtengan de nuevo los objetos funcionales.

En su lugar, almacene en caché los objetos de administrador y obtenga los objetos funcionales del objeto de administrador mediante el método de enumeración en el objeto de administrador correspondiente de nuevo para obtener los datos más recientes.

En el ejemplo de código siguiente se muestra la manera adecuada de almacenar en memoria caché los objetos de administrador.


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a>Control de todas las notificaciones

Siga y controle todas las notificaciones, incluso si la aplicación no la desencadena. Esto es necesario para mantener la interfaz de usuario sincronizada con el estado real del dispositivo.

Puede haber más de un administrador de conexiones que se ejecute en un equipo. La interfaz de usuario de la interfaz de red disponible de vista nativa proporcionada por Windows 7 es un administrador de conexiones. Cualquier otro administrador de conexiones debe responder a todas las notificaciones para permanecer sincronizando la interfaz de usuario nativa de Windows. Un usuario puede optar por realizar alguna operación en uno de los administradores de conexiones, lo que puede dar lugar a un cambio de estado del dispositivo de banda ancha móvil. Sin embargo, otros administradores de conexiones deben permanecer actualizados para indicar correctamente el estado modificado del dispositivo.

Por ejemplo, si realiza una conexión mediante uno de los administradores de conexiones, cambiará el estado del dispositivo de disponible a conectado. Este cambio debe estar visible para los administradores de conexión que no iniciaron esta acción. Todos los administradores de conexión que tienen una interfaz de usuario que indica el estado de conexión del dispositivo, deben escuchar y controlar las notificaciones de estado de conexión para actualizar correctamente su interfaz de usuario.

## <a name="sending-and-receiving-bytes"></a>Envío y recepción de bytes

Use las funciones auxiliares de IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) y [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) para enviar y recibir bytes.

## <a name="using-the-pin-unblock-api"></a>Uso de la API de PIN desbloqueado

Una aplicación cliente de llamada debe elevarse para poder invocar correctamente [**IMbnPin:: unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock). Este método es la única parte de la API de banda ancha móvil que requiere privilegios de administrador o NCO. Para obtener más información, vea [una descripción del grupo operadores de configuración de red]( https://support.microsoft.com/kb/297938/en-us) .

## <a name="working-with-safearrays"></a>Trabajar con SafeArray

-   Use ZeroMemory () antes de tener acceso a los elementos de un SafeArray.

-   No Compruebe los índices de una SafeArray. Pueden ser negativos.

En el ejemplo de código siguiente se muestra cómo administrar correctamente una SafeArray.


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
