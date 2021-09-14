---
description: El repositorio WMI contiene clases de rendimiento preinstaladas para todos los objetos de la biblioteca de rendimiento.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Acceso a clases de rendimiento preinstaladas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241472"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>Acceso a clases de rendimiento preinstaladas de WMI

El repositorio WMI contiene clases de rendimiento preinstaladas para todos los objetos de la biblioteca de rendimiento. Por ejemplo, las instancias de la clase de rendimiento de datos sin procesar [**Win32 \_ PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representan procesos. Este objeto de rendimiento es visible en el Monitor de sistema como el objeto Process.

La **propiedad PageFaultsPerSec** de [**Win32 \_ PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa el contador de rendimiento Errores de página por segundo para el proceso. Las [**clases \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen los valores de datos calculados que se muestran en el Monitor de sistema (Perfmon.exe). El valor de la **propiedad PageFaultsPerSec** de [**Win32 \_ PerfFormattedData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) es el mismo que cuando aparece en el Monitor del sistema.

Use la [API COM para WMI o](com-api-for-wmi.md) la API de scripting para [WMI](scripting-api-for-wmi.md) para acceder a los datos de rendimiento a través de las clases de contador [de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes). En ambos [*casos, se requiere un objeto*](gloss-r.md) de actualizador para obtener cada muestra de datos. Para obtener más información y crear scripts de ejemplos de código para usar actualizadores y obtener acceso a clases de rendimiento, vea [Wmi Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md). Para obtener más información, vea [Acceso a datos de rendimiento en script](accessing-performance-data-in-script.md).

## <a name="accessing-performance-data-from-c"></a>Acceso a datos de rendimiento desde C++

En el siguiente ejemplo de código de C++ se usa el proveedor de contadores de rendimiento para tener acceso a clases predefinidas de alto rendimiento. Crea un objeto de actualizador y agrega un objeto al actualizador. El objeto es una [**instancia de \_ Win32 PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) que supervisa el rendimiento de un proceso específico. El código solo lee una propiedad de contador en el objeto de proceso, la **propiedad VirtualBytes.** El código requiere las siguientes referencias e **\# instrucciones include** para compilarse correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



En el procedimiento siguiente se muestra cómo acceder a los datos de un proveedor de alto rendimiento en C++.

**Para acceder a los datos de un proveedor de alto rendimiento en C++**

1.  Establezca una conexión con el espacio de nombres WMI y establezca la seguridad wmi mediante una llamada a [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) y [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Este paso es un paso estándar para crear cualquier aplicación cliente WMI. Para obtener más información, vea [Crear una aplicación WMI mediante C++.](creating-a-wmi-application-using-c-.md)

2.  Cree un objeto de actualizador mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ WbemRefresher. Solicite una [**interfaz IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) mediante el [**método QueryInterface.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Solicite una [**interfaz IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) mediante el **método QueryInterface.**

    La [**interfaz IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) es la interfaz principal del objeto [**Refresher de**](swbemrefreshableitem-refresher.md) WMI.

    En el siguiente ejemplo de código de C++ se muestra cómo recuperar [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  Agregue un objeto al actualizador mediante una llamada al método [**IWbemConfigureRefresher::AddObjectByPath.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath)

    Al agregar un objeto al actualizador, WMI actualiza el objeto cada vez que se llama al [**método IWbemRefresher::Refresh.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) El objeto que agrega designa el proveedor en sus calificadores de clase.

    En el siguiente ejemplo de código de C++ se muestra cómo llamar a [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  Para configurar un acceso más rápido al objeto, conéctese a la [**interfaz IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) a través de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la [**interfaz IWbemClassObject.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)

    En el siguiente ejemplo de código de C++ se muestra cómo recuperar un puntero al objeto mediante [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) en lugar de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    La [**interfaz IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) aumenta el rendimiento porque puede obtener identificadores para propiedades de contador específicas y requiere que bloquee y desbloquee el objeto en el código, que es una operación que [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) realiza para cada acceso a las propiedades.

5.  Obtenga los identificadores de las propiedades que se examinarán mediante llamadas al [**método IWbemObjectAccess::GetPropertyHandle.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle)

    Los identificadores de propiedad son los mismos para todas las instancias de una clase, lo que significa que se usa el identificador de propiedad que se recupera de una instancia específica para todas las instancias de una clase específica. También puede obtener un identificador de un objeto de clase para recuperar valores de propiedad de un objeto de instancia.

    En el siguiente ejemplo de código de C++ se muestra cómo recuperar un identificador de propiedad.

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  Cree un bucle de programación que realice las siguientes acciones:

    -   Actualice el objeto con una llamada a [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) mediante el puntero creado en la llamada anterior a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

        En esta llamada, el actualizador wmi actualiza el objeto de cliente mediante los datos que proporciona el proveedor.

    -   Realice cualquier acción según sea necesario en el objeto, como recuperar un nombre de propiedad, un tipo de datos o un valor.

        Puede acceder a la propiedad a través del identificador de propiedad obtenido anteriormente. Debido a la [**llamada De**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) actualización, WMI actualiza la propiedad cada vez a través del bucle .

En el siguiente ejemplo de C++ se muestra cómo usar la API de alto rendimiento de WMI.


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases de contadores de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
