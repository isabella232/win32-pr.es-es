---
title: Trabajar con metadatos
description: Trabajar con metadatos
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- SDK de Windows Media Format, información general sobre metadatos
- Advanced Systems Format (ASF), información general sobre metadatos
- ASF (formato de sistemas avanzados), información general sobre metadatos
- metadatos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420459"
---
# <a name="working-with-metadata"></a><span data-ttu-id="bf349-107">Trabajar con metadatos</span><span class="sxs-lookup"><span data-stu-id="bf349-107">Working with Metadata</span></span>

<span data-ttu-id="bf349-108">El objeto de escritor proporciona compatibilidad con metadatos, el lector y los objetos de lector sincrónicos, y el objeto de editor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="bf349-108">Metadata support is provided by the writer object, the reader and synchronous reader objects, and the metadata editor object.</span></span> <span data-ttu-id="bf349-109">Para obtener información general sobre los metadatos, vea [metadatos](metadata.md).</span><span class="sxs-lookup"><span data-stu-id="bf349-109">For general information about metadata, see [Metadata](metadata.md).</span></span> <span data-ttu-id="bf349-110">Para obtener información sobre las características que admiten metadatos en el SDK de Windows Media Format, vea [características de metadatos](metadata-features.md).</span><span class="sxs-lookup"><span data-stu-id="bf349-110">For information about the features supporting metadata in the Windows Media Format SDK, see [Metadata Features](metadata-features.md).</span></span>

<span data-ttu-id="bf349-111">La interfaz para la edición de metadatos es [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), que puede obtener llamando al método **QueryInterface** de cualquier interfaz en uno de los objetos enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bf349-111">The interface for metadata editing is [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), which you can obtain by calling the **QueryInterface** method of any interface in one of the objects listed above.</span></span> <span data-ttu-id="bf349-112">**IWMHeaderInfo3** hereda los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) y [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span><span class="sxs-lookup"><span data-stu-id="bf349-112">**IWMHeaderInfo3** inherits the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span></span> <span data-ttu-id="bf349-113">Los métodos de **IWMHeaderInfo3** que se ocupan de los atributos de metadatos representan un enfoque diferente para tener acceso a los metadatos de los que usan los métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="bf349-113">The methods of **IWMHeaderInfo3** that deal with metadata attributes represent a different approach to accessing metadata than that used by the methods of **IWMHeaderInfo**.</span></span> <span data-ttu-id="bf349-114">Siempre debe usar los métodos más recientes.</span><span class="sxs-lookup"><span data-stu-id="bf349-114">You should always use the newer methods.</span></span>

