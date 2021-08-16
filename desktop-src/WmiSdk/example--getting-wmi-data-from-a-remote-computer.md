---
description: Puede usar el procedimiento y los ejemplos de código de este tema para crear una aplicación cliente WMI completa que realiza la inicialización COM, se conecta a WMI en un equipo remoto, obtiene datos de forma semisincronosa y, a continuación, limpia.
ms.assetid: 30e65b9e-9372-46d1-843a-bda0d6ec1c69
ms.tgt_platform: multiple
title: 'Ejemplo: Obtención de datos WMI desde un equipo remoto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722247d9b58c9fc27c5fac63a97f86d0c155faa92e41fc68506c5d280d0b040a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556628"
---
# <a name="example-getting-wmi-data-from-a-remote-computer"></a>Ejemplo: Obtención de datos WMI desde un equipo remoto

Puede usar el procedimiento y los ejemplos de código de este tema para crear una aplicación cliente WMI completa que realiza la inicialización COM, se conecta a WMI en un equipo remoto, obtiene datos de forma semisincronosa y, a continuación, limpia. Para obtener más información sobre cómo obtener datos del equipo local, vea Ejemplo: Obtener datos [WMI del equipo local.](example--getting-wmi-data-from-the-local-computer.md) Para obtener más información sobre cómo obtener los datos de forma asincrónica, vea Ejemplo: Obtener datos WMI del equipo [local de forma asincrónica.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

> [!Note]  
> Si está intentando conectarse a un equipo remoto, consulte la información de[Conexión a WMI de forma remota.](connecting-to-wmi-remotely-starting-with-vista.md)

 

En el procedimiento siguiente se muestra cómo ejecutar la aplicación WMI. Los pasos 1 a 5 contienen todos los pasos necesarios para configurar y conectarse a WMI, y los pasos 6 y 7 son donde se consultan y reciben los datos.

**Para obtener datos WMI de un equipo remoto**

1.  Inicialice los parámetros COM con una llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Para obtener más información, [vea Inicializar COM para una aplicación WMI.](initializing-com-for-a-wmi-application.md)

2.  Inicialice la seguridad del proceso COM mediante [**una llamada a CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante C++.](setting-the-default-process-security-level-using-c-.md)

3.  Obtenga el localizador inicial a WMI mediante una llamada [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Para obtener más información, vea [Crear una conexión a un espacio de nombres WMI.](creating-a-connection-to-a-wmi-namespace.md)

4.  Obtenga un puntero a [**IWbemServices para**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) el espacio de nombres cimv2 raíz en un equipo remoto mediante una llamada \\ \\ a \\ [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Al conectarse a un equipo remoto, debe conocer el nombre del equipo, el dominio, el nombre de usuario y la contraseña del equipo remoto al que se está conectando. Todos estos atributos se pasan al **método IWbemLocator::ConnectServer.** Además, asegúrese de que el nombre de usuario del equipo que está intentando conectarse al equipo remoto tiene los privilegios de acceso correctos en el equipo remoto. Para obtener más información, vea [Conectarse a través de Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). Para conectarse al equipo local, vea [Ejemplo:](example--getting-wmi-data-from-the-local-computer.md) Obtener datos WMI del equipo local y Crear una conexión [a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).

    Al controlar nombres de usuario y contraseñas, se recomienda que se le pida al usuario la información, que la use y, a continuación, elimine la información, para que haya menos posibilidades de que un usuario no autorizado intercepte la información. En el paso 4 del código de ejemplo siguiente se usa [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para obtener el nombre de usuario y la contraseña y, a continuación, se usa [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) para deshacerse de la información después de su uso en [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Para obtener más información, vea [Control de contraseñas](/windows/desktop/SecBP/handling-passwords) [y Pedir al usuario credenciales](/windows/desktop/SecBP/asking-the-user-for-credentials) en MSDN.

5.  Cree una [estructura COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) para proporcionar credenciales para establecer la seguridad del proxy.
6.  Establezca la seguridad del proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que el servicio WMI pueda suplantar al cliente mediante una llamada [**a CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Para obtener más información, vea [Establecer los niveles de seguridad en una conexión WMI.](setting-the-security-levels-on-a-wmi-connection.md)

7.  Use el [**puntero IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para realizar solicitudes de WMI. Se ejecuta una consulta para obtener el nombre del sistema operativo y la cantidad de memoria física libre mediante una llamada a [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    La siguiente consulta WQL es uno de los argumentos del método .

    `SELECT * FROM Win32_OperatingSystem`

    El resultado de esta consulta se almacena en un [**puntero IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) Esto permite que los objetos de datos de la consulta se recuperen de forma semisincronosa con la **interfaz IEnumWbemClassObject.** Para obtener más información, [vea Enumeración de WMI.](enumerating-wmi.md) Para obtener los datos de forma asincrónica, vea Ejemplo: Obtener datos [WMI del equipo local de forma asincrónica.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

    Para obtener más información sobre cómo realizar solicitudes de WMI, vea [Manipular](manipulating-class-and-instance-information.md)información de clase e instancia , [Consultar WMI](querying-wmi.md)y Llamar a [un método](calling-a-method.md).

8.  Establezca la seguridad del proxy [**del enumerador IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) Asegúrese de borrar las credenciales de la memoria una vez que haya terminado de usarlos.

    Para obtener más información, vea [Establecer la seguridad en IWbemServices y otros servidores proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md)

9.  Obtenga y muestre los datos de la consulta WQL. El [**puntero IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) está vinculado a los objetos de datos devueltos por la consulta y los objetos de datos se pueden recuperar con el método [**IEnumWbemClassObject::Next.**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) Este método vincula los objetos de datos a un [**puntero IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que se pasa al método . Use el [**método IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) para obtener la información deseada de los objetos de datos.

    El ejemplo de código siguiente se usa para obtener la propiedad del objeto `Name` de datos, que proporciona el nombre del sistema operativo.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    wcout << " OS Name : " << vtProp.bstrVal << endl;
    ```

    

    Una vez que el `Name` valor de la propiedad se almacena en la variable [**VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) se puede `vtProp` mostrar al usuario.

    En el ejemplo de código siguiente se muestra cómo se puede usar de nuevo la variable [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) para almacenar y mostrar el valor de la cantidad de memoria física libre.

    ```C++
    hr = pclsObj->Get(L"FreePhysicalMemory",
        0, &vtProp, 0, 0);
    wcout << " Free physical memory (in kilobytes): "
        << vtProp.uintVal << endl;
    ```

    

    Para obtener más información, [vea Enumeración de WMI.](enumerating-wmi.md)

En el ejemplo de código siguiente se muestra cómo obtener datos WMI de forma semisincronosa desde un equipo remoto.


```C++
#define _WIN32_DCOM
#define UNICODE
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "comsuppw.lib")
#include <wincred.h>
#include <strsafe.h>

int __cdecl main(int argc, char **argv)
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
        RPC_C_IMP_LEVEL_IDENTIFY,    // Default Impersonation  
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

    // Get the user name and password for the remote computer
    CREDUI_INFO cui;
    bool useToken = false;
    bool useNTLM = true;
    wchar_t pszName[CREDUI_MAX_USERNAME_LENGTH+1] = {0};
    wchar_t pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1] = {0};
    wchar_t pszDomain[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszUserName[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszAuthority[CREDUI_MAX_USERNAME_LENGTH+1];
    BOOL fSave;
    DWORD dwErr;

    memset(&cui,0,sizeof(CREDUI_INFO));
    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    // Ensure that MessageText and CaptionText identify
    // what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Press cancel to use process token");
    cui.pszCaptionText = TEXT("Enter Account Information");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    dwErr = CredUIPromptForCredentials( 
        &cui,                             // CREDUI_INFO structure
        TEXT(""),                         // Target for credentials
        NULL,                             // Reserved
        0,                                // Reason
        pszName,                          // User name
        CREDUI_MAX_USERNAME_LENGTH+1,     // Max number for user name
        pszPwd,                           // Password
        CREDUI_MAX_PASSWORD_LENGTH+1,     // Max number for password
        &fSave,                           // State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |// flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr == ERROR_CANCELLED)
    {
        useToken = true;
    }
    else if (dwErr)
    {
        cout << "Did not get credentials " << dwErr << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;      
    }

    // change the computerName strings below to the full computer name
    // of the remote computer
    if(!useNTLM)
    {
        StringCchPrintf(pszAuthority, CREDUI_MAX_USERNAME_LENGTH+1, L"kERBEROS:%s", L"COMPUTERNAME");
    }

    // Connect to the remote root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    //---------------------------------------------------------
   
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTERNAME\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
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


    // step 5: --------------------------------------------------
    // Create COAUTHIDENTITY that can be used for setting security on proxy

    COAUTHIDENTITY *userAcct =  NULL ;
    COAUTHIDENTITY authIdent;

    if( !useToken )
    {
        memset(&authIdent, 0, sizeof(COAUTHIDENTITY));
        authIdent.PasswordLength = wcslen (pszPwd);
        authIdent.Password = (USHORT*)pszPwd;

        LPWSTR slash = wcschr (pszName, L'\\');
        if( slash == NULL )
        {
            cout << "Could not create Auth identity. No domain specified\n" ;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return 1;               // Program has failed.
        }

        StringCchCopy(pszUserName, CREDUI_MAX_USERNAME_LENGTH+1, slash+1);
        authIdent.User = (USHORT*)pszUserName;
        authIdent.UserLength = wcslen(pszUserName);

        StringCchCopyN(pszDomain, CREDUI_MAX_USERNAME_LENGTH+1, pszName, slash - pszName);
        authIdent.Domain = (USHORT*)pszDomain;
        authIdent.DomainLength = slash - pszName;
        authIdent.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

        userAcct = &authIdent;

    }

    // Step 6: --------------------------------------------------
    // Set security levels on a WMI connection ------------------

    hres = CoSetProxyBlanket(
       pSvc,                           // Indicates the proxy to set
       RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
       COLE_DEFAULT_PRINCIPAL,         // Server principal name 
       RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
       userAcct,                       // client identity
       EOAC_NONE                       // proxy capabilities 
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

    // Step 7: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("Select * from Win32_OperatingSystem"),
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

    // Step 8: -------------------------------------------------
    // Secure the enumerator proxy
    hres = CoSetProxyBlanket(
        pEnumerator,                    // Indicates the proxy to set
        RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
        RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
        COLE_DEFAULT_PRINCIPAL,         // Server principal name 
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
        userAcct,                       // client identity
        EOAC_NONE                       // proxy capabilities 
        );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket on enumerator. Error code = 0x" 
             << hex << hres << endl;
        pEnumerator->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // When you have finished using the credentials,
    // erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    SecureZeroMemory(pszUserName, sizeof(pszUserName));
    SecureZeroMemory(pszDomain, sizeof(pszDomain));


    // Step 9: -------------------------------------------------
    // Get the data from the query in step 7 -------------------
 
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

        // Get the value of the FreePhysicalMemory property
        hr = pclsObj->Get(L"FreePhysicalMemory",
            0, &vtProp, 0, 0);
        wcout << " Free physical memory (in kilobytes): "
            << vtProp.uintVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
        pclsObj = NULL;
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    if( pclsObj )
    {
        pclsObj->Release();
    }
    
    CoUninitialize();

    return 0;   // Program successfully completed.
    
}
```



 

 
