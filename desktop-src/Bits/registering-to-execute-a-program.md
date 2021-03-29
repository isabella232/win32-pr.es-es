---
title: Registro para ejecutar un programa
description: Puede registrarse para que BITS ejecute un programa basado en los eventos de error y de trabajo transferidos, pero no en los eventos modificados de trabajo. BITS ejecuta el programa en el contexto del usuario.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- BITS de notificación de eventos, línea de comandos
- registrando los BITS de notificación de la línea de comandos
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792261"
---
# <a name="registering-to-execute-a-program"></a><span data-ttu-id="d027d-106">Registro para ejecutar un programa</span><span class="sxs-lookup"><span data-stu-id="d027d-106">Registering to Execute a Program</span></span>

<span data-ttu-id="d027d-107">Puede registrarse para que BITS ejecute un programa basado en los eventos de error y de trabajo transferidos, pero no en los eventos modificados de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d027d-107">You can register to have BITS execute a program based on job transferred and error events, but not job modified events.</span></span> <span data-ttu-id="d027d-108">BITS ejecuta el programa en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="d027d-108">BITS executes the program in the user's context.</span></span>

<span data-ttu-id="d027d-109">**Para registrarse para ejecutar un programa**</span><span class="sxs-lookup"><span data-stu-id="d027d-109">**To register to execute a program**</span></span>

1.  <span data-ttu-id="d027d-110">Llame al método **IBackgroundCopyJob:: QueryInterface** para recuperar un puntero de la interfaz [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="d027d-110">Call the **IBackgroundCopyJob::QueryInterface** method to retrieve an [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface pointer.</span></span> <span data-ttu-id="d027d-111">Especifique \_ \_ Uuidof (IBackgroundCopyJob2) como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d027d-111">Specify \_\_uuidof(IBackgroundCopyJob2) as the interface identifier.</span></span>
2.  <span data-ttu-id="d027d-112">Llame al método [**IBackgroundCopyJob2:: SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) para especificar el programa que se va a ejecutar y los argumentos requeridos por el programa, como el identificador del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d027d-112">Call the [**IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) method to specify the program to execute and any arguments required by the program, such as the job identifier.</span></span>

3.  <span data-ttu-id="d027d-113">Llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para especificar Cuándo se ejecuta la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d027d-113">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to specify when the command line executes.</span></span>

    <span data-ttu-id="d027d-114">Solo puede especificar las marcas de evento de error de trabajo de notificación de BG \_ \_ \_ transferida y BG \_ Notify \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d027d-114">You can only specify the BG\_NOTIFY\_JOB\_TRANSFERRED and BG\_NOTIFY\_JOB\_ERROR event flags.</span></span> <span data-ttu-id="d027d-115">\_ \_ Se omitirá la marca de modificación del trabajo de notificación de BG \_ .</span><span class="sxs-lookup"><span data-stu-id="d027d-115">The BG\_NOTIFY\_JOB\_MODIFICATION flag is ignored.</span></span>

<span data-ttu-id="d027d-116">Tenga en cuenta que BITS no ejecutará el programa si también se [registró para recibir devoluciones de llamada com](registering-a-com-callback.md) y el puntero de la interfaz de devolución de llamada es válido o el método de notificación que llama a bits devuelve un código de operación correcta.</span><span class="sxs-lookup"><span data-stu-id="d027d-116">Note that BITS will not execute the program if you also [registered to receive COM callbacks](registering-a-com-callback.md) and the callback interface pointer is valid or the notification method that BITS calls returns a success code.</span></span> <span data-ttu-id="d027d-117">Sin embargo, si el método de notificación devuelve un código de error, como E \_ produce un error, bits ejecutará la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d027d-117">However, if the notification method returns a failure code, such as E\_FAIL, BITS will execute the command line.</span></span>

<span data-ttu-id="d027d-118">BITS llama a la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar el programa.</span><span class="sxs-lookup"><span data-stu-id="d027d-118">BITS calls the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to launch the program.</span></span> <span data-ttu-id="d027d-119">Si especifica una cadena de parámetro, el primer parámetro debe ser el nombre del programa.</span><span class="sxs-lookup"><span data-stu-id="d027d-119">If you specify a parameter string, the first parameter must be the program name.</span></span>

<span data-ttu-id="d027d-120">En el ejemplo siguiente se muestra cómo registrar para ejecutar un programa cuando se produce el evento de trabajo transferido.</span><span class="sxs-lookup"><span data-stu-id="d027d-120">The following example shows how to register to execute a program when the job-transferred event occurs.</span></span> <span data-ttu-id="d027d-121">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.</span><span class="sxs-lookup"><span data-stu-id="d027d-121">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


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



<span data-ttu-id="d027d-122">Cuando el estado del trabajo se convierte en el estado del trabajo de BG \_ \_ \_ transferido, bits ejecuta el programa especificado en pProgram.</span><span class="sxs-lookup"><span data-stu-id="d027d-122">When the state of the job becomes BG\_JOB\_STATE\_TRANSFERRED, BITS executes the program specified in pProgram.</span></span> <span data-ttu-id="d027d-123">El ejemplo siguiente es una implementación simple de un programa que toma un identificador de trabajo como argumento.</span><span class="sxs-lookup"><span data-stu-id="d027d-123">The following example is a simple implementation of a program that takes a job identifier as an argument.</span></span> <span data-ttu-id="d027d-124">El programa asume que se le pasa el número correcto de argumentos.</span><span class="sxs-lookup"><span data-stu-id="d027d-124">The program assumes the correct number of arguments are passed to it.</span></span>


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



 

 