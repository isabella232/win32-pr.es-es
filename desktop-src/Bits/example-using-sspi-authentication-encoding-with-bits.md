---
title: Ejemplo de uso de la codificación de autenticación de SSPI con BITS
description: Puede usar los métodos de autenticación de interfaz de proveedor de compatibilidad de seguridad (SSPI) y Servicio de transferencia inteligente en segundo plano (BITS) para obtener las credenciales de un usuario, codificar las credenciales y establecer las credenciales codificadas en un trabajo de transferencia de BITS.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13abe9b0bb6d8d4252575f70738f7b2f1a5c42b4cae1a4f042725c7bae15ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528805"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>Ejemplo: Uso de la codificación de autenticación de SSPI con BITS

Puede usar los métodos de autenticación de interfaz de proveedor de compatibilidad de seguridad (SSPI) y Servicio de transferencia inteligente en segundo plano (BITS) para obtener las credenciales de un usuario, codificar las credenciales y establecer las credenciales codificadas en un trabajo de transferencia de BITS. La codificación es necesaria para convertir la estructura de credenciales en cadenas que se pueden pasar a un trabajo de transferencia de BITS.

Para obtener más información sobre la autenticación y los métodos de SSPI, vea [SSPI](../secauthn/sspi.md).

En el procedimiento siguiente se solicitan las credenciales del usuario mediante el paquete de seguridad Negotiate. El programa crea una estructura de identidad de autenticación y rellena la estructura con las cadenas codificadas que representan el nombre de usuario, el dominio y la contraseña del usuario. A continuación, el programa crea un trabajo de descarga de BITS y establece el nombre de usuario y la contraseña codificados como credenciales para el trabajo. El programa libera la estructura de identidad de autenticación después de que ya no sea necesaria.

En este ejemplo se usa el encabezado y la implementación definidos en [Ejemplo: Clases comunes](common-classes.md).

**Para usar la codificación de autenticación de SSPI con trabajos de transferencia de BITS**

