---
title: Palabras clave dinámicas del firewall
description: Las API de palabras clave dinámicas del firewall se usan para administrar direcciones de palabras clave dinámicas Firewall de Microsoft Defender.
keywords:
- Palabras clave dinámicas del firewall
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: 15e35f26b72ed8d685e8302f6222836507e5c6a3
ms.sourcegitcommit: ae8c320a757558262167a4f4e385235b8d89035c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112765539"
---
# <a name="firewall-dynamic-keywords"></a>Palabras clave dinámicas del firewall

Las API de palabras clave dinámicas del firewall se usan para administrar direcciones de *palabras clave dinámicas* [Firewall de Microsoft Defender](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security). Una dirección de palabra clave dinámica se usa para crear un conjunto de direcciones IP a las que puede hacer referencia una o varias reglas de firewall. Las direcciones de palabras clave dinámicas admiten IPv4 e IPv6.

> [!NOTE]
> Para obtener contenido de referencia de API para las API introducidas en este tema, consulte [Referencia de palabras clave dinámicas de firewall.](firewall-dynamic-keywords-reference.md)

## <a name="operations-on-dynamic-keyword-addresses"></a>Operaciones en direcciones de palabras clave dinámicas

Con las API de palabras clave dinámicas del firewall, puede realizar las siguientes operaciones.

* Adición de direcciones de palabras clave dinámicas
* Eliminación de direcciones de palabras clave dinámicas
* Enumerar direcciones de palabras clave dinámicas por identificador o por tipo
* Actualización de direcciones de palabras clave dinámicas
* Suscripción y control de notificaciones de cambio de dirección de palabras clave dinámicas

Hay ejemplos de código para todas esas operaciones más adelante en este tema.

Una vez que haya agregado una dirección de palabra clave dinámica, se conserva entre reinicios. Debe eliminar una dirección de palabra clave dinámica una vez que haya terminado con el objeto .

Hay dos clases de direcciones de palabras clave dinámicas, como se describe en las dos secciones siguientes.

## <a name="autoresolve-dynamic-keyword-addresses"></a>Direcciones de palabras clave dinámicas de AutoResolve

El primer tipo es *AutoResolve*, donde el campo de palabra clave representa un nombre que se puede resolver y las direcciones IP no se definen al crearse. 

Estos objetos están diseñados para que sus direcciones IP se resuelvan automáticamente. Es decir, no a través de un administrador en el momento de la creación del objeto; ni a través del propio sistema operativo (SO). Un componente fuera del servicio de firewall debe realizar la resolución de direcciones IP para estos objetos y actualizarlos correctamente. La implementación de este componente está fuera del ámbito de este contenido.

Una dirección de palabra clave dinámica se indica como *AutoResolve* estableciendo la marca FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE en el objeto al llamar **a** la función [**FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) El *campo de* palabra clave debe usarse para representar el valor que se resuelve, es decir, un nombre de dominio completo &mdash; (FQDN) o nombre de host. *Inicialmente,* el campo direcciones debe ser NULL para estos objetos. Estos objetos no tendrán sus direcciones IP persistentes en los ciclos de arranque y debe volver a evaluar o volver a rellenar sus direcciones durante el siguiente ciclo de arranque.

> [!NOTE]
> Los objetos de dirección de palabras clave dinámicas AutoResolve desencadenan notificaciones en [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) y [**FWDeleteDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)pero no [**en FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)

## <a name="non-autoresolve-dynamic-keyword-addresses"></a>Direcciones de palabras clave dinámicas que no son de AutoResolve

El segundo tipo no *es AutoResolve,* donde el campo *de* palabra clave es cualquier cadena y las direcciones se definen en el momento de la creación.

Estos objetos se usan para almacenar un conjunto de direcciones IP, subredes o intervalos. El *campo de* palabra clave aquí se usa para mayor comodidad de administración y se puede establecer en cualquier cadena. El *campo direcciones* debe ser distinto de NULL tras la creación. Las direcciones de estos objetos se conservan en los reinicios.

> [!NOTE]
> Los objetos de dirección de palabras clave dinámicas que no son AutoResolve desencadenan notificaciones [**en FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)y [**también FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).

## <a name="more-about-dynamic-keyword-addresses"></a>Más información sobre las direcciones de palabras clave dinámicas 

