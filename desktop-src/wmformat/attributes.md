---
title: Atributos (Windows Media Format SDK 11)
description: Obtenga información sobre los atributos del SDK Windows Media Format 11. Un atributo es un elemento individual de metadatos.
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK,attributes
- Formato de sistemas avanzados (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- attributes,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262197"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="ce1e0-108">Atributos (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="ce1e0-108">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="ce1e0-109">Un atributo es un elemento individual de metadatos.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-109">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="ce1e0-110">La aplicación puede establecer la mayoría de los atributos y se escriben en el encabezado de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-110">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="ce1e0-111">Algunos de los atributos predefinidos son atributos codificados.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-111">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="ce1e0-112">Estos atributos no se almacenan en el encabezado de un archivo ASF, sino que los calculan los objetos del SDK de Windows Media Format cuando se carga el archivo.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-112">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="ce1e0-113">Dado que los atributos codificados siempre se calculan, son inherentemente de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-113">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="ce1e0-114">Este SDK incluye muchas definiciones de atributos que puede usar.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-114">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="ce1e0-115">También puede crear atributos propios para describir el contenido.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-115">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="ce1e0-116">En las secciones siguientes se describen los atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-116">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="ce1e0-117">Sección</span><span class="sxs-lookup"><span data-stu-id="ce1e0-117">Section</span></span>                                                                | <span data-ttu-id="ce1e0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce1e0-118">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce1e0-119">Lista de atributos</span><span class="sxs-lookup"><span data-stu-id="ce1e0-119">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="ce1e0-120">Proporciona una lista alfabética de todos los atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-120">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="ce1e0-121">Después de la lista, cada atributo se describe individualmente.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-121">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="ce1e0-122">Atributos con varios valores</span><span class="sxs-lookup"><span data-stu-id="ce1e0-122">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="ce1e0-123">Enumera los atributos que se pueden agregar a un archivo más de una vez.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-123">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="ce1e0-124">Atributos por tipo</span><span class="sxs-lookup"><span data-stu-id="ce1e0-124">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="ce1e0-125">Contiene listas de atributos ordenados por tipo.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-125">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="ce1e0-126">Estas incluyen listas de atributos de propósito especial (como los que tratan con la administración de derechos digitales) y listas de atributos sugeridos por tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-126">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="ce1e0-127">Compatibilidad con etiquetas ID3</span><span class="sxs-lookup"><span data-stu-id="ce1e0-127">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="ce1e0-128">Enumera los atributos que son compatibles con las etiquetas ID3.</span><span class="sxs-lookup"><span data-stu-id="ce1e0-128">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ce1e0-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce1e0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce1e0-130">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="ce1e0-130">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="ce1e0-131">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="ce1e0-131">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="ce1e0-132">**IWMHeaderInfo::SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="ce1e0-132">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="ce1e0-133">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="ce1e0-133">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