1.  Inicialice los parámetros COM mediante una llamada a la función CCoInitializer. Para obtener más información sobre la función CCoInitializer, vea [Ejemplo: Clases comunes](common-classes.md).
2.  Obtiene punteros para las interfaces [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)y [**IBackgroundCopyJob2.**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) En este ejemplo se usa [la clase CComPtr para](/cpp/atl/reference/ccomptr-class?view=vs-2019) administrar punteros de interfaz COM.
3.  Cree una [estructura DE \_ INFORMACIÓN DE CREDUI](/windows/win32/api/wincred/ns-wincred-credui_infoa) que contenga información para personalizar la apariencia del cuadro de diálogo para la función [SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa). A continuación, solicite las credenciales del usuario. Para obtener más información, vea la [función SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).
4.  Codificar la estructura de credenciales como cadenas que se pueden pasar a un trabajo de transferencia de BITS mediante la función [SspiEncodeAuthIdentityAsStrings.](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings)
5.  Prepare una [**estructura BG \_ AUTH \_ CREDENTIALS.**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials)
6.  Inicialice la seguridad del proceso COM mediante una [llamada a CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS requiere al menos el nivel IMPERSONATE de suplantación. BITS produce un error **con E \_ ACCESSDENIED si** no se establece el nivel de suplantación correcto.
7.  Obtenga el localizador inicial a BITS mediante una llamada a la [función CoCreateInstance.](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
8.  Cree un trabajo de transferencia de BITS llamando al [**método IBackgroundCopyManager::CreateJob.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob)
9.  Obtenga el identificador de la [**interfaz IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) y llame al **método IBackgroundCopyJob::QueryInterface.**
10. Rellene la [**estructura BG \_ AUTH \_ CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) con las cadenas de nombre de usuario y contraseña codificadas y establezca el esquema de autenticación en Negotiate (**BG \_ AUTH SCHEME \_ \_ NEGOTIATE**).
11. Use el [**puntero IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) para realizar solicitudes a BITS. Este programa usa el [**método IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para establecer las credenciales del trabajo de transferencia de BITS.
12. Agregue archivos, modifique propiedades o reanude el trabajo de transferencia de BITS.
13. Una vez completado el trabajo de transferencia de BITS, quite el trabajo de la cola mediante una llamada a [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).
14. Por último, libera la estructura de identidad de autenticación mediante una llamada a la [función SspiFreeAuthIdentity.](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity)

En el ejemplo de código siguiente se muestra cómo usar la codificación de autenticación SSPI con trabajos de transferencia de BITS.


```C++
#define SECURITY_WIN32
#define _SEC_WINNT_AUTH_TYPES

#include <windows.h>
#include <ntsecapi.h>
#include <bits.h>
#include <sspi.h>
#include <wincred.h>
#include <iostream>
#include <atlbase.h>
#include "CommonCode.h"

void PromptForCredentials(PWSTR pwTargetName)
{
    HRESULT hr;
    
    // If CoInitializeEx fails, the exception is unhandled and the program terminates
    CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    CComPtr<IBackgroundCopyManager> pQueueMgr;
    CComPtr<IBackgroundCopyJob> pJob;
    CComPtr<IBackgroundCopyJob2> pJob2;

    PSEC_WINNT_AUTH_IDENTITY_OPAQUE pAuthIdentityEx2 = NULL;
    DWORD dwFlags = 0;
    BOOL fSave = FALSE;
    BOOL bReturn = TRUE;

    CREDUI_INFO creduiInfo = { 0 };
    creduiInfo.cbSize = sizeof(creduiInfo);
    // Change the message text and caption to the actual text for your dialog.
    creduiInfo.pszMessageText = pwTargetName;
    creduiInfo.pszCaptionText = L"SSPIPFC title for the dialog box";

    try {
        // Prompt for credentials from user using Negotiate security package.
        DWORD dwRet = SspiPromptForCredentials(
            pwTargetName,
            &creduiInfo,
            0,
            L"Negotiate", 
            NULL,
            &pAuthIdentityEx2,
            &fSave,
            dwFlags
            );

        if (SEC_E_OK != dwRet) 
        {
            // Prompt for credentials failed.
            throw MyException(dwRet, L"SspiPromptForCredentials");
        }

        if (NULL != pAuthIdentityEx2) 
        {
            GUID guidJob;
            BG_AUTH_CREDENTIALS authCreds;

            PCWSTR pwUserName = NULL;
            PCWSTR pwDomainName = NULL;
            PCWSTR pwPassword = NULL;

            // Encode credential structure as strings that can
            // be passed to a BITS job.
            SECURITY_STATUS secStatus = SspiEncodeAuthIdentityAsStrings(
                pAuthIdentityEx2,
                &pwUserName,
                &pwDomainName,
                &pwPassword
                );

            if(SEC_E_OK != secStatus) 
            {
                // Encode authentication identity as strings.
                throw MyException(secStatus, L"SspiEncodeAuthIdentityAsStrings");   
            }

            // Show the encoded user name and domain name.
            wprintf(
                L"User Name: %s\nDomain Name: %s",
                pwUserName,
                pwDomainName
                );

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
            hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                CLSCTX_LOCAL_SERVER,
                __uuidof(IBackgroundCopyManager),
                (void**) &pQueueMgr);

            if (FAILED(hr))
            {
                // Failed to connect.
                throw MyException(hr, L"CoCreateInstance");
            }

            // Create a job.
            hr = pQueueMgr->CreateJob(
                L"EncodeSample", 
                BG_JOB_TYPE_DOWNLOAD, 
                &guidJob, 
                &pJob
                );

            if(FAILED(hr))
            {   
                // Failed to create a BITS job.
                throw MyException(hr, L"CreateJob");
            }

            // Get IBackgroundCopyJob2 interface.
            hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
            if (FAILED(hr)) 
            {
                // Failed to get a reference to the IBackgroundCopyJob2 interface.
                throw MyException(hr, L"QueryInterface(IBackgroundCopyJob2)");
            }

            // Create a BITS authentication structure from the encoded strings.
            authCreds.Target = BG_AUTH_TARGET_SERVER;
            authCreds.Scheme = BG_AUTH_SCHEME_NEGOTIATE;
            authCreds.Credentials.Basic.UserName = (LPWSTR)pwUserName;
            authCreds.Credentials.Basic.Password = (LPWSTR)pwPassword;

            // Set the credentials for the job.
            hr = pJob2->SetCredentials(&authCreds);
            if (FAILED(hr)) 
            {
                // Failed to set credentials.
                throw MyException(hr, L"SetCredentials");
            }

            // Modify the job's property values.
            // Add files to the job.
            // Activate (resume) the job in the transfer queue.

            // Remove the job from the transfer queue.
            hr = pJob->Complete();
            if (FAILED(hr)) 
            {
                // Failed to complete the job.
                throw MyException(hr, L"Complete");
            }
        }
    }
    catch(std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }
    catch(MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }

    // Free the auth identity structure.
    if (NULL != pAuthIdentityEx2)
    {
        SspiFreeAuthIdentity(pAuthIdentityEx2);
        pAuthIdentityEx2 = NULL;
    }

    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{
    PromptForCredentials(L"Target");
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SSPI](../secauthn/sspi.md)
</dt> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Ejemplo: Clases comunes](common-classes.md)
</dt> </dl>

 

 