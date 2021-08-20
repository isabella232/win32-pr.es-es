---
description: Al trabajar con Mobile Broadband API, se debe usar el siguiente conjunto de procedimientos recomendados para lograr el mejor rendimiento posible.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Procedimientos recomendados de la API de banda ancha móvil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3a6c1e236a61dd2a5321be2edb7a68156f904605bd8a1da5fc169ea8b70e464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881659"
---
# <a name="mobile-broadband-api-best-practices"></a>Procedimientos recomendados de la API de banda ancha móvil

Al trabajar con Mobile Broadband API, se debe usar el siguiente conjunto de procedimientos recomendados para lograr el mejor rendimiento posible.

## <a name="do-not-cache-functional-objects"></a>No almacenar en caché objetos funcionales

Los objetos funcionales, como [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) y otros, se obtienen de objetos de administrador, como [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), mediante el método de enumeración en el objeto de administrador correspondiente. No almacene en caché estos objetos funcionales, ya que los objetos funcionales almacenados en caché contienen datos obsoletos. Las operaciones sincrónicas realizadas en estos objetos funcionales devolverán los mismos datos hasta que se vuelvan a obtener los objetos funcionales.

En su lugar, almacenar en caché los objetos de administrador y obtener los objetos funcionales del objeto de administrador mediante el método de enumeración en el objeto de administrador correspondiente de nuevo para obtener los datos más recientes.

En el ejemplo de código siguiente se muestra la manera adecuada de almacenar en caché los objetos del administrador.


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



## <a name="handle-all-notifications"></a>Controlar todas las notificaciones

Siga y controle todas las notificaciones, incluso si la aplicación no las desencadena. Esto es necesario para mantener la interfaz de usuario sincronizada con el estado real del dispositivo.

Puede haber más de un administrador de conexiones ejecutándose en un equipo. La interfaz de usuario nativa ver interfaz de red disponible proporcionada por Windows 7 es un administrador de conexiones. Los demás administradores de conexiones deben responder a todas las notificaciones para que permanezcan sincronizados con Windows interfaz de usuario nativa. Un usuario puede optar por realizar alguna operación en uno de los administradores de conexión, lo que puede dar lugar a un cambio de estado del dispositivo de banda ancha móvil. Sin embargo, otros administradores de conexiones deben permanecer actualizados para indicar correctamente el estado modificado del dispositivo.

Por ejemplo, realizar una conexión mediante uno de los administradores de conexión cambiará el estado del dispositivo de disponible a conectado. Este cambio debe ser visible para los administradores de conexiones que no iniciaron esta acción. Todos los administradores de conexiones que tengan una interfaz de usuario que indique el estado de conexión del dispositivo deben escuchar y controlar las notificaciones de estado de conexión para actualizar correctamente su interfaz de usuario.

## <a name="sending-and-receiving-bytes"></a>Enviar y recibir bytes

Use las funciones del asistente de IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) y [GetlfEntry2 para](/windows/win32/api/netioapi/nf-netioapi-getifentry2) enviar y recibir bytes.

## <a name="using-the-pin-unblock-api"></a>Uso de la API Anclar desbloqueo

Una aplicación cliente que realiza la llamada debe tener privilegios elevados para invocar correctamente [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock). Este método es la única parte de Mobile Broadband API que requiere privilegios de administrador o NCO. Consulte [Una descripción del grupo de operadores de configuración de red]( https://support.microsoft.com/kb/297938/en-us) para obtener más información.

## <a name="working-with-safearrays"></a>Trabajar con SafeArrays

-   Use ZeroMemory() antes de acceder a los elementos de una safeArray.

-   No compruebe los índices de una safeArray. Pueden ser negativos.

En el ejemplo de código siguiente se muestra cómo controlar correctamente safeArray.


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



 

 
