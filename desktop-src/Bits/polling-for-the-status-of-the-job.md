---
title: Sondeo del estado del trabajo
description: De forma predeterminada, una aplicación debe sondear si hay cambios en el estado de un trabajo.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- bits de trabajo de transferencia, sondeo
- sondeo de bits de estado de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167998"
---
# <a name="polling-for-the-status-of-the-job"></a>Sondeo del estado del trabajo

De forma predeterminada, una aplicación debe sondear si hay cambios en el estado de un trabajo. Para capturar los cambios en el estado del trabajo, llame al [**método IBackgroundCopyJob::GetState.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) Para capturar los cambios en el número de bytes y archivos transferidos, llame al método [**IBackgroundCopyJob::GetProgress.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) Para recuperar información de progreso sobre la parte de respuesta de un trabajo de carga y respuesta, llame al método [**IBackgroundCopyJob2::GetReplyProgress.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) Para obtener un ejemplo en el que se usa la información de progreso, vea [Determinar el progreso de un trabajo.](determining-the-progress-of-a-job.md)

La [**\_ enumeración BG JOB \_ STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) define los estados de un trabajo y la estructura [**BG JOB \_ \_ PROGRESS**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contiene información sobre el número de bytes y archivos transferidos.

Para usar el sondeo, debe crear un mecanismo para iniciar el sondeo. Por ejemplo, cree un temporizador o use un botón "Actualizar" en la interfaz de usuario. Sin embargo, puede ser más fácil registrarse para la notificación de eventos y recibir eventos cuando cambia el estado o el progreso. Para obtener información sobre la notificación de eventos, [vea Registrar una devolución de llamada COM.](registering-a-com-callback.md)

En el ejemplo siguiente se usa un temporizador para sondear el estado de un trabajo. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


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



 

 




