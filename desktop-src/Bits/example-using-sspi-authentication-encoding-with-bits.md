---
title: Ejemplo de uso de la codificación de autenticación SSPI con BITS
description: Puede usar métodos de autenticación y Servicio de transferencia inteligente en segundo plano (BITS) de la interfaz del proveedor de compatibilidad con seguridad (SSPI) para obtener las credenciales de un usuario, codificar las credenciales y establecer las credenciales codificadas en un trabajo de transferencia de BITS.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b86248c4782789010a817755d9bc27b3e5373b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793773"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a><span data-ttu-id="23e32-103">Ejemplo: uso de la codificación de autenticación SSPI con BITS</span><span class="sxs-lookup"><span data-stu-id="23e32-103">Example: Using SSPI Authentication Encoding with BITS</span></span>

<span data-ttu-id="23e32-104">Puede usar métodos de autenticación y Servicio de transferencia inteligente en segundo plano (BITS) de la interfaz del proveedor de compatibilidad con seguridad (SSPI) para obtener las credenciales de un usuario, codificar las credenciales y establecer las credenciales codificadas en un trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="23e32-104">You can use Security Support Provider Interface (SSPI) Authentication and Background Intelligent Transfer Service (BITS) methods to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span> <span data-ttu-id="23e32-105">La codificación es necesaria para convertir la estructura de credenciales en cadenas que se pueden pasar a un trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="23e32-105">Encoding is required to convert credentials structure into strings that can be passed to a BITS transfer job.</span></span>

<span data-ttu-id="23e32-106">Para obtener más información acerca de los métodos y la autenticación SSPI, vea [SSPI](../secauthn/sspi.md).</span><span class="sxs-lookup"><span data-stu-id="23e32-106">For more information about SSPI authentication and methods, see [SSPI](../secauthn/sspi.md).</span></span>

<span data-ttu-id="23e32-107">El procedimiento siguiente solicita las credenciales del usuario mediante el paquete de seguridad Negotiate.</span><span class="sxs-lookup"><span data-stu-id="23e32-107">The following procedure prompts for credentials from the user by using the Negotiate security package.</span></span> <span data-ttu-id="23e32-108">El programa crea una estructura de identidad de autenticación y rellena la estructura con las cadenas codificadas que representan el nombre de usuario, el dominio y la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="23e32-108">The program creates an authentication identity structure and populates the structure with the encoded strings that represent the user name, domain, and password of the user.</span></span> <span data-ttu-id="23e32-109">A continuación, el programa crea un trabajo de descarga de BITS y establece el nombre de usuario codificado y la contraseña como credenciales para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="23e32-109">Then the program creates a BITS download job and sets the encoded user name and password as the credentials for the job.</span></span> <span data-ttu-id="23e32-110">El programa libera la estructura de identidad de autenticación una vez que ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="23e32-110">The program frees the authentication identity structure after it is no longer needed.</span></span>

