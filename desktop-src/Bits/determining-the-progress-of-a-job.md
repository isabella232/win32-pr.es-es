---
title: Determinar el progreso de un trabajo
description: BITS mantiene la información de progreso de cada trabajo. Use la información de progreso para determinar cuántos bytes y archivos se han transferido.
ms.assetid: 8bac62b3-cb7e-45ba-85f0-95f3a7e8bffd
keywords:
- bits de trabajo de transferencia, progreso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085ddcdeea106be2998f828879bc92273f22b328
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266671"
---
# <a name="determining-the-progress-of-a-job"></a>Determinar el progreso de un trabajo

BITS mantiene la información de progreso de cada trabajo. Use la información de progreso para determinar cuántos bytes y archivos se han transferido.

Para recuperar la información de progreso del trabajo, llame al método [**IBackgroundCopyJob::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) como se muestra en el ejemplo siguiente. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


```C++
#define PROGRESS_COMPLETE_LEN 50

HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR szProgressComplete[PROGRESS_COMPLETE_LEN+1];
BG_JOB_PROGRESS Progress;

hr = pJob->GetProgress(&Progress); 
if (FAILED(hr))
{
  //Handle error
}

//Because the BytesTotal member can be 0 or BG_SIZE_UNKNOWN, you may not be able 
//to determine a percentage value to display, such as 57%. It is best to display a 
//string that shows the number of bytes transferred. For example, "123456 of 
//999999" or "123456 of Unknown".
if (BG_SIZE_UNKNOWN == Progress.BytesTotal)
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of Unknown", 
     Progress.BytesTransferred);
}
else
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of %I64d", 
     Progress.BytesTransferred, Progress.BytesTotal); 
}
```



Para recuperar información de progreso sobre la parte de respuesta de un trabajo de respuesta de carga, llame al método [**IBackgroundCopyJob2::GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) como se muestra en el ejemplo siguiente. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


```C++
#define REPLY_COMPLETE_LEN 4

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szReplyComplete[REPLY_COMPLETE_LEN+1];
BG_JOB_REPLY_PROGRESS Progress;

pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
hr = pJob2->GetReplyProgress(&Progress); 
if (SUCCEEDED(hr))
{
  if (0 == Progress.BytesTotal) //The job type is not BG_JOB_TYPE_UPLOAD_REPLY
  {
    //Logic to deal with this case  
  }
  else if (BG_SIZE_UNKNOWN == Progress.BytesTotal) //The reply has not begun
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1, L"0%%");
  }
  else
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1 L"%I64d%%",
       100*Progress.BytesTransferred/Progress.BytesTotal); 
  }
}
```



Los archivos también contienen información de progreso. Para recuperar la información de progreso, use [**el método IBackgroundCopyFile::GetProgress.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyfile-getprogress) Para obtener información sobre cómo recuperar los archivos de un trabajo, vea [Enumerar archivos en un trabajo.](enumerating-files-in-a-job.md)

 

 




