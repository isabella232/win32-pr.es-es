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
# <a name="handling-errors-bits"></a>Control de errores (BITS)

Hay dos tipos de errores que se pueden controlar en la aplicación. El primer error es una llamada al método con errores. Cada método devuelve un valor **HRESULT** . La página de referencia de cada método identifica los valores devueltos que es más probable que genere. Para obtener valores devueltos adicionales, vea [valores devueltos de bits](bits-return-values.md). Para obtener el texto del mensaje asociado al valor devuelto, llame al método [**IBackgroundCopyManager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .

El segundo tipo de error que se debe controlar es un trabajo cuyo [Estado](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) pasa [a \_ \_ \_ error de estado de trabajo de BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **\_ \_ \_ \_ error transitorio de estado de trabajo de BG**. Para recuperar información relacionada con estos tipos de errores, llame al método [**IBackgroundCopyJob:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) del trabajo. El método devuelve un puntero de la interfaz [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) que contiene información que se usa para determinar la causa del error. También puede recibir notificaciones de error si se registra para recibir la notificación de eventos. Para obtener más información, consulte [registrar una devolución de llamada com](registering-a-com-callback.md).

BITS considera que cada trabajo es atómico. Si uno de los archivos del trabajo genera un error, el trabajo permanece en un estado de error hasta que se resuelve el error. Por lo tanto, no se puede eliminar el archivo que está causando el error del trabajo. Sin embargo, si el error se debe a que el servidor no está disponible o un archivo remoto no válido, puede llamar al método [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2:: SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) para identificar un nuevo nombre de servidor o archivo.

Después de determinar la causa del error, realice una de las siguientes opciones:

-   Cancele el trabajo mediante una llamada al método [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .
-   Para un trabajo de descarga, llame al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para guardar los archivos transferidos correctamente antes de que se produjera el error.
-   Corrija el error y llame al método [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para finalizar el trabajo.

Para un trabajo de carga y respuesta, compruebe el valor del miembro **bytesTotal** de la estructura de progreso de la respuesta del trabajo de BG para determinar si el error se produjo en la parte de carga o respuesta del trabajo. [**\_ \_ \_**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) El error se produjo en la carga si el valor es BG \_ size \_ Unknown.

En el ejemplo siguiente se muestra cómo recuperar un puntero de la interfaz [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) . En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


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



 

 




