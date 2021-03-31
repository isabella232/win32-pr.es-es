---
title: Ejemplo de adición de un token auxiliar a un trabajo de transferencia de BITS
description: Puede configurar un trabajo de transferencia de Servicio de transferencia inteligente en segundo plano (BITS) con un token de seguridad adicional. El trabajo de transferencia de BITS usa este token auxiliar para la autenticación y para tener acceso a los recursos.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab12fe93ae54d91d02bef5e59e99d267571413e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078300"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a><span data-ttu-id="3a3c6-104">Ejemplo: agregar un token auxiliar a un trabajo de transferencia de BITS</span><span class="sxs-lookup"><span data-stu-id="3a3c6-104">Example: Adding a Helper Token to a BITS Transfer Job</span></span>

<span data-ttu-id="3a3c6-105">Puede configurar un trabajo de transferencia de Servicio de transferencia inteligente en segundo plano (BITS) con un token de seguridad adicional.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-105">You can configure a Background Intelligent Transfer Service (BITS) transfer job with an additional security token.</span></span> <span data-ttu-id="3a3c6-106">El trabajo de transferencia de BITS usa este token auxiliar para la autenticación y para tener acceso a los recursos.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-106">The BITS transfer job uses this helper token for authentication and to access resources.</span></span>

<span data-ttu-id="3a3c6-107">Para obtener más información, consulte [tokens de aplicación auxiliar para trabajos de transferencia de bits](helper-tokens-for-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-107">For more information, see [Helper tokens for BITS transfer jobs](helper-tokens-for-bits-transfer-jobs.md).</span></span>

<span data-ttu-id="3a3c6-108">En el procedimiento siguiente se crea un trabajo de transferencia de BITS en el contexto del usuario local, se obtienen las credenciales de un segundo usuario, se crea un token auxiliar con estas credenciales y, a continuación, se establece el token auxiliar en el trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-108">The following procedure creates a BITS transfer job in the context of the local user, gets credentials of a second user, creates a helper token with these credentials, and then sets the helper token on the BITS transfer job.</span></span>

<span data-ttu-id="3a3c6-109">En este ejemplo se usa el encabezado y la implementación definidos en el [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="3a3c6-110">**Para agregar un token auxiliar a un trabajo de transferencia de BITS**</span><span class="sxs-lookup"><span data-stu-id="3a3c6-110">**To add a helper token to a BITS transfer job**</span></span>

1.  <span data-ttu-id="3a3c6-111">Inicialice los parámetros COM llamando a la función CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-111">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="3a3c6-112">Para obtener más información sobre la función CCoInitializer, vea [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-112">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="3a3c6-113">Obtiene un puntero a la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .</span><span class="sxs-lookup"><span data-stu-id="3a3c6-113">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface.</span></span> <span data-ttu-id="3a3c6-114">En este ejemplo se usa la [Clase CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) para administrar punteros de interfaz com.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-114">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="3a3c6-115">Inicialice la seguridad del proceso COM llamando a [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-115">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="3a3c6-116">BITS requiere al menos el nivel de suplantación de suplantación.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-116">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="3a3c6-117">BITS produce un error con E \_ ACCESSDENIED si no se establece el nivel de suplantación correcto.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-117">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
4.  <span data-ttu-id="3a3c6-118">Obtiene un puntero a la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) y obtiene el localizador inicial a bits llamando a la función [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="3a3c6-118">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
5.  <span data-ttu-id="3a3c6-119">Cree un trabajo de transferencia de BITS llamando al método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="3a3c6-119">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
6.  <span data-ttu-id="3a3c6-120">Obtiene un puntero a la interfaz de devolución de llamada CNotifyInterface y llama al método [**IBackgroundCopyJob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para recibir la notificación de eventos relacionados con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-120">Get a pointer to the CNotifyInterface callback interface, and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="3a3c6-121">Para obtener más información sobre CNotifyInterface, vea [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-121">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
7.  <span data-ttu-id="3a3c6-122">Llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para establecer los tipos de notificaciones que se van a recibir.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-122">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="3a3c6-123">En este ejemplo, se establecen las marcas de **\_ \_ \_ error** del trabajo de **notificación de BG \_ \_ \_ transferida** y de notificación de BG.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-123">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
8.  <span data-ttu-id="3a3c6-124">Obtenga un puntero a la interfaz [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) llamando al método **IBackgroundCopyJob:: QueryInterface** con el identificador de interfaz adecuado.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-124">Get a pointer to the [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) interface by calling the **IBackgroundCopyJob::QueryInterface** method with the proper interface identifier.</span></span>
9.  <span data-ttu-id="3a3c6-125">Intente iniciar sesión en el usuario del token de la aplicación auxiliar.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-125">Attempt to log on the user of the helper token.</span></span> <span data-ttu-id="3a3c6-126">Cree un identificador de suplantación y llame a la [función LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) para rellenar el identificador de suplantación.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-126">Create an impersonation handle, and call the [LogonUser Function]( /windows/win32/api/winbase/nf-winbase-logonusera) to populate the impersonation handle.</span></span> <span data-ttu-id="3a3c6-127">Si la operación se realiza correctamente, llame a la [función ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-127">If successful, call the [ImpersonateLoggedOnUser Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span></span> <span data-ttu-id="3a3c6-128">Si no se realiza correctamente, el ejemplo llama a la [función RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para finalizar la suplantación del usuario que ha iniciado sesión, se produce un error y se cierra el identificador.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-128">If unsuccessful, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
10. <span data-ttu-id="3a3c6-129">Llame al método [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para suplantar el token del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-129">Call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method to impersonate the token of the logged-on user.</span></span> <span data-ttu-id="3a3c6-130">Si se produce un error en este método, el ejemplo llama a la [función RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para finalizar la suplantación del usuario que ha iniciado sesión, se produce un error y se cierra el identificador.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-130">If this method fails, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
    > [!Note]
    >
    > <span data-ttu-id="3a3c6-131">En las versiones compatibles de Windows anteriores a Windows 10, versión 1607, el propietario del trabajo debe tener credenciales administrativas para llamar al método [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .</span><span class="sxs-lookup"><span data-stu-id="3a3c6-131">In supported versions of Windows before Windows 10, version 1607, the job owner must have administrative credentials to call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method.</span></span>
    >
    > <span data-ttu-id="3a3c6-132">A partir de Windows 10, versión 1607, los propietarios de trabajos que no son administradores pueden establecer tokens auxiliares que no son de administrador en trabajos de BITS que poseen.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-132">Starting with Windows 10, version 1607, non-administrator job owners can set non-administrator helper tokens on BITS jobs they own.</span></span> <span data-ttu-id="3a3c6-133">Los propietarios de los trabajos deben tener credenciales administrativas para establecer tokens auxiliares con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-133">Job owners must still have administrative credentials to set helper tokens with administrator privileges.</span></span>

     

11. <span data-ttu-id="3a3c6-134">Llame al método [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) para especificar a qué recursos acceder mediante el contexto de seguridad del token auxiliar.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-134">Call the [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) method to specify which resources to access using the helper token's security context.</span></span>
12. <span data-ttu-id="3a3c6-135">Una vez completada la suplantación, el ejemplo llama a la [función RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para finalizar la suplantación del usuario que ha iniciado sesión y el identificador está cerrado.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-135">After the impersonation is complete, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of logged on user, and the handle is closed.</span></span>
13. <span data-ttu-id="3a3c6-136">Agregue archivos al trabajo de transferencia de BITS llamando a [**IBackgroundCopyJob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-136">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span>
14. <span data-ttu-id="3a3c6-137">Una vez agregado el archivo, llame a [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para reanudar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-137">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="3a3c6-138">Configure un bucle while para esperar el mensaje de salida de la interfaz de devolución de llamada mientras se transfiere el trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-138">Set up a while loop to wait for the quit message from the callback interface while the job is transferring.</span></span> <span data-ttu-id="3a3c6-139">El bucle while utiliza la función [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar el número de milisegundos que han transcurrido desde que comenzó el trabajo de transferencia.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-139">The while loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>
16. <span data-ttu-id="3a3c6-140">Una vez completado el trabajo de transferencia de BITS, quite el trabajo de la cola mediante una llamada a [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="3a3c6-140">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="3a3c6-141">En el ejemplo de código siguiente se agrega un token de aplicación auxiliar a un trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="3a3c6-141">The following code example adds a helper token to a BITS transfer job.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3a3c6-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a3c6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a3c6-143">Tokens de aplicación auxiliar para trabajos de transferencia de BITS</span><span class="sxs-lookup"><span data-stu-id="3a3c6-143">Helper tokens for BITS transfer jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[<span data-ttu-id="3a3c6-144">**IBitsTokenOptions**</span><span class="sxs-lookup"><span data-stu-id="3a3c6-144">**IBitsTokenOptions**</span></span>](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[<span data-ttu-id="3a3c6-145">Ejemplo: clases comunes</span><span class="sxs-lookup"><span data-stu-id="3a3c6-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 