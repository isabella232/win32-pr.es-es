---
title: Características de metadatos
description: Los metadatos se usan en archivos ASF para describir el contenido y las propiedades del archivo.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- SDK de Windows Media Format, características de metadatos
- Windows Media Format SDK, características
- Advanced Systems Format (ASF), características de metadatos
- ASF (formato de sistemas avanzados), características de metadatos
- Advanced Systems Format (ASF), características
- ASF (formato de sistemas avanzados), características
- metadatos, características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420451"
---
# <a name="metadata-features"></a><span data-ttu-id="83a25-110">Características de metadatos</span><span class="sxs-lookup"><span data-stu-id="83a25-110">Metadata Features</span></span>

<span data-ttu-id="83a25-111">Los metadatos se usan en archivos ASF para describir el contenido y las propiedades del archivo.</span><span class="sxs-lookup"><span data-stu-id="83a25-111">Metadata is used in ASF files to describe file contents and properties.</span></span> <span data-ttu-id="83a25-112">Todos los archivos ASF que cree deben incluir los metadatos adecuados.</span><span class="sxs-lookup"><span data-stu-id="83a25-112">All ASF files you create should include appropriate metadata.</span></span> <span data-ttu-id="83a25-113">(Para obtener información general, consulte [metadatos](metadata.md)). El SDK de Windows Media Format incluye compatibilidad con la edición de metadatos mediante el objeto de escritor, el objeto de editor de metadatos y los objetos de lector y lector sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="83a25-113">(For an overview, see [Metadata](metadata.md).) The Windows Media Format SDK includes support for metadata editing through the writer object, the metadata editor object, and both the reader and synchronous reader objects.</span></span> <span data-ttu-id="83a25-114">Se incluye compatibilidad nativa para una amplia variedad de atributos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="83a25-114">Native support for a wide variety of metadata attributes is included.</span></span> <span data-ttu-id="83a25-115">Vea [atributos](attributes.md) para obtener una lista de los atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="83a25-115">See [Attributes](attributes.md) for a list of the predefined attributes.</span></span>

<span data-ttu-id="83a25-116">La compatibilidad de metadatos proporcionada por los distintos objetos del SDK de Windows Media Format es flexible y eficaz.</span><span class="sxs-lookup"><span data-stu-id="83a25-116">The metadata support provided by the various objects of the Windows Media Format SDK is flexible and powerful.</span></span> <span data-ttu-id="83a25-117">Las principales características de los metadatos se resumen en la siguiente lista:</span><span class="sxs-lookup"><span data-stu-id="83a25-117">The main metadata features are summarized in the following list:</span></span>

