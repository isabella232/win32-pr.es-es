---
title: Enumerar trabajos en la cola de transferencia
description: Para enumerar los trabajos de la cola de transferencia, llame al método IBackgroundCopyManager EnumJobs. El método devuelve un puntero de la interfaz IEnumBackgroundCopyJobs que se usa para enumerar los trabajos de la cola.
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- BITS de trabajo de transferencia, enumeración
- enumerar trabajos en los BITS de la cola de transferencia
- BITS de la cola de transferencia, enumeración
- enumerar BITS
- enumerar BITS, trabajos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356742"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a><span data-ttu-id="4022d-109">Enumerar trabajos en la cola de transferencia</span><span class="sxs-lookup"><span data-stu-id="4022d-109">Enumerating Jobs in the Transfer Queue</span></span>

<span data-ttu-id="4022d-110">Para enumerar los trabajos de la cola de transferencia, llame al método [**IBackgroundCopyManager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="4022d-110">To enumerate jobs from the transfer queue, call the [**IBackgroundCopyManager::EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="4022d-111">El método devuelve un puntero de la interfaz [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) que se usa para enumerar los trabajos de la cola.</span><span class="sxs-lookup"><span data-stu-id="4022d-111">The method returns an [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) interface pointer that you use to enumerate the jobs in the queue.</span></span>

<span data-ttu-id="4022d-112">Para recuperar los trabajos del usuario, establezca el primer parámetro del método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) en 0.</span><span class="sxs-lookup"><span data-stu-id="4022d-112">To retrieve the user's jobs, set the first parameter of the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method to 0.</span></span> <span data-ttu-id="4022d-113">Para recuperar todos los trabajos de la cola, establezca el primer parámetro del método **EnumJobs** en la \_ enumeración del trabajo BG \_ \_ All \_ users.</span><span class="sxs-lookup"><span data-stu-id="4022d-113">To retrieve all jobs in the queue, set the first parameter of the **EnumJobs** method to BG\_JOB\_ENUM\_ALL\_USERS.</span></span> <span data-ttu-id="4022d-114">Solo los usuarios con privilegios de administrador pueden recuperar todos los trabajos de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="4022d-114">Only users with administrator privileges can retrieve all jobs in the transfer queue.</span></span>

<span data-ttu-id="4022d-115">Tenga en cuenta que la lista enumerada es una instantánea de los trabajos de la cola de transferencia en el momento de llamar al método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="4022d-115">Note that the enumerated list is a snapshot of the jobs in the transfer queue at the time you call the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="4022d-116">Sin embargo, los valores de propiedad de esos trabajos reflejan los valores actuales del trabajo.</span><span class="sxs-lookup"><span data-stu-id="4022d-116">However, the property values of those jobs reflect the current values of the job.</span></span>

<span data-ttu-id="4022d-117">Si desea recuperar trabajos de transferencia individuales, llame al método [**IBackgroundCopyManager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .</span><span class="sxs-lookup"><span data-stu-id="4022d-117">If you want to retrieve individual transfer jobs, call the [**IBackgroundCopyManager::GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) method.</span></span>

<span data-ttu-id="4022d-118">Para enumerar los archivos de un trabajo, consulte [enumerar archivos en un trabajo](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="4022d-118">To enumerate files in a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="4022d-119">En el ejemplo siguiente se muestra cómo enumerar los trabajos en la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="4022d-119">The following example shows how to enumerate jobs in the transfer queue.</span></span> <span data-ttu-id="4022d-120">La \_ variable g XferManager en el ejemplo es un puntero de la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="4022d-120">The g\_XferManager variable in the example is an [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="4022d-121">Para obtener más información sobre cómo crear el puntero de interfaz **IBackgroundCopyManager** , consulte [conectarse al servicio bits](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="4022d-121">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




