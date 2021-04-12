---
title: Quitar atributos de metadatos
description: Quitar atributos de metadatos
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- SDK de Windows Media Format, quitar atributos de metadatos
- Advanced Systems Format (ASF), quitar atributos de metadatos
- ASF (formato de sistemas avanzados), quitar atributos de metadatos
- metadatos, quitar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420445"
---
# <a name="removing-metadata-attributes"></a><span data-ttu-id="d7291-107">Quitar atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="d7291-107">Removing Metadata Attributes</span></span>

<span data-ttu-id="d7291-108">Puede quitar un atributo de metadatos pasando su índice y el número de secuencia al método [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) .</span><span class="sxs-lookup"><span data-stu-id="d7291-108">You can remove a metadata attribute by passing its index and stream number to the [**IWMHeaderInfo3::DeleteAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) method.</span></span> <span data-ttu-id="d7291-109">El orden en el que se indexan los atributos restantes después de quitar un atributo no cambia; todos los atributos restantes que originalmente tenían un valor de índice mayor que el que se ha quitado tienen sus valores de índice reducidos en uno.</span><span class="sxs-lookup"><span data-stu-id="d7291-109">The order in which the remaining attributes are indexed after removing an attribute does not change; all remaining attributes that originally had an index value greater than the one removed have their index values reduced by one.</span></span> <span data-ttu-id="d7291-110">Al quitar varios atributos, hágalo en orden descendente por índice para evitar tener que calcular el ajuste en la indexación.</span><span class="sxs-lookup"><span data-stu-id="d7291-110">When removing multiple attributes, do so in descending order by index to avoid having to calculate the adjustment in indexing.</span></span>

<span data-ttu-id="d7291-111">Para mayor comodidad en la eliminación de valores, el método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) devuelve los valores de índice en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="d7291-111">For convenience in removing values, the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method returns the index values in descending order.</span></span>

> [!Note]  
> <span data-ttu-id="d7291-112">Los valores de índice obtenidos mediante el uso de los métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) no son compatibles con los valores de índice obtenidos mediante los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="d7291-112">Index values obtained by using the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) are not compatible with index values obtained by using the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span> <span data-ttu-id="d7291-113">Si usa los métodos de una interfaz para cambiar los atributos de un archivo, debe suponer que los valores de índice recuperados previamente de la otra interfaz ya no son válidos y se deben obtener de nuevo.</span><span class="sxs-lookup"><span data-stu-id="d7291-113">If you use the methods of one interface to change attributes in a file, you should assume that any index values previously retrieved from the other interface are no longer valid and must be obtained again.</span></span> <span data-ttu-id="d7291-114">Debe evitar el uso de los métodos de **IWMHeaderInfo** si es posible.</span><span class="sxs-lookup"><span data-stu-id="d7291-114">You should avoid using the methods of **IWMHeaderInfo** if possible.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d7291-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7291-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7291-116">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="d7291-116">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




