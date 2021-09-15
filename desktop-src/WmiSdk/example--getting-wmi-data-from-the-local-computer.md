---
description: Puede usar el procedimiento y los ejemplos de código de este tema para crear una aplicación cliente WMI completa que realice la inicialización COM, se conecte a WMI en el equipo local, recupere datos de forma semisincronosa y, a continuación, limpie.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 'Ejemplo: Obtener datos WMI del equipo local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840cd4ada941bdfd8ba7fca9b8ca9393c0b5eb55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359426"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a>Ejemplo: Obtener datos WMI del equipo local

Puede usar el procedimiento y los ejemplos de código de este tema para crear una aplicación cliente WMI completa que realice la inicialización COM, se conecte a WMI en el equipo local, recupere datos de forma semisincronosa y, a continuación, limpie. En este ejemplo se obtiene el nombre del sistema operativo en el equipo local y se muestra. Para recuperar datos de un equipo remoto, vea Ejemplo: Obtener datos [WMI de un equipo remoto.](example--getting-wmi-data-from-a-remote-computer.md) Para obtener los datos de forma asincrónica, vea Ejemplo: Obtener datos [WMI del equipo local de forma asincrónica.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

El siguiente procedimiento se usa para ejecutar la aplicación WMI. Los pasos 1 a 5 contienen todos los pasos necesarios para configurar y conectarse a WMI, y los pasos 6 y 7 son donde se consultan y reciben los datos.

1.  Inicialice los parámetros COM con una llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Para obtener más información, [vea Inicializar COM para una aplicación WMI.](initializing-com-for-a-wmi-application.md)

2.  Inicialice la seguridad del proceso COM mediante una [**llamada a CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante C++.](setting-the-default-process-security-level-using-c-.md)

3.  Obtenga el localizador inicial a WMI mediante una llamada [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Para obtener más información, vea [Crear una conexión a un espacio de nombres WMI.](creating-a-connection-to-a-wmi-namespace.md)

4.  Obtenga un puntero a [**IWbemServices para**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) el espacio de nombres cimv2 raíz en el equipo local mediante una llamada a \\ [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Para conectarse a un equipo remoto, vea [Ejemplo: Obtención de datos WMI desde un equipo remoto.](example--getting-wmi-data-from-a-remote-computer.md)

    Para obtener más información, vea [Crear una conexión a un espacio de nombres WMI.](creating-a-connection-to-a-wmi-namespace.md)

5.  Establezca la seguridad del proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que el servicio WMI pueda suplantar al cliente mediante una llamada [**a CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Para obtener más información, vea [Establecer los niveles de seguridad en una conexión WMI.](setting-the-security-levels-on-a-wmi-connection.md)

6.  Use el [**puntero IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para realizar solicitudes de WMI. En este ejemplo se ejecuta una consulta para el nombre del sistema operativo mediante una llamada a [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    La siguiente consulta WQL es uno de los argumentos del método .

    `SELECT * FROM Win32_OperatingSystem`

    El resultado de esta consulta se almacena en un [**puntero IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) Esto permite que los objetos de datos de la consulta se recuperen de forma semisincronosa con la **interfaz IEnumWbemClassObject.** Para obtener más información, [vea Enumerar WMI.](enumerating-wmi.md) Para obtener los datos de forma asincrónica, vea Ejemplo: Obtener datos [WMI del equipo local de forma asincrónica.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

    Para obtener más información sobre cómo realizar solicitudes a WMI, vea [Manipular](manipulating-class-and-instance-information.md)información de clase e instancia , Consultar [WMI](querying-wmi.md)y Llamar a [un método](calling-a-method.md).

7.  Obtenga y muestre los datos de la consulta WQL. El [**puntero IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) está vinculado a los objetos de datos devueltos por la consulta y los objetos de datos se pueden recuperar con el método [**IEnumWbemClassObject::Next.**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) Este método vincula los objetos de datos a un [**puntero IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que se pasa al método . Use el [**método IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) para obtener la información deseada de los objetos de datos.

    En el ejemplo de código siguiente se usa para obtener la propiedad Name del objeto de datos, que proporciona el nombre del sistema operativo.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    Después de almacenar el valor de la propiedad Name en la variable [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) vtProp, se puede mostrar al usuario.

    Para obtener más información, [vea Enumerar WMI.](enumerating-wmi.md)

En el ejemplo de código siguiente se recuperan datos WMI de forma semisincronosa desde un equipo local.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



 

 
