---
title: Control de errores (BITS)
description: Hay dos tipos de errores para controlar en la aplicación.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- control de errores BITS
- transferir bits de trabajo , errores
- BITS de errores
- errores bits , control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1b0f389b6f0bdeefdfd5868b444384af26027b9b688a8fb83ba89ea370b9360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528815"
---
# <a name="handling-errors-bits"></a>Control de errores (BITS)

Hay dos tipos de errores para controlar en la aplicación. El primer error es una llamada al método con error. Cada método devuelve un **valor HRESULT.** La página de referencia de cada método identifica los valores devueltos que es más probable que genere. Para obtener valores devueltos adicionales, [vea Valores devueltos de BITS](bits-return-values.md). Para obtener el texto del mensaje asociado al valor devuelto, llame al método [**IBackgroundCopyManager::GetErrorDescription.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription)

El segundo tipo de error que [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) se va a controlar es un trabajo cuyo estado pasa a [BG JOB \_ STATE \_ \_ ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR**. Para recuperar información relacionada con estos tipos de errores, llame al método [**IBackgroundCopyJob::GetError del**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) trabajo. El método devuelve un [**puntero de interfaz IBackgroundCopyError que**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) contiene información que se usa para determinar la causa del error. También puede recibir una notificación de error si se registra para recibir la notificación de eventos. Para obtener más información, [vea Registrar una devolución de llamada COM.](registering-a-com-callback.md)

BITS considera que cada trabajo es atómico. Si uno de los archivos del trabajo genera un error, el trabajo permanece en estado de error hasta que se resuelve el error. Por lo tanto, no se puede eliminar el archivo que está causando el error del trabajo. Sin embargo, si el error se debe a que el servidor no está disponible o a un archivo remoto no válido, puede llamar al método [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) para identificar un nuevo nombre de archivo o servidor.

Después de determinar la causa del error, realice una de las siguientes opciones:

-   Cancele el trabajo llamando al [**método IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   Para un trabajo de descarga, llame al método [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para guardar los archivos transferidos correctamente antes de que se produjese el error.
-   Corrija el error y llame [**al método IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para finalizar el trabajo.

Para un trabajo de carga y respuesta, compruebe el valor del miembro **BytesTotal** de la estructura [**BG JOB REPLY \_ \_ \_ PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) para determinar si el error se produjo en la parte de carga o respuesta del trabajo. El error se produjo en la carga si el valor es BG \_ SIZE \_ UNKNOWN.

En el ejemplo siguiente se muestra cómo recuperar un puntero de [**interfaz IBackgroundCopyError.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) En el ejemplo se supone que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


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



 

 