<span data-ttu-id="23e32-111">En este ejemplo se usa el encabezado y la implementación definidos en el [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="23e32-111">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="23e32-112">**Para usar la codificación de autenticación SSPI con trabajos de transferencia de BITS**</span><span class="sxs-lookup"><span data-stu-id="23e32-112">**To use SSPI authentication encoding with BITS transfer jobs**</span></span>

1.  <span data-ttu-id="23e32-113">Inicialice los parámetros COM llamando a la función CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="23e32-113">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="23e32-114">Para obtener más información sobre la función CCoInitializer, vea [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="23e32-114">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="23e32-115">Obtener punteros para las interfaces [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="23e32-115">Get pointers for the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interfaces.</span></span> <span data-ttu-id="23e32-116">En este ejemplo se usa la [Clase CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) para administrar punteros de interfaz com.</span><span class="sxs-lookup"><span data-stu-id="23e32-116">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="23e32-117">Cree una estructura de [ \_ información CREDUI](/windows/win32/api/wincred/ns-wincred-credui_infoa) que contenga información para personalizar la apariencia del cuadro de diálogo para la [función SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="23e32-117">Create a [CREDUI\_INFO](/windows/win32/api/wincred/ns-wincred-credui_infoa) structure that contains information for customizing the appearance of the dialog box for the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span> <span data-ttu-id="23e32-118">A continuación, solicite las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="23e32-118">Then prompt for credentials from the user.</span></span> <span data-ttu-id="23e32-119">Para obtener más información, vea la [función SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="23e32-119">For more information, see the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span>
4.  <span data-ttu-id="23e32-120">Codifique la estructura de credenciales como cadenas que se pueden pasar a un trabajo de transferencia de BITS mediante la función [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) .</span><span class="sxs-lookup"><span data-stu-id="23e32-120">Encode credential structure as strings that can be passed to a BITS transfer job by using the [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) function.</span></span>
5.  <span data-ttu-id="23e32-121">Preparar una estructura de [**\_ \_ credenciales de autenticación BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="23e32-121">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span>
6.  <span data-ttu-id="23e32-122">Inicialice la seguridad del proceso COM llamando a [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="23e32-122">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="23e32-123">BITS requiere al menos el nivel de suplantación de suplantación.</span><span class="sxs-lookup"><span data-stu-id="23e32-123">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="23e32-124">BITS produce un error con **E \_ ACCESSDENIED** si no se establece el nivel de suplantación correcto.</span><span class="sxs-lookup"><span data-stu-id="23e32-124">BITS fails with **E\_ACCESSDENIED** if the correct impersonation level is not set.</span></span>
7.  <span data-ttu-id="23e32-125">Obtenga el localizador inicial a BITS llamando a la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="23e32-125">Obtain the initial locator to BITS by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
8.  <span data-ttu-id="23e32-126">Cree un trabajo de transferencia de BITS llamando al método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="23e32-126">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
9.  <span data-ttu-id="23e32-127">Obtiene el identificador de la interfaz [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) y llama al método **IBackgroundCopyJob:: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="23e32-127">Get the identifier for the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface, and call the **IBackgroundCopyJob::QueryInterface** method.</span></span>
10. <span data-ttu-id="23e32-128">Rellene la estructura de [**\_ \_ credenciales de autenticación BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) con las cadenas de contraseña y nombre de usuario codificadas, y establezca el esquema de autenticación en Negotiate (**negociación de \_ esquema de autenticación \_ \_ BG**).</span><span class="sxs-lookup"><span data-stu-id="23e32-128">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure with the encoded user name and password strings, and set the authentication scheme to Negotiate (**BG\_AUTH\_SCHEME\_NEGOTIATE**).</span></span>
11. <span data-ttu-id="23e32-129">Use el puntero [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) para hacer solicitudes a bits.</span><span class="sxs-lookup"><span data-stu-id="23e32-129">Use the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) pointer to make requests to BITS.</span></span> <span data-ttu-id="23e32-130">Este programa usa el método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para establecer las credenciales para el trabajo de transferencia de bits.</span><span class="sxs-lookup"><span data-stu-id="23e32-130">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
12. <span data-ttu-id="23e32-131">Agregue archivos, modifique las propiedades o reanude el trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="23e32-131">Add files, modify properties, or resume the BITS transfer job.</span></span>
13. <span data-ttu-id="23e32-132">Una vez completado el trabajo de transferencia de BITS, quite el trabajo de la cola mediante una llamada a [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="23e32-132">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>
14. <span data-ttu-id="23e32-133">Por último, libere la estructura de identidad de autenticación mediante una llamada a la función [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) .</span><span class="sxs-lookup"><span data-stu-id="23e32-133">Finally, free the authentication identity structure by calling the [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) function.</span></span>

<span data-ttu-id="23e32-134">En el ejemplo de código siguiente se muestra cómo usar la codificación de autenticación SSPI con trabajos de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="23e32-134">The following code example demonstrates how to use SSPI Authentication Encoding with BITS transfer jobs.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="23e32-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23e32-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23e32-136">SSPI</span><span class="sxs-lookup"><span data-stu-id="23e32-136">SSPI</span></span>](../secauthn/sspi.md)
</dt> <dt>

[<span data-ttu-id="23e32-137">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="23e32-137">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="23e32-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="23e32-138">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="23e32-139">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="23e32-139">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="23e32-140">Ejemplo: clases comunes</span><span class="sxs-lookup"><span data-stu-id="23e32-140">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 