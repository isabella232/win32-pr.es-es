---
title: Control de errores (BITS)
description: Hay dos tipos de errores que se pueden controlar en la aplicación.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- controlar BITS de errores
- transferir BITS de trabajo, errores
- BITS de errores
- BITS de errores, control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078687"
---
# <a name="handling-errors-bits"></a><span data-ttu-id="2832e-107">Control de errores (BITS)</span><span class="sxs-lookup"><span data-stu-id="2832e-107">Handling Errors (BITS)</span></span>

<span data-ttu-id="2832e-108">Hay dos tipos de errores que se pueden controlar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2832e-108">There are two types of errors to handle in your application.</span></span> <span data-ttu-id="2832e-109">El primer error es una llamada al método con errores.</span><span class="sxs-lookup"><span data-stu-id="2832e-109">The first error is a failed method call.</span></span> <span data-ttu-id="2832e-110">Cada método devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2832e-110">Each method returns an **HRESULT** value.</span></span> <span data-ttu-id="2832e-111">La página de referencia de cada método identifica los valores devueltos que es más probable que genere.</span><span class="sxs-lookup"><span data-stu-id="2832e-111">The reference page for each method identifies the return values that it is most likely to generate.</span></span> <span data-ttu-id="2832e-112">Para obtener valores devueltos adicionales, vea [valores devueltos de bits](bits-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2832e-112">For additional return values, see [BITS Return Values](bits-return-values.md).</span></span> <span data-ttu-id="2832e-113">Para obtener el texto del mensaje asociado al valor devuelto, llame al método [**IBackgroundCopyManager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .</span><span class="sxs-lookup"><span data-stu-id="2832e-113">To get the message text associated with the return value, call the [**IBackgroundCopyManager::GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) method.</span></span>

<span data-ttu-id="2832e-114">El segundo tipo de error que se debe controlar es un trabajo cuyo [Estado](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) pasa [a \_ \_ \_ error de estado de trabajo de BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **\_ \_ \_ \_ error transitorio de estado de trabajo de BG**.</span><span class="sxs-lookup"><span data-stu-id="2832e-114">The second type of error to handle is a job whose [state](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) transitions to [BG\_JOB\_STATE\_ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) or **BG\_JOB\_STATE\_TRANSIENT\_ERROR**.</span></span> <span data-ttu-id="2832e-115">Para recuperar información relacionada con estos tipos de errores, llame al método [**IBackgroundCopyJob:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2832e-115">To retrieve information related to these types of errors, call the job's [**IBackgroundCopyJob::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) method.</span></span> <span data-ttu-id="2832e-116">El método devuelve un puntero de la interfaz [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) que contiene información que se usa para determinar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="2832e-116">The method returns an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer that contains information you use to determine the cause of the error.</span></span> <span data-ttu-id="2832e-117">También puede recibir notificaciones de error si se registra para recibir la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="2832e-117">You can also receive error notification by registering to receive event notification.</span></span> <span data-ttu-id="2832e-118">Para obtener más información, consulte [registrar una devolución de llamada com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="2832e-118">For details, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="2832e-119">BITS considera que cada trabajo es atómico.</span><span class="sxs-lookup"><span data-stu-id="2832e-119">BITS considers each job to be atomic.</span></span> <span data-ttu-id="2832e-120">Si uno de los archivos del trabajo genera un error, el trabajo permanece en un estado de error hasta que se resuelve el error.</span><span class="sxs-lookup"><span data-stu-id="2832e-120">If one of the files in the job generates an error, the job remains in an error state until the error is resolved.</span></span> <span data-ttu-id="2832e-121">Por lo tanto, no se puede eliminar el archivo que está causando el error del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2832e-121">Thus, you cannot delete the file that is causing the error from the job.</span></span> <span data-ttu-id="2832e-122">Sin embargo, si el error se debe a que el servidor no está disponible o un archivo remoto no válido, puede llamar al método [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2:: SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) para identificar un nuevo nombre de servidor o archivo.</span><span class="sxs-lookup"><span data-stu-id="2832e-122">However, if the error is caused by the server not being available or an invalid remote file, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) or [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method to identify a new server or file name.</span></span>

<span data-ttu-id="2832e-123">Después de determinar la causa del error, realice una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="2832e-123">After determining the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="2832e-124">Cancele el trabajo mediante una llamada al método [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="2832e-124">Cancel the job by calling the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>
-   <span data-ttu-id="2832e-125">Para un trabajo de descarga, llame al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para guardar los archivos transferidos correctamente antes de que se produjera el error.</span><span class="sxs-lookup"><span data-stu-id="2832e-125">For a download job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method to save the files that transferred successfully before the error occurred.</span></span>
-   <span data-ttu-id="2832e-126">Corrija el error y llame al método [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para finalizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2832e-126">Fix the error and call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method to finish the job.</span></span>

<span data-ttu-id="2832e-127">Para un trabajo de carga y respuesta, compruebe el valor del miembro **bytesTotal** de la estructura de progreso de la respuesta del trabajo de BG para determinar si el error se produjo en la parte de carga o respuesta del trabajo. [**\_ \_ \_**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress)</span><span class="sxs-lookup"><span data-stu-id="2832e-127">For an upload-reply job, check the value of the **BytesTotal** member of the [**BG\_JOB\_REPLY\_PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) structure to determine if the error occurred on the upload or reply portion of the job.</span></span> <span data-ttu-id="2832e-128">El error se produjo en la carga si el valor es BG \_ size \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="2832e-128">The error occurred on the upload if the value is BG\_SIZE\_UNKNOWN.</span></span>

<span data-ttu-id="2832e-129">En el ejemplo siguiente se muestra cómo recuperar un puntero de la interfaz [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) .</span><span class="sxs-lookup"><span data-stu-id="2832e-129">The following example shows how to retrieve an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer.</span></span> <span data-ttu-id="2832e-130">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.</span><span class="sxs-lookup"><span data-stu-id="2832e-130">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