-   <span data-ttu-id="83a25-118">Tamaño de atributo flexible.</span><span class="sxs-lookup"><span data-stu-id="83a25-118">Flexible attribute size.</span></span> <span data-ttu-id="83a25-119">Los atributos de metadatos no tienen un tamaño limitado.</span><span class="sxs-lookup"><span data-stu-id="83a25-119">Metadata attributes are not limited in size.</span></span>
-   <span data-ttu-id="83a25-120">Atributos de nivel de secuencia.</span><span class="sxs-lookup"><span data-stu-id="83a25-120">Stream-level attributes.</span></span> <span data-ttu-id="83a25-121">Los metadatos de los archivos ASF se pueden asignar al archivo en su totalidad o a una secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="83a25-121">Metadata in ASF files can be assigned to the file as a whole, or to a particular stream.</span></span>
-   <span data-ttu-id="83a25-122">Atributos duplicados.</span><span class="sxs-lookup"><span data-stu-id="83a25-122">Duplicated attributes.</span></span> <span data-ttu-id="83a25-123">Un atributo con nombre se puede usar varias veces en el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="83a25-123">A named attribute can be used multiple times in the same file.</span></span> <span data-ttu-id="83a25-124">Esta característica es de uso particular cuando se asignan atributos descriptivos de contenido.</span><span class="sxs-lookup"><span data-stu-id="83a25-124">This feature is of particular use when assigning content descriptive attributes.</span></span> <span data-ttu-id="83a25-125">Por ejemplo, una canción puede tener varios autores, cada uno de los cuales requiere un atributo **Author** independiente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="83a25-125">For example, a song may have several authors, each requiring a separate **Author** attribute in the file.</span></span>
-   <span data-ttu-id="83a25-126">Varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="83a25-126">Multiple languages.</span></span> <span data-ttu-id="83a25-127">Cada atributo tiene un idioma asociado.</span><span class="sxs-lookup"><span data-stu-id="83a25-127">Every attribute has a language associated with it.</span></span> <span data-ttu-id="83a25-128">Puede establecer los idiomas admitidos y, a continuación, asignar uno a cada atributo que escriba.</span><span class="sxs-lookup"><span data-stu-id="83a25-128">You can set the supported languages and then assign one to each attribute you write.</span></span> <span data-ttu-id="83a25-129">Dado que puede duplicar atributos, puede proporcionar los atributos más importantes en varios idiomas para llegar a un público más grande.</span><span class="sxs-lookup"><span data-stu-id="83a25-129">Because you can duplicate attributes, you can provide the most important attributes in several languages to reach a larger audience.</span></span> <span data-ttu-id="83a25-130">Si no especifica un idioma, se usará el idioma predeterminado (obtenido del sistema operativo del equipo que ejecuta la aplicación).</span><span class="sxs-lookup"><span data-stu-id="83a25-130">If you do not specify a language, the default language (obtained from the operating system of the computer running your application) will be used.</span></span>
-   <span data-ttu-id="83a25-131">Atributos complejos.</span><span class="sxs-lookup"><span data-stu-id="83a25-131">Complex attributes.</span></span> <span data-ttu-id="83a25-132">Algunos de los atributos predefinidos admiten datos estructurados.</span><span class="sxs-lookup"><span data-stu-id="83a25-132">Some of the predefined attributes support structured data.</span></span> <span data-ttu-id="83a25-133">Para estos atributos, el tipo de datos es binario, pero el valor es una estructura definida en este SDK.</span><span class="sxs-lookup"><span data-stu-id="83a25-133">For these attributes, the data type is binary, but the value is a structure defined in this SDK.</span></span>

<span data-ttu-id="83a25-134">En los temas siguientes se describen las demás características de metadatos admitidas.</span><span class="sxs-lookup"><span data-stu-id="83a25-134">The following topics discuss the other supported metadata features.</span></span>



| <span data-ttu-id="83a25-135">Tema</span><span class="sxs-lookup"><span data-stu-id="83a25-135">Topic</span></span>                                  | <span data-ttu-id="83a25-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="83a25-136">Description</span></span>                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="83a25-137">Compatibilidad con ID3</span><span class="sxs-lookup"><span data-stu-id="83a25-137">ID3 Support</span></span>](id3.md)                 | <span data-ttu-id="83a25-138">Describe la compatibilidad con tramas ID3 mediante los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="83a25-138">Discusses the support for ID3 frames using the objects of the Windows Media Format SDK.</span></span> |
| [<span data-ttu-id="83a25-139">Metadatos personalizados</span><span class="sxs-lookup"><span data-stu-id="83a25-139">Custom Metadata</span></span>](custom-metadata.md) | <span data-ttu-id="83a25-140">Describe las implicaciones del uso de metadatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="83a25-140">Discusses the implications of using custom metadata.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="83a25-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83a25-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83a25-142">**Características**</span><span class="sxs-lookup"><span data-stu-id="83a25-142">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="83a25-143">**Interfaz IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="83a25-143">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="83a25-144">**Interfaz IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="83a25-144">**IWMHeaderInfo2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[<span data-ttu-id="83a25-145">**Interfaz IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="83a25-145">**IWMHeaderInfo3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[<span data-ttu-id="83a25-146">**Metadatos**</span><span class="sxs-lookup"><span data-stu-id="83a25-146">**Metadata**</span></span>](metadata.md)
</dt> </dl>

 

 




