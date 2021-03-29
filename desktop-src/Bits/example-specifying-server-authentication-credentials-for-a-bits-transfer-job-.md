---
title: Especificar credenciales de autenticación de servidor para un trabajo de transferencia de BITS
description: Puede especificar diferentes esquemas de autenticación para un trabajo de transferencia de Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: 31db38f6-3639-4042-97f2-4f9d78942e15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4373cdf0c8b4c8afe7dff367fda9387eec0b54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078352"
---
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a>Especificar credenciales de autenticación de servidor para un trabajo de transferencia de BITS

Puede especificar diferentes esquemas de autenticación para un trabajo de transferencia de Servicio de transferencia inteligente en segundo plano (BITS).

El siguiente procedimiento obtiene un esquema de autenticación y crea una estructura de identidad de autenticación. A continuación, la aplicación crea un trabajo de descarga de BITS y establece las credenciales para el trabajo. Una vez creado el trabajo, la aplicación obtiene un puntero a una interfaz de devolución de llamada y sondea el estado del trabajo de transferencia de BITS. Una vez completado el trabajo, se quita de la cola.

En este ejemplo se usa el encabezado y la implementación definidos en el [ejemplo: clases comunes](common-classes.md).

**Para especificar las credenciales de autenticación del servidor para un trabajo de transferencia de BITS**

1.  Cree una estructura de contenedor que asigne los valores de [**\_ \_ esquema de autenticación BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) a los nombres de esquema.

    ```C++
    struct
    {
        LPCWSTR        Name;
        BG_AUTH_SCHEME Scheme;
    }
    SchemeNames[] =
    {
        { L"basic",      BG_AUTH_SCHEME_BASIC },
        { L"digest",     BG_AUTH_SCHEME_DIGEST },
        { L"ntlm",       BG_AUTH_SCHEME_NTLM },
        { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
        { L"passport",   BG_AUTH_SCHEME_PASSPORT },

        { NULL,         BG_AUTH_SCHEME_BASIC }
    };
    ```

    

2.  Inicialice los parámetros COM llamando a la función CCoInitializer. Para obtener más información sobre la función CCoInitializer, vea [ejemplo: clases comunes](common-classes.md).
3.  Preparar una estructura de [**\_ \_ credenciales de autenticación BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) . En el ejemplo se usa la función [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) para borrar las ubicaciones de memoria asociadas a la información confidencial. La función [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) se define en Winbase. h.
4.  Utilice la función GetScheme para obtener el esquema de autenticación que se va a usar para conectarse al servidor.

    ```C++
    bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
    {
        int i;

        i = 0;
        while (SchemeNames[i].Name != NULL)
        {
            if (0 == _wcsicmp( s, SchemeNames[i].Name ))
            {

                *scheme = SchemeNames[i].Scheme;
                return true;
            }

            ++i;
        }

        return false;
    }
    ```

    

