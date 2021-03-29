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
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a><span data-ttu-id="46944-103">Recuperación de la respuesta de un trabajo Upload-Reply</span><span class="sxs-lookup"><span data-stu-id="46944-103">Retrieving the Reply from an Upload-Reply Job</span></span>

<span data-ttu-id="46944-104">Un trabajo de Upload-Reply BITS, además de cargar un archivo en un servidor, también examinará una dirección URL de respuesta que se envía como parte de la respuesta del servidor y, a continuación, sigue automáticamente la dirección URL de respuesta y descarga una respuesta de ella.</span><span class="sxs-lookup"><span data-stu-id="46944-104">A BITS Upload-Reply job, in addition to uploading a file to a server, will also examine a reply URL sent as part of the server reply and then automatically follow the reply URL and download a response from it.</span></span> <span data-ttu-id="46944-105">Consulte la documentación [de ACK for Fragment](/windows/desktop/Bits/ack-for-fragment) para obtener más detalles sobre el valor de encabezado bits-respuesta-URL.</span><span class="sxs-lookup"><span data-stu-id="46944-105">See the [Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) documentation for more details about the BITS-Reply-URL header value.</span></span>

<span data-ttu-id="46944-106">Establezca el tipo de trabajo como \_ tipo de trabajo BG \_ \_ enviar \_ respuesta para crear un trabajo de tipo Upload-Reply.</span><span class="sxs-lookup"><span data-stu-id="46944-106">Set the job type as BG\_JOB\_TYPE\_UPLOAD\_REPLY to create an Upload-Reply type job.</span></span> <span data-ttu-id="46944-107">Los datos de la respuesta están disponibles para el cliente después de que el trabajo entre en el estado de trabajo de BG en \_ \_ \_ Estado transferido.</span><span class="sxs-lookup"><span data-stu-id="46944-107">The reply data is available to the client after the job enters the BG\_JOB\_STATE\_TRANSFERRED state.</span></span> <span data-ttu-id="46944-108">Para recuperar la respuesta, llame a uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="46944-108">To retrieve the reply, call one of the following methods:</span></span>

-   [<span data-ttu-id="46944-109">**IBackgroundCopyJob2::GetReplyData**</span><span class="sxs-lookup"><span data-stu-id="46944-109">**IBackgroundCopyJob2::GetReplyData**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    <span data-ttu-id="46944-110">Proporciona una copia en memoria de los datos de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46944-110">Provides an in-memory copy of the reply data.</span></span> <span data-ttu-id="46944-111">Use este método para leer los datos de la respuesta antes o después de llamar al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="46944-111">Use this method to read the reply data before or after calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="46944-112">Si los datos de respuesta superan 1 MB, la aplicación debe llamar al método [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) para recuperar el nombre del archivo de respuesta y leer su contenido directamente.</span><span class="sxs-lookup"><span data-stu-id="46944-112">If the reply data exceeds 1 MB, the application must call the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method to retrieve the name of the reply file and read its contents directly.</span></span>

-   [<span data-ttu-id="46944-113">**IBackgroundCopyJob2::GetReplyFileName**</span><span class="sxs-lookup"><span data-stu-id="46944-113">**IBackgroundCopyJob2::GetReplyFileName**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    <span data-ttu-id="46944-114">Proporciona el nombre del archivo que contiene la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46944-114">Provides the name of the file that contains the reply.</span></span> <span data-ttu-id="46944-115">Debe llamar al método **IBackgroundCopyJob:: Complete** antes de abrir y leer el archivo de respuesta; el archivo de respuesta no está disponible para el cliente hasta que se llama al método **Complete** .</span><span class="sxs-lookup"><span data-stu-id="46944-115">You must call the **IBackgroundCopyJob::Complete** method before opening and reading the reply file; the reply file is not available to the client until you call the **Complete** method.</span></span>

<span data-ttu-id="46944-116">Llame a estos métodos en el método [**IBackgroundCopyCallback:: JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) solo si la respuesta es pequeña y se puede procesar rápidamente para que no bloquee el subproceso de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="46944-116">Call these methods in your [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) method only if the reply is small and can be processed quickly so as to not block the callback thread.</span></span> <span data-ttu-id="46944-117">Si usa la [**notificación**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) de la línea de comandos en lugar de la devolución de llamada, pase el identificador del trabajo al archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="46944-117">If you use [**command line notification**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) instead of the callback, pass the job identifier to the executable file.</span></span> <span data-ttu-id="46944-118">El archivo ejecutable utiliza el identificador de trabajo para llamar al método **Complete** para que el archivo de respuesta esté disponible.</span><span class="sxs-lookup"><span data-stu-id="46944-118">The executable file uses the job identifier to call the **Complete** method to make the reply file available.</span></span>

<span data-ttu-id="46944-119">En los siguientes ejemplos se muestra cómo utilizar cada método para recuperar los datos de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46944-119">The following examples show how to use each method to retrieve the reply data.</span></span>

-   [<span data-ttu-id="46944-120">Usar GetReplyData</span><span class="sxs-lookup"><span data-stu-id="46944-120">Using GetReplyData</span></span>](#using-getreplydata)
-   [<span data-ttu-id="46944-121">Usar GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="46944-121">Using GetReplyFileName</span></span>](#using-getreplyfilename)

## <a name="using-getreplydata"></a><span data-ttu-id="46944-122">Usar GetReplyData</span><span class="sxs-lookup"><span data-stu-id="46944-122">Using GetReplyData</span></span>

<span data-ttu-id="46944-123">En el ejemplo siguiente se muestra cómo recuperar los datos de respuesta mediante el método [**IBackgroundCopyJob2:: GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) .</span><span class="sxs-lookup"><span data-stu-id="46944-123">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) method.</span></span> <span data-ttu-id="46944-124">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido, el tipo del trabajo es upload-Response y el estado del trabajo es transferencia de estado del trabajo de BG \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="46944-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of the job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



## <a name="using-getreplyfilename"></a><span data-ttu-id="46944-125">Usar GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="46944-125">Using GetReplyFileName</span></span>

<span data-ttu-id="46944-126">En el ejemplo siguiente se muestra cómo recuperar los datos de respuesta mediante el método [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) .</span><span class="sxs-lookup"><span data-stu-id="46944-126">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method.</span></span> <span data-ttu-id="46944-127">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido, el tipo de trabajo es upload-Response y el estado del trabajo es transferencia de estado del trabajo de BG \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="46944-127">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



 

 