<span data-ttu-id="bf349-115">Los metadatos de un archivo ASF se identifican mediante un índice y un número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="bf349-115">Metadata in an ASF file is identified by an index and a stream number.</span></span> <span data-ttu-id="bf349-116">A los atributos de nivel de archivo se les asigna un número de secuencia de 0.</span><span class="sxs-lookup"><span data-stu-id="bf349-116">File-level attributes are assigned a stream number of 0.</span></span> <span data-ttu-id="bf349-117">En versiones anteriores del SDK de Windows Media Format, los atributos se pueden identificar por su nombre.</span><span class="sxs-lookup"><span data-stu-id="bf349-117">In previous versions of the Windows Media Format SDK, attributes could be identified by name.</span></span> <span data-ttu-id="bf349-118">Sin embargo, dado que ahora puede duplicar los nombres de atributo dentro de una secuencia, esto ya no es posible.</span><span class="sxs-lookup"><span data-stu-id="bf349-118">However, because you can now duplicate attribute names within a stream, this is no longer possible.</span></span> <span data-ttu-id="bf349-119">En su lugar, puede recuperar todos los índices que coinciden con un nombre.</span><span class="sxs-lookup"><span data-stu-id="bf349-119">Instead, you can retrieve all the indexes matching a name.</span></span> <span data-ttu-id="bf349-120">Para obtener más información, vea [recuperar atributos de metadatos](retrieving-metadata-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="bf349-120">For more information, see [Retrieving Metadata Attributes](retrieving-metadata-attributes.md).</span></span>

<span data-ttu-id="bf349-121">Para ayudar a encontrar los atributos rápidamente, puede usar un número de secuencia especial, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="bf349-121">To aid in finding attributes quickly, you can use a special stream number, 0xFFFF.</span></span> <span data-ttu-id="bf349-122">Use este número de secuencia para identificar el archivo como un todo, en lugar de una secuencia específica o los atributos de nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="bf349-122">Use this stream number to identify the file as a whole, rather than a specific stream or the file-level attributes.</span></span> <span data-ttu-id="bf349-123">Los objetos del SDK de Windows Media Format mantienen índices independientes para cada flujo y para los atributos de nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="bf349-123">The objects of the Windows Media Format SDK maintain separate indexes for each stream and for the file-level attributes.</span></span> <span data-ttu-id="bf349-124">Cuando se usa el flujo 0xFFFF, los índices son diferentes de los que se usan al especificar una secuencia específica.</span><span class="sxs-lookup"><span data-stu-id="bf349-124">When using stream 0xFFFF, the indexes are different from those you use when specifying a specific stream.</span></span> <span data-ttu-id="bf349-125">Por ejemplo, el atributo que es el índice 0 de la secuencia 0 no será el mismo que el atributo que es el índice 0 para el flujo 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="bf349-125">For example, the attribute that is index 0 for stream 0 will not be the same as the attribute that is index 0 for stream 0xFFFF.</span></span>

<span data-ttu-id="bf349-126">En las secciones siguientes se describe el uso de metadatos con mayor detalle.</span><span class="sxs-lookup"><span data-stu-id="bf349-126">The following sections describe the use of metadata in greater detail.</span></span>



| <span data-ttu-id="bf349-127">Sección</span><span class="sxs-lookup"><span data-stu-id="bf349-127">Section</span></span>                                                                    | <span data-ttu-id="bf349-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf349-128">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="bf349-129">Recuperación de atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="bf349-129">Retrieving Metadata Attributes</span></span>](retrieving-metadata-attributes.md)       | <span data-ttu-id="bf349-130">Describe cómo leer los atributos de metadatos de un encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="bf349-130">Describes how to read metadata attributes from a file header.</span></span>                     |
| [<span data-ttu-id="bf349-131">Establecer atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="bf349-131">Setting Metadata Attributes</span></span>](setting-metadata-attributes.md)             | <span data-ttu-id="bf349-132">Describe cómo agregar nuevos atributos de metadatos a un encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="bf349-132">Describes how to add new metadata attributes to a file header.</span></span>                    |
| [<span data-ttu-id="bf349-133">Editar atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="bf349-133">Editing Metadata Attributes</span></span>](editing-metadata-attributes.md)             | <span data-ttu-id="bf349-134">Describe cómo editar los atributos de metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="bf349-134">Describes how to edit existing metadata attributes.</span></span>                               |
| [<span data-ttu-id="bf349-135">Quitar atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="bf349-135">Removing Metadata Attributes</span></span>](removing-metadata-attributes.md)           | <span data-ttu-id="bf349-136">Describe cómo quitar atributos de metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="bf349-136">Describes how to remove existing metadata attributes.</span></span>                             |
| [<span data-ttu-id="bf349-137">Usar atributos de metadatos complejos</span><span class="sxs-lookup"><span data-stu-id="bf349-137">Using Complex Metadata Attributes</span></span>](using-complex-metadata-attributes.md) | <span data-ttu-id="bf349-138">Describe cómo trabajar con atributos cuyos valores se representan mediante estructuras.</span><span class="sxs-lookup"><span data-stu-id="bf349-138">Describes how to work with attributes whose values are represented by structures.</span></span> |



 

<span data-ttu-id="bf349-139">Algunas de las aplicaciones de ejemplo muestran cómo recuperar y editar metadatos.</span><span class="sxs-lookup"><span data-stu-id="bf349-139">Several of the sample applications show how to retrieve and edit metadata.</span></span> <span data-ttu-id="bf349-140">En concreto, vea el ejemplo MetadataEdit, que se incluye en las versiones de C++ y C#.</span><span class="sxs-lookup"><span data-stu-id="bf349-140">In particular, see the MetadataEdit sample, which comes in both C++ and C# versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf349-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf349-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf349-142">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="bf349-142">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="bf349-143">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="bf349-143">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="bf349-144">**Aplicaciones de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="bf349-144">**Sample Applications**</span></span>](sample-applications.md)
</dt> </dl>

 

 