Todas las direcciones de palabras clave dinámicas deben tener un [**identificador GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) único para representarlas.

La API [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) entrega notificaciones a un cliente cuando cambian las direcciones de palabras clave dinámicas. No se entrega ninguna carga al cliente que describa exactamente lo que cambió en el sistema. Si necesita saber qué objetos han cambiado, debe consultar el estado actual de los objetos en el sistema mediante las API [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) o [**FWEnumDynamicKeywordAddressesByType0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) Puede usar las distintas marcas para solicitar notificaciones solo para un subconjunto de objetos. Si no usa ninguna marca, se entregarán notificaciones de cambio para todos los objetos.

Una regla de firewall puede usar direcciones de palabras clave dinámicas en lugar de definir explícitamente direcciones IP para su condición de dirección remota. Una regla de firewall puede usar direcciones de palabras clave dinámicas e intervalos de direcciones remotas definidos estáticamente. Un único objeto de dirección de palabra clave dinámica se puede volver a usar en varias reglas de firewall. Si una regla de firewall no tiene ninguna dirección remota configurada (es decir, configurada solo con objetos AutoResolve que aún no se han resuelto), la regla no se aplicará. Además, si una regla usa varias direcciones de palabras clave dinámicas, la regla se aplicará para todas las direcciones que se resuelven actualmente, incluso si hay otros objetos que aún no se han resuelto. Cuando se actualiza una dirección de palabra clave dinámica, todos los objetos de regla asociados también tendrán sus direcciones remotas actualizadas.

El propio sistema operativo (SO) no aplica ninguna dependencia entre una regla y una dirección de palabra clave dinámica. Esto significa que cualquier objeto se puede crear primero, la regla puede hacer referencia a los ID de dirección de palabra clave dinámica que aún no existen (en cuyo caso, la regla no se &mdash; aplicará). Además, puede eliminar una dirección de palabra clave dinámica incluso si está en uso por una regla de firewall. En este tema se describe cómo un administrador puede configurar reglas para usar la dirección de palabra clave dinámica.

## <a name="code-examples"></a>Ejemplos de código

Para probar cada uno de estos ejemplos de código, primero inicie Visual Studio y cree un proyecto basado en la plantilla de proyecto **Aplicación** de consola. Solo puede reemplazar el contenido de `main.cpp` por la lista de código.

La mayoría de los ejemplos de código usan [bibliotecas de implementación de Windows (WIL).](https://github.com/Microsoft/wil) Una manera cómoda de instalar WIL es ir  a Visual Studio, hacer clic en Project Manage NuGet Packages... Browse (Administrar proyectos paquetes NuGet... Examinar), escribir o pegar \>  \>  **Microsoft.Windows.ImplementationLibrary**  en el cuadro de búsqueda, seleccionar el elemento en los resultados de la búsqueda y, a continuación, hacer clic en Instalar para instalar el paquete para ese proyecto.

> [!NOTE]
> Los tipos de puntero para las funciones gratuitas de NetFw se publican a través de , pero no se publica una biblioteca de vínculos `NetFw.h` estáticos. Use el [patrón LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) / [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para llamar a estas funciones, como se muestra en estos ejemplos de código.

### <a name="add-a-dynamic-keyword-address"></a>Adición de una dirección de palabra clave dinámica

En este ejemplo se muestra cómo usar la [**función FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a>Eliminación de una dirección de palabra clave dinámica

En este ejemplo se muestra cómo usar la [**función FWDeleteDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a>Enumerar y liberar direcciones de palabras clave dinámicas por identificador

En este ejemplo se muestra cómo usar las funciones [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) y [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a>Enumerar y liberar direcciones de palabras clave dinámicas por tipo

En este ejemplo se muestra cómo usar las funciones [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) y [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a>Actualización de direcciones de palabras clave dinámicas

En este ejemplo se muestra cómo usar la [**función FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a>Suscripción y control de notificaciones de cambio de dirección de palabras clave dinámicas

En este ejemplo se muestra cómo usar las funciones [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) y [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) y la devolución [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) llamada.

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a>Temas relacionados

* [Referencia de palabras clave dinámicas del firewall](firewall-dynamic-keywords-reference.md)
