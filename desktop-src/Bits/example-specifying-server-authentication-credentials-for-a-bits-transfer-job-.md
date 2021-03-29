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
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a><span data-ttu-id="ac701-103">Especificar credenciales de autenticación de servidor para un trabajo de transferencia de BITS</span><span class="sxs-lookup"><span data-stu-id="ac701-103">Specify server authentication credentials for a BITS transfer job</span></span>

<span data-ttu-id="ac701-104">Puede especificar diferentes esquemas de autenticación para un trabajo de transferencia de Servicio de transferencia inteligente en segundo plano (BITS).</span><span class="sxs-lookup"><span data-stu-id="ac701-104">You can specify different authentication schemes for a Background Intelligent Transfer Service (BITS) transfer job.</span></span>

<span data-ttu-id="ac701-105">El siguiente procedimiento obtiene un esquema de autenticación y crea una estructura de identidad de autenticación.</span><span class="sxs-lookup"><span data-stu-id="ac701-105">The following procedure gets an authentication scheme and creates an authentication identity structure.</span></span> <span data-ttu-id="ac701-106">A continuación, la aplicación crea un trabajo de descarga de BITS y establece las credenciales para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac701-106">Then the application creates a BITS download job and sets the credentials for the job.</span></span> <span data-ttu-id="ac701-107">Una vez creado el trabajo, la aplicación obtiene un puntero a una interfaz de devolución de llamada y sondea el estado del trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="ac701-107">After the job is created, the application gets a pointer to a callback interface and polls for the status of the BITS transfer job.</span></span> <span data-ttu-id="ac701-108">Una vez completado el trabajo, se quita de la cola.</span><span class="sxs-lookup"><span data-stu-id="ac701-108">After the job is complete, it is removed from the queue.</span></span>