5.  Rellene la estructura de [**\_ \_ credenciales**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) de autenticación BG con el esquema de autenticación devuelto por la función GetScheme y el nombre de usuario y la contraseña que se pasaron a la función ServerAuthentication.
6.  Obtiene un puntero a la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).
7.  Inicialice la seguridad del proceso COM llamando a [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS requiere al menos el nivel de suplantación de suplantación. BITS produce un error con E \_ ACCESSDENIED si no se establece el nivel de suplantación correcto.
8.  Obtiene un puntero a la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) y obtiene el localizador inicial a bits llamando a la función [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
9.  Cree un trabajo de transferencia de BITS llamando al método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
10. Obtiene un puntero a la interfaz de devolución de llamada CNotifyInterface y llama al método [**IBackgroundCopyJob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para recibir la notificación de eventos relacionados con el trabajo. Para obtener más información sobre CNotifyInterface, vea [ejemplo: clases comunes](common-classes.md).
11. Llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para establecer los tipos de notificaciones que se van a recibir. En este ejemplo, se establecen las marcas de **\_ \_ \_ error** del trabajo de **notificación de BG \_ \_ \_ transferida** y de notificación de BG.
12. Obtiene un puntero a la interfaz [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Use el puntero **IBackgroundCopyJob2** para establecer propiedades adicionales en el trabajo. Este programa usa el método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para establecer las credenciales para el trabajo de transferencia de bits.
13. Agregue archivos al trabajo de transferencia de BITS llamando a [**IBackgroundCopyJob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile). En este ejemplo, el método **IBackgroundCopyJob:: AddFile** usa las variables Archivoremoto y archivolocal que se pasaron a la función ServerAuthentication.
14. Una vez agregado el archivo, llame a [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para reanudar el trabajo.
15. Configure un bucle while para esperar el mensaje de salida de la interfaz de devolución de llamada mientras se transfiere el trabajo.

    > [!Note]  
    > Este paso solo es necesario si el apartamento COM es un contenedor uniproceso. Para obtener más información, consulte [apartamentos de un solo subproceso](../com/single-threaded-apartments.md).

     

    ```C++
    // Wait for QuitMessage from CallBack
        DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
        while (dwLimit > GetTickCount())
        {
            MSG msg;

            while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                // If it is a quit message, exit.
                if (msg.message == WM_QUIT) 
                {
                    return;
                }

                // Otherwise, dispatch the message.
                DispatchMessage(&msg); 
            } // End of PeekMessage while loop
        }
    ```

    

    El bucle anterior utiliza la función [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar el número de milisegundos que han transcurrido desde que el trabajo empezó a transferir.

16. Una vez completado el trabajo de transferencia de BITS, quite el trabajo de la cola mediante una llamada a [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

En el ejemplo de código siguiente se especifican las credenciales de autenticación del servidor para un trabajo de transferencia de BITS.


```C++
#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

//
// Retrieve BG_AUTH_SCHEME from scheme name.
//
//
struct
{
    LPCWSTR        Name;
    BG_AUTH_SCHEME Scheme;
}
SchemeNames[] =
{
    { L"basic",      BG_AUTH_SCHEME_BASIC },
    { L"digest",     BG_AUTH_SCHEME_DIGEST },
    { L"ntlm",       BG_AUTH_SCHEME_NTLM },
    { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
    { L"passport",   BG_AUTH_SCHEME_PASSPORT },

    { NULL,         BG_AUTH_SCHEME_BASIC }
};

bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
{
    int i;

    i = 0;
    while (SchemeNames[i].Name != NULL)
    {
        if (0 == _wcsicmp( s, SchemeNames[i].Name ))
        {

            *scheme = SchemeNames[i].Scheme;
            return true;
        }

        ++i;
    }

    return false;
}

void ServerAuthentication(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &scheme, const LPWSTR &username, const LPWSTR &password)
{

 // If CoInitializeEx fails, the exception is unhandled and the program terminates  
 CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    // Prepare the credentials structure.
    BG_AUTH_CREDENTIALS cred;
    ZeroMemory(&cred, sizeof(cred));
    if (!GetScheme(scheme,&cred.Scheme))
    {
        wprintf(L"Invalid authentication scheme specified\n");
        return;
    }

    cred.Target = BG_AUTH_TARGET_SERVER;
    cred.Credentials.Basic.UserName = username;
    if (0 == _wcsicmp(cred.Credentials.Basic.UserName, L"NULL"))
    {
        cred.Credentials.Basic.UserName = NULL;
    }

    cred.Credentials.Basic.Password = password;
    if (0 == _wcsicmp(cred.Credentials.Basic.Password, L"NULL"))
    {
        cred.Credentials.Basic.Password = NULL;
    }

    CComPtr<IBackgroundCopyJob> pJob;
    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(NULL, 
            -1, 
            NULL, 
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL, 
            EOAC_DYNAMIC_CLOAKING, 
            0);
        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void**)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"BitsAuthSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyFlags");
        }

        // Set credentials.
        CComPtr<IBackgroundCopyJob2> job2;
        hr = pJob.QueryInterface(&job2);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"QueryInterface");
        }

        hr = job2->SetCredentials(&cred);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetCredentials");
        }

        // Add a file.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile, localFile);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"Resume");
        }
    }
    catch(const std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }
    catch(const MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack.
    DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
    while (dwLimit > GetTickCount())
    {
        MSG msg;

        while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
        { 
            // If it is a quit message, exit.
            if (msg.message == WM_QUIT) 
            {
                return;
            }

            // Otherwise, dispatch the message.
            DispatchMessage(&msg); 
        } // End of PeekMessage while loop
    }

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s", argv[0]);
        wprintf(L" [remote name] [local name] [server authentication scheme =\"NTLM\"|\"NEGOTIATE\"|\"BASIC\"|\"DIGEST\"] [username] [password]\n");
        return;
    }

    ServerAuthentication(argv[1], argv[2], argv[3], argv[4], argv[5]); 

}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Ejemplo: clases comunes](common-classes.md)
</dt> </dl>

 

 