---
title: Recuperar la respuesta de un trabajo Upload-Reply trabajo
description: Para cargar datos en una aplicación de servidor y hacer que devuelvan datos al cliente, especifique el trabajo como un trabajo BG \_ JOB \_ TYPE UPLOAD \_ \_ REPLY.
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 79ca145a3ed243209fc0059b20823e32da3cf3974850a6bc3e872f43dbd40aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004885"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Recuperar la respuesta de un trabajo Upload-Reply trabajo

Un trabajo Upload-Reply BITS, además de cargar un archivo en un servidor, también examinará una dirección URL de respuesta enviada como parte de la respuesta del servidor y, a continuación, seguirá automáticamente la dirección URL de respuesta y descargará una respuesta de ella. Consulte la [documentación de Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) para obtener más detalles sobre el valor del encabezado BITS-Reply-URL.

Establezca el tipo de trabajo como BG \_ JOB TYPE UPLOAD REPLY para crear un Upload-Reply trabajo de tipo de \_ \_ \_ trabajo. Los datos de respuesta están disponibles para el cliente después de que el trabajo entre en el estado BG \_ JOB \_ STATE \_ TRANSFERRED. Para recuperar la respuesta, llame a uno de los métodos siguientes:

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Proporciona una copia en memoria de los datos de respuesta. Use este método para leer los datos de respuesta antes o después de llamar al [**método IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Si los datos de respuesta superan los 1 MB, la aplicación debe llamar al método [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) para recuperar el nombre del archivo de respuesta y leer su contenido directamente.

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Proporciona el nombre del archivo que contiene la respuesta. Debe llamar al método **IBackgroundCopyJob::Complete** antes de abrir y leer el archivo de respuesta. el archivo de respuesta no está disponible para el cliente hasta que se llama al **método** Complete.

Llame a estos métodos en el método [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) solo si la respuesta es pequeña y se puede procesar rápidamente para no bloquear el subproceso de devolución de llamada. Si usa la notificación [**de línea de comandos en**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) lugar de la devolución de llamada, pase el identificador del trabajo al archivo ejecutable. El archivo ejecutable usa el identificador de trabajo para llamar al **método Complete** para que el archivo de respuesta esté disponible.

En los ejemplos siguientes se muestra cómo usar cada método para recuperar los datos de respuesta.

-   [Uso de GetReplyData](#using-getreplydata)
-   [Uso de GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Uso de GetReplyData

En el ejemplo siguiente se muestra cómo recuperar los datos de respuesta mediante el [**método IBackgroundCopyJob2::GetReplyData.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) En el ejemplo se supone que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido, el tipo del trabajo es upload-reply y el estado del trabajo es BG \_ JOB STATE \_ \_ TRANSFERRED.


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



## <a name="using-getreplyfilename"></a>Uso de GetReplyFileName

En el ejemplo siguiente se muestra cómo recuperar los datos de respuesta mediante el [**método IBackgroundCopyJob2::GetReplyFileName.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) En el ejemplo se supone que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido, el tipo de trabajo es upload-reply y el estado del trabajo es BG \_ JOB STATE \_ \_ TRANSFERRED.


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



 

 




