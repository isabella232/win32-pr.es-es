---
title: Registro para ejecutar un programa
description: Puede registrarse para que BITS ejecute un programa basado en el trabajo transferido y los eventos de error, pero no en los eventos modificados del trabajo. BITS ejecuta el programa en el contexto del usuario.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- BITS de notificación de eventos, línea de comandos
- registro para bits de notificación de línea de comandos
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063410"
---
# <a name="registering-to-execute-a-program"></a>Registro para ejecutar un programa

Puede registrarse para que BITS ejecute un programa basado en el trabajo transferido y los eventos de error, pero no en los eventos modificados del trabajo. BITS ejecuta el programa en el contexto del usuario.

**Para registrarse para ejecutar un programa**

1.  Llame al **método IBackgroundCopyJob::QueryInterface** para recuperar un puntero de [**interfaz IBackgroundCopyJob2.**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) Especifique \_ \_ uuidof(IBackgroundCopyJob2) como identificador de interfaz.
2.  Llame al [**método IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) para especificar el programa que se ejecutará y los argumentos requeridos por el programa, como el identificador de trabajo.

3.  Llame al [**método IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para especificar cuándo se ejecuta la línea de comandos.

    Solo puede especificar las marcas de eventos BG \_ NOTIFY JOB TRANSFERRED y BG NOTIFY JOB \_ \_ \_ \_ \_ ERROR. Se omite la marca BG \_ NOTIFY \_ JOB \_ MODIFICATION.

Tenga en cuenta que BITS no ejecutará el programa si también se registró para recibir devoluciones de llamada [COM](registering-a-com-callback.md) y el puntero de interfaz de devolución de llamada es válido o el método de notificación que llama a BITS devuelve un código correcto. Sin embargo, si el método de notificación devuelve un código de error, como E \_ FAIL, BITS ejecutará la línea de comandos.

BITS llama a [**la función CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar el programa. Si especifica una cadena de parámetro, el primer parámetro debe ser el nombre del programa.

En el ejemplo siguiente se muestra cómo registrarse para ejecutar un programa cuando se produce el evento transferido por el trabajo. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


```C++
#define MAX_PARAMETER_LEN 4000

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szJobId[48];
const WCHAR *pProgram = L"c:\\PATHHERE\\PROGRAMNAMEHERE.exe";
WCHAR szParameters[MAX_PARAMETER_LEN+1];
GUID JobId;
int rc;

hr = pJob->GetId(&JobId);
if (SUCCEEDED(hr))
{
  rc = StringFromGUID2(JobId, szJobId, ARRAYSIZE(szJobId));
  if (rc)
  {
    StringCchPrintf(szParameters, MAX_PARAMETER_LEN+1, L"%s %s", pProgram, szJobId);
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    hr = pJob2->SetNotifyCmdLine(pProgram, szParameters);
    if (SUCCEEDED(hr))
    {
      hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED);
    }
    pJob2->Release();
    if (FAILED(hr))
    {
      //Handle error - unable to register for command line notification.
    }
  }
}
```



Cuando el estado del trabajo se convierte en BG \_ JOB \_ STATE \_ TRANSFERRED, BITS ejecuta el programa especificado en pProgram. El ejemplo siguiente es una implementación sencilla de un programa que toma un identificador de trabajo como argumento. El programa supone que se pasa el número correcto de argumentos.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <strsafe.h>

int wmain(int argc, wchar_t *argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *pManager = NULL;
 IBackgroundCopyJob *pJob = NULL;
 GUID JobId;
 LPWSTR pDisplayName = NULL;
 LPCWSTR pSuccessString = L" completed successfully.";
 LPWSTR pMessage;

 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
  NULL, CLSCTX_LOCAL_SERVER,
  __uuidof(IBackgroundCopyManager), (void**)&pManager);

 if (pManager)
 {
  hr = CLSIDFromString(argv[1], &JobId);
  if (SUCCEEDED(hr))
  {
   hr = pManager->GetJob(JobId, &pJob);
   if (SUCCEEDED(hr))
   {
    hr = pJob->GetDisplayName(&pDisplayName);
    if (SUCCEEDED(hr))
    {
     int messageLen = wcslen(pDisplayName) + wcslen(pSuccessString) + 1;
     pMessage = (WCHAR*)malloc(messageLen * sizeof(WCHAR));
     if (pMessage)
     {
      StringCchPrintf(pMessage, messageLen,
       L"%s%s", pDisplayName, pSuccessString);
      MessageBox(HWND_DESKTOP, pMessage, L"MyProgram - Transferred", MB_OK);
      free(pMessage);
     }
     else
     {
      hr = E_OUTOFMEMORY;
     }
     CoTaskMemFree(pDisplayName);
    }
    pJob->Release();
   }
  }
  pManager->Release();
 }

 CoUninitialize();
 return(hr);
}
```



 

 