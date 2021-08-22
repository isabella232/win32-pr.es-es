---
description: La API de alto rendimiento de WMI es una serie de interfaces que obtienen datos de las clases de contador de rendimiento.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Acceso a datos de rendimiento en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e566fb5803e598e42fac06d8f04fe3e71935008668e397a47d0226a96560eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820332"
---
# <a name="accessing-performance-data-in-c"></a>Acceso a datos de rendimiento en C++

La API de alto rendimiento de WMI es una serie de interfaces que obtienen datos de las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes). Estas interfaces requieren el uso de un objeto [*de actualizador*](gloss-r.md) para aumentar la frecuencia de muestreo. Para obtener más información sobre cómo usar el objeto de actualizador en scripting, vea Acceso a datos de rendimiento en [tareas de script](accessing-performance-data-in-script.md) [y WMI: supervisión de rendimiento.](wmi-tasks--performance-monitoring.md)

En este tema se de abordan las siguientes secciones:

-   [Actualizar datos de rendimiento](#refreshing-performance-data)
-   [Agregar enumeradores al actualizador wmi](#adding-enumerators-to-the-wmi-refresher)
-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="refreshing-performance-data"></a>Actualizar datos de rendimiento

Un objeto de actualizador aumenta el rendimiento del cliente y del proveedor de datos mediante la recuperación de datos sin traspasar los límites del proceso. Si el cliente y el servidor se encuentran en el mismo equipo, un actualizador carga el proveedor de alto rendimiento en proceso en el cliente y copia los datos directamente de los objetos de proveedor en objetos de cliente. Si el cliente y el servidor se encuentran en equipos diferentes, el actualizador aumenta el rendimiento mediante el almacenamiento en caché de objetos en el equipo remoto y la transmisión de conjuntos de datos mínimos al cliente.

Un actualizador también:

-   Vuelve a conectar automáticamente un cliente a un servicio WMI remoto cuando se produce un error de red o se reinicia el equipo remoto.

    De forma predeterminada, un actualizador intenta volver a conectar la aplicación al proveedor de alto rendimiento correspondiente cuando se produce un error en una conexión remota entre los dos equipos. Para evitar la reconexión, pase la marca **WBEM \_ FLAG REFRESH NO AUTO \_ \_ \_ \_ RECONNECT** en la [**llamada al método Refresh.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Los clientes de scripting deben [**establecer la propiedad SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) en **FALSE.**

-   Carga varios objetos y enumeradores proporcionados por el mismo proveedor o por otros distintos.

    Permite agregar varios objetos, enumeradores o ambos a un actualizador.

-   Enumera los objetos .

    Al igual que otros proveedores, un proveedor de alto rendimiento puede enumerar objetos.

Cuando termine de escribir el cliente de alto rendimiento, es posible que desee mejorar el tiempo de respuesta. Dado que [**la interfaz IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) está optimizada para la velocidad, la interfaz no es intrínsecamente segura para subprocesos. Por lo tanto, durante una operación de actualización, no acceda al objeto actualizable o la enumeración. Para proteger objetos entre subprocesos durante las llamadas al método **IWbemObjectAccess,** use los métodos [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) [**y Unlock.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) Para mejorar el rendimiento, sincronice los subprocesos para que no sea necesario bloquear subprocesos individuales. La reducción de subprocesos y la sincronización de grupos de objetos para las operaciones de actualización proporciona el mejor rendimiento general.

## <a name="adding-enumerators-to-the-wmi-refresher"></a>Agregar enumeradores al actualizador wmi

Tanto el número de instancias como los datos de cada instancia se actualizan agregando un enumerador al actualizador para que cada llamada a [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) da como resultado una enumeración completa.

El siguiente ejemplo de código de C++ requiere las siguientes referencias e \# instrucciones include para compilarse correctamente.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



El procedimiento siguiente muestra cómo agregar un enumerador a un actualizador.

**Para agregar un enumerador a un actualizador**

1.  Llame al [**método IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) mediante la ruta de acceso al objeto actualizable y a la [**interfaz IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

    El actualizador devuelve un puntero a una [**interfaz IWbemHiPerfEnum.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) Puede usar la **interfaz IWbemHiPerfEnum para** tener acceso a los objetos de la enumeración .

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  Cree un bucle que realice las siguientes acciones:

    -   Actualiza el objeto mediante una llamada a [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).
    -   Proporciona una matriz de punteros de interfaz [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) al [**método IWbemHiPerfEnum::GetObjects.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)
    -   Obtiene acceso a las propiedades del enumerador mediante los métodos [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) pasados a [**GetObjects.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)

        Se puede pasar un identificador de propiedad a cada [**instancia de IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) para recuperar el valor actualizado. El cliente debe llamar [**a Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar los **punteros IWbemObjectAccess** devueltos [**por GetObjects.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)

## <a name="example"></a>Ejemplo

En el siguiente ejemplo de código de C++ se enumera una clase de alto rendimiento, donde el cliente recupera un identificador de propiedad del primer objeto y reutiliza el identificador para el resto de la operación de actualización. Cada llamada al [**método Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) actualiza el número de instancias y los datos de instancia.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Acceso a datos de rendimiento en script](accessing-performance-data-in-script.md)
</dt> <dt>

[Actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Calificadores de propiedad para clases de contadores de rendimiento con formato](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
