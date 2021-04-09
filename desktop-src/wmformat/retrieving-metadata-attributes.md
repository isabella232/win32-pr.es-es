---
title: Recuperación de atributos de metadatos
description: Recuperación de atributos de metadatos
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- SDK de Windows Media Format, recuperar atributos de metadatos
- Advanced Systems Format (ASF), recuperar atributos de metadatos
- ASF (formato de sistemas avanzados), recuperar atributos de metadatos
- metadatos, recuperar atributos
- flujos, recuperar atributos de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077280"
---
# <a name="retrieving-metadata-attributes"></a><span data-ttu-id="da7d2-108">Recuperación de atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="da7d2-108">Retrieving Metadata Attributes</span></span>

<span data-ttu-id="da7d2-109">Para recuperar un atributo de un encabezado de archivo, debe conocer el número de secuencia y el índice del atributo.</span><span class="sxs-lookup"><span data-stu-id="da7d2-109">To retrieve an attribute from a file header, you must know the stream number and index of the attribute.</span></span> <span data-ttu-id="da7d2-110">Puede usar el método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) para obtener los índices de todos los atributos con el mismo nombre o con todos los índices en el mismo idioma.</span><span class="sxs-lookup"><span data-stu-id="da7d2-110">You can use the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method to get the indexes for all attributes with the same name or all indexes in the same language.</span></span> <span data-ttu-id="da7d2-111">Al igual que los demás métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** trabaja con un solo flujo o con todos los atributos de nivel de archivo mediante la secuencia 0.</span><span class="sxs-lookup"><span data-stu-id="da7d2-111">Like the other methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** deals with a single stream, or with all file-level attributes using stream 0.</span></span> <span data-ttu-id="da7d2-112">Puede usar 0xFFFF para el número de secuencia con el fin de obtener índices globales que coincidan con los criterios en todo el archivo, independientemente del número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="da7d2-112">You can use 0xFFFF for the stream number to get global indexes matching your criteria throughout the entire file, regardless of stream number.</span></span>

<span data-ttu-id="da7d2-113">Cuando conozca el índice del atributo que desea recuperar, llame a [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) para obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="da7d2-113">When you know the index of the attribute you want to retrieve, call [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) to get the attribute.</span></span> <span data-ttu-id="da7d2-114">Debe realizar dos llamadas a **GetAttributeByIndexEx** para cada atributo recuperado.</span><span class="sxs-lookup"><span data-stu-id="da7d2-114">You need to make two calls to **GetAttributeByIndexEx** for each attribute retrieved.</span></span> <span data-ttu-id="da7d2-115">En la primera llamada, pase **null** para los punteros de nombre y de búfer de datos para obtener el tamaño necesario.</span><span class="sxs-lookup"><span data-stu-id="da7d2-115">On the first call, pass **NULL** for the name and data buffer pointers to get the size needed.</span></span> <span data-ttu-id="da7d2-116">A continuación, asigne los búferes del tamaño indicado y realice la segunda llamada para recuperar el nombre y los datos.</span><span class="sxs-lookup"><span data-stu-id="da7d2-116">Then allocate buffers of the size indicated and make the second call to retrieve the name and data.</span></span>

<span data-ttu-id="da7d2-117">Para obtener un ejemplo de código que muestra cómo recuperar los atributos de metadatos, vea [para recuperar todos los metadatos de un archivo](to-retrieve-all-metadata-in-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="da7d2-117">For example code showing how to retrieve metadata attributes, see [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="da7d2-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da7d2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da7d2-119">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="da7d2-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




