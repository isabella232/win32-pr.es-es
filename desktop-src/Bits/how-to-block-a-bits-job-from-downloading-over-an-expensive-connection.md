---
title: Controlar una descarga de BITS a través de una conexión costosa
description: Bloquear la descarga a través de una conexión costosa, como un vínculo móvil móvil.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- descargar BITS, procedimientos
- descarga BITS, evitando costosas
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 6326838f08f1879929d9a6be67ef94c4aa035e00
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103904334"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a><span data-ttu-id="f14c1-105">Controlar una descarga de BITS a través de una conexión costosa</span><span class="sxs-lookup"><span data-stu-id="f14c1-105">Control a BITS download over an expensive connection</span></span>

<span data-ttu-id="f14c1-106">En este tema se muestra cómo bloquear un trabajo de BITS para que no se descargue a través de una conexión costosa, como un vínculo móvil móvil.</span><span class="sxs-lookup"><span data-stu-id="f14c1-106">This topic shows how to block a BITS job from downloading over an expensive connection such as a roaming cellular link.</span></span> <span data-ttu-id="f14c1-107">BITS es una API asincrónica en la que la aplicación crea un trabajo, agrega direcciones URL a ese trabajo y llama a la función de [**reanudación**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) del objeto de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f14c1-107">BITS is an asynchronous API where the application creates a job, adds URLs to that job, and calls the job object's [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) function.</span></span> <span data-ttu-id="f14c1-108">A partir de ese momento, BITS elige cuando el trabajo se descarga en función de factores como la prioridad del trabajo y la Directiva de transferencia.</span><span class="sxs-lookup"><span data-stu-id="f14c1-108">From that point, BITS chooses when the job downloads based on factors such as job priority and the transfer policy.</span></span> <span data-ttu-id="f14c1-109">Una vez finalizada la descarga del trabajo, BITS notifica a la aplicación que se ha descargado la dirección URL (si la aplicación se ha registrado para la notificación de finalización).</span><span class="sxs-lookup"><span data-stu-id="f14c1-109">After the job has finished downloading, BITS notifies the application that the URL has been downloaded (if the application has registered for completion notification).</span></span> <span data-ttu-id="f14c1-110">Durante la vigencia del trabajo, si cambia la red del usuario final (por ejemplo, si el usuario está viajando y actualmente está incurriendo en tarifas móviles), BITS suspenderá el trabajo hasta que las condiciones de la red sean óptimas.</span><span class="sxs-lookup"><span data-stu-id="f14c1-110">During the job's lifetime, if the end user's network changes—such as if the user is traveling and is currently incurring roaming fees—then BITS will suspend the job until network conditions are optimal.</span></span> <span data-ttu-id="f14c1-111">Las siguientes instrucciones paso a paso muestran cómo crear el trabajo y especificar la configuración de directiva de transferencia adecuada.</span><span class="sxs-lookup"><span data-stu-id="f14c1-111">The following step-by-step instructions show how to create the job and specify the appropriate transfer policy settings.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f14c1-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f14c1-112">Prerequisites</span></span>

-   <span data-ttu-id="f14c1-113">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f14c1-113">Microsoft Visual Studio</span></span>

## <a name="instructions"></a><span data-ttu-id="f14c1-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f14c1-114">Instructions</span></span>

### <a name="step-1-include-the-required-bits-header-files"></a><span data-ttu-id="f14c1-115">Paso 1: incluir los archivos de encabezado de BITS necesarios</span><span class="sxs-lookup"><span data-stu-id="f14c1-115">Step 1: Include the required BITS header files</span></span>

<span data-ttu-id="f14c1-116">Inserte las siguientes directivas de encabezado en la parte superior del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="f14c1-116">Insert the following header directives at the top of the source file.</span></span>


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a><span data-ttu-id="f14c1-117">Paso 2: inicializar COM</span><span class="sxs-lookup"><span data-stu-id="f14c1-117">Step 2: Initialize COM</span></span>

<span data-ttu-id="f14c1-118">Antes de crear una instancia de la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (que se usa para crear un trabajo de bits), debe inicializar com, establecer el modelo de subprocesos com y especificar un nivel de suplantación de, como mínimo, la \_ \_ \_ suplantación del nivel Imp de RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="f14c1-118">Before instantiating the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface (used to create a BITS job), you must initialize COM, set the COM threading model, and specify an impersonation level of at least RPC\_C\_IMP\_LEVEL\_IMPERSONATE.</span></span>


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a><span data-ttu-id="f14c1-119">Paso 3: crear una instancia de la interfaz IBackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="f14c1-119">Step 3: Instantiate the IBackgroundCopyManager interface</span></span>

<span data-ttu-id="f14c1-120">Use la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para crear trabajos de transferencia, recuperar un objeto de enumerador que contiene los trabajos de la cola y recuperar trabajos individuales de la cola.</span><span class="sxs-lookup"><span data-stu-id="f14c1-120">Use the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to create transfer jobs, retrieve an enumerator object that contains the jobs in the queue, and retrieve individual jobs from the queue.</span></span>


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a><span data-ttu-id="f14c1-121">Paso 4: crear el trabajo de BITS</span><span class="sxs-lookup"><span data-stu-id="f14c1-121">Step 4: Create the BITS job</span></span>

<span data-ttu-id="f14c1-122">Solo el usuario que crea el trabajo o un usuario con privilegios de administrador puede Agregar archivos al trabajo y cambiar las propiedades del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f14c1-122">Only the user who creates the job or a user with administrator privileges can add files to the job and change the job's properties.</span></span>


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a><span data-ttu-id="f14c1-123">Paso 5: especificar la configuración de la Directiva de transferencia para el trabajo</span><span class="sxs-lookup"><span data-stu-id="f14c1-123">Step 5: Specify the transfer policy setting for the job</span></span>

<span data-ttu-id="f14c1-124">Aquí es donde se especifica la Directiva de transferencia de estado de costo.</span><span class="sxs-lookup"><span data-stu-id="f14c1-124">This is where you specify the cost state transfer policy.</span></span> <span data-ttu-id="f14c1-125">Puede establecer varias marcas de estado de costo de BITS mediante \_ \_ una  combinación OR bit a bit para lograr los resultados deseados.</span><span class="sxs-lookup"><span data-stu-id="f14c1-125">You can set several BITS\_COST\_STATE flags by using a bitwise **OR** combination to achieve the desired results.</span></span>


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a><span data-ttu-id="f14c1-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f14c1-126">Example</span></span>

<span data-ttu-id="f14c1-127">En el ejemplo de código siguiente se muestra cómo establecer la Directiva de transferencia de un trabajo de BITS para que el procesamiento del trabajo no se produzca mientras se cumplen determinadas condiciones, como cuando el usuario está en itinerancia o ha superado su límite de transferencia de datos mensual.</span><span class="sxs-lookup"><span data-stu-id="f14c1-127">The following code example shows how to set a BITS job's transfer policy so that the processing of the job doesn't occur while certain conditions are met—such as when the user is roaming or has exceeded their monthly data transfer limit.</span></span>


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




