---
title: Recuperación de la respuesta de un trabajo Upload-Reply
description: Para cargar datos en una aplicación de servidor y devolver datos al cliente, especifique el trabajo como el tipo de trabajo de BG \_ \_ \_ \_ Job upload Response.
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993969"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Recuperación de la respuesta de un trabajo Upload-Reply

Un trabajo de Upload-Reply BITS, además de cargar un archivo en un servidor, también examinará una dirección URL de respuesta que se envía como parte de la respuesta del servidor y, a continuación, sigue automáticamente la dirección URL de respuesta y descarga una respuesta de ella. Consulte la documentación [de ACK for Fragment](/windows/desktop/Bits/ack-for-fragment) para obtener más detalles sobre el valor de encabezado bits-respuesta-URL.

Establezca el tipo de trabajo como \_ tipo de trabajo BG \_ \_ enviar \_ respuesta para crear un trabajo de tipo Upload-Reply. Los datos de la respuesta están disponibles para el cliente después de que el trabajo entre en el estado de trabajo de BG en \_ \_ \_ Estado transferido. Para recuperar la respuesta, llame a uno de los métodos siguientes:

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Proporciona una copia en memoria de los datos de la respuesta. Use este método para leer los datos de la respuesta antes o después de llamar al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Si los datos de respuesta superan 1 MB, la aplicación debe llamar al método [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) para recuperar el nombre del archivo de respuesta y leer su contenido directamente.

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Proporciona el nombre del archivo que contiene la respuesta. Debe llamar al método **IBackgroundCopyJob:: Complete** antes de abrir y leer el archivo de respuesta; el archivo de respuesta no está disponible para el cliente hasta que se llama al método **Complete** .

Llame a estos métodos en el método [**IBackgroundCopyCallback:: JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) solo si la respuesta es pequeña y se puede procesar rápidamente para que no bloquee el subproceso de devolución de llamada. Si usa la [**notificación**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) de la línea de comandos en lugar de la devolución de llamada, pase el identificador del trabajo al archivo ejecutable. El archivo ejecutable utiliza el identificador de trabajo para llamar al método **Complete** para que el archivo de respuesta esté disponible.

En los siguientes ejemplos se muestra cómo utilizar cada método para recuperar los datos de la respuesta.

-   [Usar GetReplyData](#using-getreplydata)
-   [Usar GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Usar GetReplyData

En el ejemplo siguiente se muestra cómo recuperar los datos de respuesta mediante el método [**IBackgroundCopyJob2:: GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) . En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido, el tipo del trabajo es upload-Response y el estado del trabajo es transferencia de estado del trabajo de BG \_ \_ \_ .


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BYTE* pReply = NULL;
UINT64 ReplySize;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyData method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyData(&pReply, &ReplySize);
    if (S_OK == hr))
    {
        if (pReply)
        {
            //Do something with the data.
            CoTaskMemFree(pReply);
        }
        else
        {
            //The server application did not return a reply.
        }
    }
    else if (BG_E_TOO_LARGE == hr)
    {
        //The reply exceeds 1 MB. To retrieve the reply, get the reply file name,
        //complete the job, open the reply file, and read the reply.
    }
    else
    {
        //Handle the error
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



## <a name="using-getreplyfilename"></a>Usar GetReplyFileName

En el ejemplo siguiente se muestra cómo recuperar los datos de respuesta mediante el método [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) . En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido, el tipo de trabajo es upload-Response y el estado del trabajo es transferencia de estado del trabajo de BG \_ \_ \_ .


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR* pszFileName = NULL;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyFileName method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        //Calling the Complete method removes the job from the queue, 
        //so make sure you maintain an interface pointer to this job 
        //or retrieve any job related information that you require 
        //when processing the reply.
        hr = pJob->Complete();

        //Open, read the file, and do something with the data.
        CoTaskMemFree(pszFileName);
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



 

 




