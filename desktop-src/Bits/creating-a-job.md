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
# <a name="creating-a-job"></a>Crear un trabajo

Para crear un trabajo de transferencia, llame al método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) . Después de que BITS cree el trabajo, [agregue archivos al trabajo](adding-files-to-a-job.md) y [modifique las propiedades del trabajo](setting-and-retrieving-the-properties-of-a-job.md) según sea necesario para la aplicación. Para activar el trabajo en la cola, llame al método [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .

El método [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crea un GUID que identifica de forma única el trabajo. El GUID se usa para [recuperar el trabajo de la cola de transferencia](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob). El nombre para mostrar que proporcione al crear el trabajo no es único. más de un trabajo puede usar el mismo nombre.

BITS limita el número de trabajos de la cola a 300 trabajos y el número de trabajos que un usuario puede crear en el trabajo 60. Estos límites no se aplican a los administradores o servicios. Para cambiar estos límites predeterminados, consulte [directivas de grupo](group-policies.md).

En el ejemplo siguiente se muestra cómo crear un trabajo de descarga. En el ejemplo se presupone que la \_ variable g pbcm es un puntero de interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) válido. Para obtener más información sobre cómo crear el puntero de interfaz **IBackgroundCopyManager** , consulte [conectarse al servicio bits](connecting-to-the-bits-service.md).


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



Para obtener la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) más reciente, llame al método **IBackgroundCopyJob:: QueryInterface** . En el ejemplo siguiente se muestra cómo obtener la interfaz [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .


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



 

 




