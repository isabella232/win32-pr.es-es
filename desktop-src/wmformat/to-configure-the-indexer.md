---
title: Para configurar el indexador
description: Para configurar el indexador
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- SDK de Windows Media Format, configurar indexadores
- Advanced Systems Format (ASF), configurar indexadores
- ASF (formato de sistemas avanzados), configurar indexadores
- índices, configurar indexadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420295"
---
# <a name="to-configure-the-indexer"></a><span data-ttu-id="39587-107">Para configurar el indexador</span><span class="sxs-lookup"><span data-stu-id="39587-107">To Configure the Indexer</span></span>

<span data-ttu-id="39587-108">Puede configurar el indexador antes de usarlo para indizar un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="39587-108">You can configure the indexer before using it to index an ASF file.</span></span> <span data-ttu-id="39587-109">Cada secuencia del archivo puede configurarse por separado, o bien puede establecer la misma configuración para todos los flujos.</span><span class="sxs-lookup"><span data-stu-id="39587-109">Each stream in the file can be configured separately, or you can set the same configuration for all streams.</span></span>

<span data-ttu-id="39587-110">Si está configurando varias transmisiones para la indexación en un archivo, debe configurarlas todas y, a continuación, comenzar la indexación.</span><span class="sxs-lookup"><span data-stu-id="39587-110">If you are configuring multiple steams for indexing in a file, you must configure them all and then begin indexing.</span></span> <span data-ttu-id="39587-111">Si configura e indexa una secuencia y, a continuación, configura otra secuencia en el mismo archivo, si vuelve a iniciar el indexador, se eliminará el primer índice.</span><span class="sxs-lookup"><span data-stu-id="39587-111">If you configure and index a stream and then configure another stream in the same file, starting the indexer again will delete the first index.</span></span> <span data-ttu-id="39587-112">Esto es para cumplir con el formato de archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="39587-112">This is to comply with the ASF file format.</span></span>

<span data-ttu-id="39587-113">En el código siguiente se muestra cómo configurar el indizador.</span><span class="sxs-lookup"><span data-stu-id="39587-113">The following code shows how to configure the indexer.</span></span> <span data-ttu-id="39587-114">El código presupone que el archivo que se va a indexar tiene dos flujos: el primero es una secuencia de audio que no necesita indexarse y el segundo es una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="39587-114">The code assumes that the file to be indexed has two streams: the first is an audio stream which does not need to be indexed, and the second is a video stream.</span></span> <span data-ttu-id="39587-115">Este código solo muestra cómo configurar el indizador.</span><span class="sxs-lookup"><span data-stu-id="39587-115">This code shows only how to configure the indexer.</span></span> <span data-ttu-id="39587-116">Para indexar un archivo, debe seguir los pasos que se describen en [para indizar un archivo ASF](to-index-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="39587-116">To index a file, you must follow the steps presented in [To Index an ASF File](to-index-an-asf-file.md).</span></span>


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> <span data-ttu-id="39587-117">El tipo de índice predeterminado es WMT es el \_ \_ \_ punto limpio más cercano \_ .</span><span class="sxs-lookup"><span data-stu-id="39587-117">The default index type is WMT\_IT\_NEAREST\_CLEAN\_POINT.</span></span> <span data-ttu-id="39587-118">Aunque puede establecer el tipo de índice en otros valores, al hacerlo se reducirá el rendimiento de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="39587-118">Although you can set the index type to other values, doing so will degrade seeking performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="39587-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39587-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39587-120">**IWMIndexer2:: configure**</span><span class="sxs-lookup"><span data-stu-id="39587-120">**IWMIndexer2::Configure**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[<span data-ttu-id="39587-121">**Para indexar un archivo ASF**</span><span class="sxs-lookup"><span data-stu-id="39587-121">**To Index an ASF File**</span></span>](to-index-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="39587-122">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="39587-122">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="39587-123">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="39587-123">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




