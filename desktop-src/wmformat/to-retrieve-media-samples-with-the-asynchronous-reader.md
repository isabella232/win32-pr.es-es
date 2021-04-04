---
title: Para recuperar ejemplos de medios con el lector asincrónico
description: Para recuperar ejemplos de medios con el lector asincrónico
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Advanced Systems Format (ASF), recuperar ejemplos de medios
- ASF (formato de sistemas avanzados), recuperar ejemplos de medios
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, recuperar ejemplos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077301"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a><span data-ttu-id="248db-108">Para recuperar ejemplos de medios con el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="248db-108">To Retrieve Media Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="248db-109">Después de recibir el mensaje de \_ estado abierto de WMT en la implementación de [**IWMStatusCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)en el estado, puede empezar a recibir ejemplos llamando a [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span><span class="sxs-lookup"><span data-stu-id="248db-109">After you have received the WMT\_OPENED status message in your implementation of [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), you can begin receiving samples by calling [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span></span> <span data-ttu-id="248db-110">El lector asincrónico proporciona ejemplos a su implementación de [**IWMReaderCallback:: websample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="248db-110">The asynchronous reader delivers samples to your implementation of [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="248db-111">Los ejemplos se entregan en el orden de presentación.</span><span class="sxs-lookup"><span data-stu-id="248db-111">Samples are delivered in presentation-time order.</span></span>

<span data-ttu-id="248db-112">**Start** es una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="248db-112">**Start** is an asynchronous call.</span></span> <span data-ttu-id="248db-113">Se devolverá casi inmediatamente y continuará ejecutándose en subprocesos independientes.</span><span class="sxs-lookup"><span data-stu-id="248db-113">It will return almost immediately and continue to run on separate threads.</span></span> <span data-ttu-id="248db-114">El lector asincrónico usa varios subprocesos al descodificar el contenido y entregar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="248db-114">The asynchronous reader uses multiple threads when decoding content and delivering samples.</span></span> <span data-ttu-id="248db-115">Cuando se alcanza el final del archivo, el lector envía un mensaje de \_ Estado de EOF de WMT a su implementación de la devolución de llamada de **Estado** .</span><span class="sxs-lookup"><span data-stu-id="248db-115">When the end of the file is reached, the reader sends a WMT\_EOF status message to your implementation of the **OnStatus** callback.</span></span> <span data-ttu-id="248db-116">Cuando \_ se envía el EOF para WMT, el lector detiene su propio procesamiento; no es necesario responder al \_ EOF de WMT con una llamada a [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span><span class="sxs-lookup"><span data-stu-id="248db-116">When WMT\_EOF is sent, the reader stops its own processing; you do not need to respond to WMT\_EOF with a call to [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span></span>

## <a name="related-topics"></a><span data-ttu-id="248db-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="248db-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="248db-118">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="248db-118">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="248db-119">**Para implementar mensajes de lector en la devolución de llamada de estado**</span><span class="sxs-lookup"><span data-stu-id="248db-119">**To Implement Reader Messages in the OnStatus Callback**</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[<span data-ttu-id="248db-120">**Para implementar la devolución de llamada de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="248db-120">**To Implement the OnSample Callback**</span></span>](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




