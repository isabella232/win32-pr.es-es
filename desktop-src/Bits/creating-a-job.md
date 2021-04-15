---
title: Crear un trabajo
description: Para crear un trabajo de transferencia, llame al método IBackgroundCopyManager CreateJob.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- transferir BITS de trabajo
- transferir BITS de trabajo, crear
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486662"
---
# <a name="creating-a-job"></a><span data-ttu-id="283c3-105">Crear un trabajo</span><span class="sxs-lookup"><span data-stu-id="283c3-105">Creating a Job</span></span>

<span data-ttu-id="283c3-106">Para crear un trabajo de transferencia, llame al método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="283c3-106">To create a transfer job, call the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span> <span data-ttu-id="283c3-107">Después de que BITS cree el trabajo, [agregue archivos al trabajo](adding-files-to-a-job.md) y [modifique las propiedades del trabajo](setting-and-retrieving-the-properties-of-a-job.md) según sea necesario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="283c3-107">After BITS creates the job, [add files to the job](adding-files-to-a-job.md) and [modify the job's properties](setting-and-retrieving-the-properties-of-a-job.md) as appropriate for your application.</span></span> <span data-ttu-id="283c3-108">Para activar el trabajo en la cola, llame al método [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .</span><span class="sxs-lookup"><span data-stu-id="283c3-108">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method.</span></span>

<span data-ttu-id="283c3-109">El método [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crea un GUID que identifica de forma única el trabajo.</span><span class="sxs-lookup"><span data-stu-id="283c3-109">The [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method creates a GUID that uniquely identifies the job.</span></span> <span data-ttu-id="283c3-110">El GUID se usa para [recuperar el trabajo de la cola de transferencia](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="283c3-110">You use the GUID to [retrieve the job from the transfer queue](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span> <span data-ttu-id="283c3-111">El nombre para mostrar que proporcione al crear el trabajo no es único. más de un trabajo puede usar el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="283c3-111">The display name that you provide when you create the job is not unique; more than one job can use the same name.</span></span>

<span data-ttu-id="283c3-112">BITS limita el número de trabajos de la cola a 300 trabajos y el número de trabajos que un usuario puede crear en el trabajo 60.</span><span class="sxs-lookup"><span data-stu-id="283c3-112">BITS limits the number of jobs in the queue to 300 jobs and the number of jobs that a user can create to 60 job.</span></span> <span data-ttu-id="283c3-113">Estos límites no se aplican a los administradores o servicios.</span><span class="sxs-lookup"><span data-stu-id="283c3-113">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="283c3-114">Para cambiar estos límites predeterminados, consulte [directivas de grupo](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="283c3-114">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="283c3-115">En el ejemplo siguiente se muestra cómo crear un trabajo de descarga.</span><span class="sxs-lookup"><span data-stu-id="283c3-115">The following example shows how to create a download job.</span></span> <span data-ttu-id="283c3-116">En el ejemplo se presupone que la \_ variable g pbcm es un puntero de interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) válido.</span><span class="sxs-lookup"><span data-stu-id="283c3-116">The example assumes the g\_pbcm variable is a valid [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="283c3-117">Para obtener más información sobre cómo crear el puntero de interfaz **IBackgroundCopyManager** , consulte [conectarse al servicio bits](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="283c3-117">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



<span data-ttu-id="283c3-118">Para obtener la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) más reciente, llame al método **IBackgroundCopyJob:: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="283c3-118">To get the latest [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface, call the **IBackgroundCopyJob::QueryInterface** method.</span></span> <span data-ttu-id="283c3-119">En el ejemplo siguiente se muestra cómo obtener la interfaz [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .</span><span class="sxs-lookup"><span data-stu-id="283c3-119">The following example shows how to get the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface.</span></span>


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




