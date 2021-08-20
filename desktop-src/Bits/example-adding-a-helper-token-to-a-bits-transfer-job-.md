---
title: Ejemplo de adición de un token auxiliar a un trabajo de transferencia de BITS
description: Puede configurar un trabajo de Servicio de transferencia inteligente en segundo plano (BITS) con un token de seguridad adicional. El trabajo de transferencia de BITS usa este token auxiliar para la autenticación y el acceso a los recursos.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4adab6ca8cebeeca9b9883e89db28205dfdab1ea43e05c01fd119c14c26d374
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528825"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>Ejemplo: Agregar un token auxiliar a un trabajo de transferencia de BITS

Puede configurar un trabajo de Servicio de transferencia inteligente en segundo plano (BITS) con un token de seguridad adicional. El trabajo de transferencia de BITS usa este token auxiliar para la autenticación y el acceso a los recursos.

Para obtener más información, vea [Tokens auxiliares para trabajos de transferencia de BITS.](helper-tokens-for-bits-transfer-jobs.md)

En el procedimiento siguiente se crea un trabajo de transferencia de BITS en el contexto del usuario local, se obtienen las credenciales de un segundo usuario, se crea un token auxiliar con estas credenciales y, a continuación, se establece el token auxiliar en el trabajo de transferencia de BITS.

En este ejemplo se usa el encabezado y la implementación definidos en [Ejemplo: Clases comunes](common-classes.md).

**Para agregar un token auxiliar a un trabajo de transferencia de BITS**

