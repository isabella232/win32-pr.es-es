---
title: Sondeo del estado del trabajo
description: De forma predeterminada, una aplicación debe sondear los cambios en el estado de un trabajo.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- transferir BITS de trabajo, sondeo
- sondeo de BITS de estado de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903167"
---
# <a name="polling-for-the-status-of-the-job"></a>Sondeo del estado del trabajo

De forma predeterminada, una aplicación debe sondear los cambios en el estado de un trabajo. Para capturar los cambios en el estado del trabajo, llame al método [**IBackgroundCopyJob:: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) . Para capturar los cambios en el número de bytes y archivos transferidos, llame al método [**IBackgroundCopyJob:: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) . Para recuperar información de progreso en la parte de respuesta de un trabajo de carga y respuesta, llame al método [**IBackgroundCopyJob2:: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) . Para obtener un ejemplo en el que se usa la información de progreso, vea [determinar el progreso de un trabajo](determining-the-progress-of-a-job.md).

La enumeración de [**\_ \_ Estado del trabajo de BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) define los Estados de un trabajo y la estructura de [**\_ \_ progreso del trabajo de BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contiene información sobre el número de bytes y archivos transferidos.

Para usar el sondeo, debe crear un mecanismo para iniciar el sondeo. Por ejemplo, cree un temporizador o use un botón "actualizar" en la interfaz de usuario. Sin embargo, puede ser más fácil registrarse para la notificación de eventos y recibir eventos cuando cambie el estado o el progreso. Para obtener información sobre la notificación de eventos, vea [registrar una devolución de llamada com](registering-a-com-callback.md).

En el ejemplo siguiente se usa un temporizador para sondear el estado de un trabajo. En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




