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
# <a name="enumerating-jobs-in-the-transfer-queue"></a>Enumerar trabajos en la cola de transferencia

Para enumerar los trabajos de la cola de transferencia, llame al método [**IBackgroundCopyManager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . El método devuelve un puntero de la interfaz [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) que se usa para enumerar los trabajos de la cola.

Para recuperar los trabajos del usuario, establezca el primer parámetro del método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) en 0. Para recuperar todos los trabajos de la cola, establezca el primer parámetro del método **EnumJobs** en la \_ enumeración del trabajo BG \_ \_ All \_ users. Solo los usuarios con privilegios de administrador pueden recuperar todos los trabajos de la cola de transferencia.

Tenga en cuenta que la lista enumerada es una instantánea de los trabajos de la cola de transferencia en el momento de llamar al método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . Sin embargo, los valores de propiedad de esos trabajos reflejan los valores actuales del trabajo.

Si desea recuperar trabajos de transferencia individuales, llame al método [**IBackgroundCopyManager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .

Para enumerar los archivos de un trabajo, consulte [enumerar archivos en un trabajo](enumerating-files-in-a-job.md).

En el ejemplo siguiente se muestra cómo enumerar los trabajos en la cola de transferencia. La \_ variable g XferManager en el ejemplo es un puntero de la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) . Para obtener más información sobre cómo crear el puntero de interfaz **IBackgroundCopyManager** , consulte [conectarse al servicio bits](connecting-to-the-bits-service.md).


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



 

 