1.  Inicialice los parámetros COM mediante una llamada a la función CCoInitializer. Para obtener más información sobre la función CCoInitializer, vea [Ejemplo: Clases comunes](common-classes.md).
2.  Obtenga un puntero a la [**interfaz IBackgroundCopyJob.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) En este ejemplo se usa [la clase CComPtr para](/cpp/atl/reference/ccomptr-class?view=vs-2019) administrar punteros de interfaz COM.
3.  Inicialice la seguridad del proceso COM mediante una [llamada a CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS requiere al menos el nivel IMPERSONATE de suplantación. BITS produce un error con E ACCESSDENIED si no se establece el nivel de \_ suplantación correcto.
4.  Obtenga un puntero a la [**interfaz IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) y obtenga el localizador inicial de BITS mediante una llamada a la [función CoCreateInstance.]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
5.  Cree un trabajo de transferencia de BITS llamando al [**método IBackgroundCopyManager::CreateJob.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob)
6.  Obtenga un puntero a la interfaz de devolución de llamada CNotifyInterface y llame al método [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para recibir notificaciones de eventos relacionados con el trabajo. Para obtener más información sobre CNotifyInterface, vea [Ejemplo: Clases comunes](common-classes.md).
7.  Llame al [**método IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para establecer los tipos de notificaciones que se recibirán. En este ejemplo, se establecen **las marcas BG NOTIFY JOB \_ \_ \_ TRANSFERRED** y **BG NOTIFY JOB \_ \_ \_ ERROR.**
8.  Obtenga un puntero a la [**interfaz IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) llamando al método **IBackgroundCopyJob::QueryInterface** con el identificador de interfaz adecuado.
9.  Intente iniciar sesión en el usuario del token auxiliar. Cree un identificador de suplantación y llame a [la función LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) para rellenar el identificador de suplantación. Si se realiza correctamente, llame a [la función ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser). Si no se realiza correctamente, el ejemplo llama a la función [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para finalizar la suplantación del usuario que ha iniciado sesión, se produce un error y se cierra el identificador.
10. Llame al [**método IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para suplantar el token del usuario que inició sesión. Si se produce un error en este método, el ejemplo llama a la función [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para finalizar la suplantación del usuario que ha iniciado sesión, se produce un error y se cierra el identificador.
    > [!Note]
    >
    > En las versiones admitidas de Windows antes de Windows 10, versión 1607, el propietario del trabajo debe tener credenciales administrativas para llamar al método [**IBitsTokenOptions::SetHelperToken.**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)
    >
    > A partir Windows 10, versión 1607, los propietarios de trabajos que no son administradores pueden establecer tokens auxiliares que no son de administrador en los trabajos BITS que poseen. Los propietarios de trabajos todavía deben tener credenciales administrativas para establecer tokens auxiliares con privilegios de administrador.

     

11. Llame al [**método IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) para especificar a qué recursos acceder mediante el contexto de seguridad del token auxiliar.
12. Una vez completada la suplantación, en el ejemplo se llama a la función [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para finalizar la suplantación del usuario que ha iniciado sesión y se cierra el identificador.
13. Agregue archivos al trabajo de transferencia de BITS mediante una [**llamada a IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).
14. Una vez agregado el archivo, llame a [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para reanudar el trabajo.
15. Configure un bucle while para esperar el mensaje de salida de la interfaz de devolución de llamada mientras se transfiere el trabajo. El bucle while usa la [función GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar el número de milisegundos transcurridos desde que el trabajo empezó a transferirse.
16. Una vez completado el trabajo de transferencia de BITS, quite el trabajo de la cola mediante una llamada a [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

En el ejemplo de código siguiente se agrega un token auxiliar a un trabajo de transferencia de BITS.


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


void HelperToken(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &domain, const LPWSTR &username, const LPWSTR &password)
{
// If CoInitializeEx fails, the exception is unhandled and the program terminates   
CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);

CComPtr<IBackgroundCopyJob> pJob; 

    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(
            NULL,
            -1,
            NULL,
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL,
            EOAC_DYNAMIC_CLOAKING,
            0
            );

        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void **)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"HelperTokenSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);


        if(FAILED(hr))
        {   
            // Failed to create job.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;    
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to SetNotifyInterface.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to SetNotifyFlags.
            throw MyException(hr, L"SetNotifyFlags");
        }

        //Retrieve the IBitsTokenOptions interface pointer from the BITS transfer job.
        CComPtr<IBitsTokenOptions> pTokenOptions;
        hr = pJob->QueryInterface(__uuidof(IBitsTokenOptions), (void** ) &pTokenOptions);

        if (FAILED(hr))
        {
            // Failed to QueryInterface.
            throw MyException(hr, L"QueryInterface");
        }

        // Log on user of the helper token.
        wprintf(L"Credentials for helper token %s\\%s %s\n", domain, username, password);

        HANDLE hImpersonation = INVALID_HANDLE_VALUE;
        if(LogonUser(username, domain, password, LOGON32_LOGON_INTERACTIVE, LOGON32_PROVIDER_DEFAULT, &hImpersonation))
        {
            // Impersonate the logged-on user.
            if(ImpersonateLoggedOnUser(hImpersonation))
            {
                // Configure the impersonated logged-on user's token as the helper token.
                hr = pTokenOptions->SetHelperToken();        
                if (FAILED(hr))
                {
                    //Failed to set helper token.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperToken");
                }

                hr = pTokenOptions->SetHelperTokenFlags(BG_TOKEN_LOCAL_FILE);
                if (FAILED(hr))
                {
                    //Failed to set helper token flags.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperTokenFlags");
                }

                RevertToSelf();
            }               
            CloseHandle(hImpersonation);
        }

        // Add a file.
        // Replace parameters with variables that contain valid paths.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile,localFile);

        if(FAILED(hr))
        {   
            //Failed to add file to job.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Resume failed.                   
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
        wprintf(L"Error 0x%x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

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

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s ", argv[0]);
        wprintf(L"[remote name] [local name] [helpertoken domain] [helpertoken userrname] [helpertoken password]\n");
        return;
    }

    HelperToken(argv[1],argv[2],argv[3],argv[4],argv[5]);

}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tokens auxiliares para trabajos de transferencia de BITS](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[Ejemplo: Clases comunes](common-classes.md)
</dt> </dl>

 

 