<span data-ttu-id="ac701-109">En este ejemplo se usa el encabezado y la implementación definidos en el [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ac701-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="ac701-110">**Para especificar las credenciales de autenticación del servidor para un trabajo de transferencia de BITS**</span><span class="sxs-lookup"><span data-stu-id="ac701-110">**To specify server authentication credentials for a BITS transfer job**</span></span>

1.  <span data-ttu-id="ac701-111">Cree una estructura de contenedor que asigne los valores de [**\_ \_ esquema de autenticación BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) a los nombres de esquema.</span><span class="sxs-lookup"><span data-stu-id="ac701-111">Create a container structure that maps [**BG\_AUTH\_SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) values to scheme names.</span></span>

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

    

2.  <span data-ttu-id="ac701-112">Inicialice los parámetros COM llamando a la función CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="ac701-112">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="ac701-113">Para obtener más información sobre la función CCoInitializer, vea [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ac701-113">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
3.  <span data-ttu-id="ac701-114">Preparar una estructura de [**\_ \_ credenciales de autenticación BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="ac701-114">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span> <span data-ttu-id="ac701-115">En el ejemplo se usa la función [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) para borrar las ubicaciones de memoria asociadas a la información confidencial.</span><span class="sxs-lookup"><span data-stu-id="ac701-115">The example uses the [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function to clear the memory locations associated with the sensitive information.</span></span> <span data-ttu-id="ac701-116">La función [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) se define en Winbase. h.</span><span class="sxs-lookup"><span data-stu-id="ac701-116">The [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function is defined in WinBase.h.</span></span>
4.  <span data-ttu-id="ac701-117">Utilice la función GetScheme para obtener el esquema de autenticación que se va a usar para conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="ac701-117">Use the GetScheme function to get the authentication scheme to use to connect to the server.</span></span>

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

    

5.  <span data-ttu-id="ac701-118">Rellene la estructura de [**\_ \_ credenciales**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) de autenticación BG con el esquema de autenticación devuelto por la función GetScheme y el nombre de usuario y la contraseña que se pasaron a la función ServerAuthentication.</span><span class="sxs-lookup"><span data-stu-id="ac701-118">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure with the authentication scheme returned by the GetScheme function and the user name and password that were passed into the ServerAuthentication function.</span></span>
6.  <span data-ttu-id="ac701-119">Obtiene un puntero a la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).</span><span class="sxs-lookup"><span data-stu-id="ac701-119">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface (pJob).</span></span>
7.  <span data-ttu-id="ac701-120">Inicialice la seguridad del proceso COM llamando a [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="ac701-120">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="ac701-121">BITS requiere al menos el nivel de suplantación de suplantación.</span><span class="sxs-lookup"><span data-stu-id="ac701-121">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="ac701-122">BITS produce un error con E \_ ACCESSDENIED si no se establece el nivel de suplantación correcto.</span><span class="sxs-lookup"><span data-stu-id="ac701-122">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
8.  <span data-ttu-id="ac701-123">Obtiene un puntero a la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) y obtiene el localizador inicial a bits llamando a la función [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="ac701-123">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
9.  <span data-ttu-id="ac701-124">Cree un trabajo de transferencia de BITS llamando al método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="ac701-124">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
10. <span data-ttu-id="ac701-125">Obtiene un puntero a la interfaz de devolución de llamada CNotifyInterface y llama al método [**IBackgroundCopyJob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para recibir la notificación de eventos relacionados con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac701-125">Get a pointer to the CNotifyInterface callback interface and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="ac701-126">Para obtener más información sobre CNotifyInterface, vea [ejemplo: clases comunes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ac701-126">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
11. <span data-ttu-id="ac701-127">Llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para establecer los tipos de notificaciones que se van a recibir.</span><span class="sxs-lookup"><span data-stu-id="ac701-127">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="ac701-128">En este ejemplo, se establecen las marcas de **\_ \_ \_ error** del trabajo de **notificación de BG \_ \_ \_ transferida** y de notificación de BG.</span><span class="sxs-lookup"><span data-stu-id="ac701-128">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
12. <span data-ttu-id="ac701-129">Obtiene un puntero a la interfaz [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="ac701-129">Get a pointer to the [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface.</span></span> <span data-ttu-id="ac701-130">Use el puntero **IBackgroundCopyJob2** para establecer propiedades adicionales en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac701-130">Use the **IBackgroundCopyJob2** pointer to set additional properties on the job.</span></span> <span data-ttu-id="ac701-131">Este programa usa el método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para establecer las credenciales para el trabajo de transferencia de bits.</span><span class="sxs-lookup"><span data-stu-id="ac701-131">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
13. <span data-ttu-id="ac701-132">Agregue archivos al trabajo de transferencia de BITS llamando a [**IBackgroundCopyJob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="ac701-132">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span> <span data-ttu-id="ac701-133">En este ejemplo, el método **IBackgroundCopyJob:: AddFile** usa las variables Archivoremoto y archivolocal que se pasaron a la función ServerAuthentication.</span><span class="sxs-lookup"><span data-stu-id="ac701-133">In this example, the **IBackgroundCopyJob::AddFile** method uses the remoteFile and localFile variables that were passed into the ServerAuthentication function.</span></span>
14. <span data-ttu-id="ac701-134">Una vez agregado el archivo, llame a [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para reanudar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac701-134">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="ac701-135">Configure un bucle while para esperar el mensaje de salida de la interfaz de devolución de llamada mientras se transfiere el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac701-135">Set up a while loop to wait for Quit Message from the callback interface while the job is transferring.</span></span>

    > [!Note]  
    > <span data-ttu-id="ac701-136">Este paso solo es necesario si el apartamento COM es un contenedor uniproceso.</span><span class="sxs-lookup"><span data-stu-id="ac701-136">This step is necessary only if the COM apartment is a single-threaded apartment.</span></span> <span data-ttu-id="ac701-137">Para obtener más información, consulte [apartamentos de un solo subproceso](../com/single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="ac701-137">For more information, see [Single-Threaded Apartments](../com/single-threaded-apartments.md).</span></span>

     

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

    

    <span data-ttu-id="ac701-138">El bucle anterior utiliza la función [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar el número de milisegundos que han transcurrido desde que el trabajo empezó a transferir.</span><span class="sxs-lookup"><span data-stu-id="ac701-138">The preceding loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>

16. <span data-ttu-id="ac701-139">Una vez completado el trabajo de transferencia de BITS, quite el trabajo de la cola mediante una llamada a [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="ac701-139">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="ac701-140">En el ejemplo de código siguiente se especifican las credenciales de autenticación del servidor para un trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="ac701-140">The following code example specifies server authentication credentials for a BITS transfer job.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ac701-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac701-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac701-142">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="ac701-142">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="ac701-143">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="ac701-143">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="ac701-144">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="ac701-144">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="ac701-145">Ejemplo: clases comunes</span><span class="sxs-lookup"><span data-stu-id="ac701-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 