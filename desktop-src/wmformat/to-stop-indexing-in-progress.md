---
title: Para detener la indización en curso
description: Para detener la indización en curso
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- SDK de Windows Media Format, detener la indexación en curso
- Advanced Systems Format (ASF), detener la indexación en curso
- ASF (formato de sistemas avanzados), detener la indexación en curso
- índices, detener la indexación en curso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077338"
---
# <a name="to-stop-indexing-in-progress"></a><span data-ttu-id="4a930-107">Para detener la indización en curso</span><span class="sxs-lookup"><span data-stu-id="4a930-107">To Stop Indexing in Progress</span></span>

<span data-ttu-id="4a930-108">Después de comenzar la indexación con una llamada a [**IWMIndexer:: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), el indizador continuará normalmente hasta que se indexe el archivo.</span><span class="sxs-lookup"><span data-stu-id="4a930-108">After you begin indexing with a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), the indexer will normally continue until the file is indexed.</span></span> <span data-ttu-id="4a930-109">Puede detener las operaciones de indización mediante una llamada al método [**IWMIndexer:: CANCEL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) .</span><span class="sxs-lookup"><span data-stu-id="4a930-109">You can stop indexing operations by calling the [**IWMIndexer::Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) method.</span></span> <span data-ttu-id="4a930-110">Una vez cancelada la indexación, puede volver a llamar a **StartIndexing** , pero el indexador comenzará desde el principio del archivo en lugar de reanudarse desde el punto de cancelación.</span><span class="sxs-lookup"><span data-stu-id="4a930-110">After you have canceled indexing, you can call **StartIndexing** again, but the indexer will start from the beginning of the file rather than resuming from the point of cancellation.</span></span>

<span data-ttu-id="4a930-111">Dado que **StartIndexing** es una llamada asincrónica, normalmente necesitará llamar a **Cancel** desde otro subproceso o controlador de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4a930-111">Because **StartIndexing** is an asynchronous call, you will normally need to call **Cancel** from some other thread or event handler in your application.</span></span> <span data-ttu-id="4a930-112">Normalmente se llama a **Cancel** desde un procedimiento de evento asociado a un control de botón de una aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="4a930-112">Typically **Cancel** will be called from an event procedure associated with a button control of a Windows application.</span></span>

<span data-ttu-id="4a930-113">Cuando se cancela la indexación, el indexador pasará un mensaje de estado de WMT \_ cerrado, como si el archivo se hubiera indizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4a930-113">When indexing is canceled, the indexer will pass a status message of WMT\_CLOSED, just as if the file had been indexed properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a930-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a930-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a930-115">**Interfaz IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="4a930-115">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="4a930-116">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="4a930-116">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




