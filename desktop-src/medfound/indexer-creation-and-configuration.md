---
description: En este tema se proporciona información sobre cómo crear el objeto indexador predeterminado proporcionado por Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Creación y configuración de indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277841"
---
# <a name="indexer-creation-and-configuration"></a><span data-ttu-id="13bda-103">Creación y configuración de indexador</span><span class="sxs-lookup"><span data-stu-id="13bda-103">Indexer Creation and Configuration</span></span>

<span data-ttu-id="13bda-104">El *indexador* ASF es un componente de nivel WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="13bda-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="13bda-105">En este tema se proporciona información sobre cómo crear el objeto indexador predeterminado proporcionado por Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="13bda-105">This topic provides information about creating the default indexer object provided by Media Foundation.</span></span>

<span data-ttu-id="13bda-106">Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="13bda-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="13bda-107">**Para crear e inicializar el indizador ASF**</span><span class="sxs-lookup"><span data-stu-id="13bda-107">**To create and initialize the ASF indexer**</span></span>

1.  <span data-ttu-id="13bda-108">Llame a la función [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para recibir un puntero [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) al objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="13bda-108">Call the [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) function to receive an [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) pointer to the indexer object.</span></span>
2.  <span data-ttu-id="13bda-109">Llame a [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) para especificar el modo de lectura o escritura para el objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="13bda-109">Call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) to specify the read or write mode for indexer object.</span></span> <span data-ttu-id="13bda-110">De forma predeterminada, el indexador está configurado para búsquedas hacia delante.</span><span class="sxs-lookup"><span data-stu-id="13bda-110">By default, the indexer is configured for forward seeking.</span></span>

    

    | <span data-ttu-id="13bda-111">Use</span><span class="sxs-lookup"><span data-stu-id="13bda-111">Use</span></span>                       | <span data-ttu-id="13bda-112">Marca</span><span class="sxs-lookup"><span data-stu-id="13bda-112">Flag</span></span>                                           |
    |---------------------------|------------------------------------------------|
    | <span data-ttu-id="13bda-113">Lectura (búsquedas hacia delante)</span><span class="sxs-lookup"><span data-stu-id="13bda-113">Reading (forward seeking)</span></span> | <span data-ttu-id="13bda-114">Cero (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="13bda-114">Zero (default)</span></span>                                 |
    | <span data-ttu-id="13bda-115">Lectura (búsqueda inversa)</span><span class="sxs-lookup"><span data-stu-id="13bda-115">Reading (reverse seeking)</span></span> | <span data-ttu-id="13bda-116">**\_indexador \_ de MFASF leído \_ para \_ REVERSEPLAYBACK**</span><span class="sxs-lookup"><span data-stu-id="13bda-116">**MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK**</span></span> |
    | <span data-ttu-id="13bda-117">Escritura</span><span class="sxs-lookup"><span data-stu-id="13bda-117">Writing</span></span>                   | <span data-ttu-id="13bda-118">Índice nuevo de MFASF de \_ escritura de indexador \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="13bda-118">MFASF\_INDEXER\_WRITE\_NEW\_INDEX</span></span>              |

    

     

    > [!Note]  
    > <span data-ttu-id="13bda-119">No se puede usar la misma instancia del indexador para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="13bda-119">The same instance of the indexer cannot be used for both reading and writing.</span></span> <span data-ttu-id="13bda-120">Debe configurar el indizador para uno u otro.</span><span class="sxs-lookup"><span data-stu-id="13bda-120">You must configure the indexer for one or the other.</span></span>

     

3.  <span data-ttu-id="13bda-121">Llame a [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar el indizador especificando el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del objeto ContentInfo que describe el archivo que se va a escribir o leer.</span><span class="sxs-lookup"><span data-stu-id="13bda-121">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer by specifying the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ContentInfo object that describes the file to be written or read.</span></span> <span data-ttu-id="13bda-122">El objeto ContentInfo contiene información que constituye el [objeto de encabezado ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="13bda-122">The ContentInfo object contains information that constitutes the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="13bda-123">El objeto de indexador requiere un objeto ContentInfo válido antes de generar o leer entradas de índice de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="13bda-123">The indexer object requires a valid ContentInfo object before generating or reading index entries of an ASF file.</span></span>

<span data-ttu-id="13bda-124">En el ejemplo de código siguiente se muestra cómo una aplicación puede crear e inicializar el objeto de indexador para trabajar con contenido ASF específico.</span><span class="sxs-lookup"><span data-stu-id="13bda-124">The following code example shows how an application can create and initialize the indexer object to work with specific ASF content.</span></span> <span data-ttu-id="13bda-125">El objeto ContentInfo representa el objeto de encabezado ASF; el contenido se pasa como un flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="13bda-125">The ContentInfo object represents the ASF Header Object; the content is passed as a byte stream.</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="13bda-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13bda-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13bda-127">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="13bda-127">ASF Indexer</span></span>](asf-index-object.md)
</dt> <dt>

[<span data-ttu-id="13bda-128">Uso del indexador para buscar en un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="13bda-128">Using the Indexer to Seek Within an ASF File</span></span>](using-the-indexer-to-seek.md)
</dt> <dt>

[<span data-ttu-id="13bda-129">Usar el indexador para escribir un nuevo índice</span><span class="sxs-lookup"><span data-stu-id="13bda-129">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



