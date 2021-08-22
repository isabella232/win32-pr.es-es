---
title: Creación de un trabajo
description: Para crear un trabajo de transferencia, llame al método CreateJob de IBackgroundCopyManager.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- bits de trabajo de transferencia
- transferir bits de trabajo , crear
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0241d855d60178e87f28820f14b39e497f200fe5770933f293257e62b2d1b601
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528895"
---
# <a name="creating-a-job"></a>Creación de un trabajo

Para crear un trabajo de transferencia, llame al [**método IBackgroundCopyManager::CreateJob.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) Después de que BITS cree el trabajo, [agregue archivos al](adding-files-to-a-job.md) trabajo y [modifique](setting-and-retrieving-the-properties-of-a-job.md) las propiedades del trabajo según corresponda para la aplicación. Para activar el trabajo en la cola, llame al [**método IBackgroundCopyJob::Resume.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)

El [**método CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crea un GUID que identifica de forma única el trabajo. Use el GUID para recuperar [el trabajo de la cola de transferencia.](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) El nombre para mostrar que se proporciona al crear el trabajo no es único; más de un trabajo puede usar el mismo nombre.

BITS limita el número de trabajos de la cola a 300 trabajos y el número de trabajos que un usuario puede crear a 60 trabajos. Estos límites no se aplican a los administradores ni a los servicios. Para cambiar estos límites predeterminados, vea [Directivas de grupo.](group-policies.md)

En el ejemplo siguiente se muestra cómo crear un trabajo de descarga. En el ejemplo se supone que la \_ variable gismom es un puntero de interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) válido. Para obtener más información sobre cómo crear el puntero de interfaz **IBackgroundCopyManager,** vea [Conexión al servicio BITS](connecting-to-the-bits-service.md).


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



Para obtener la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) más reciente, llame al **método IBackgroundCopyJob::QueryInterface.** En el ejemplo siguiente se muestra cómo obtener la [**interfaz IBackgroundCopyJob5.**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)


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



 

 




