---
title: Atributos (Windows Media Format 11 SDK)
description: Atributos
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421827"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="31a97-107">Atributos (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="31a97-107">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="31a97-108">Un atributo es un elemento individual de metadatos.</span><span class="sxs-lookup"><span data-stu-id="31a97-108">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="31a97-109">La mayoría de los atributos se pueden establecer en la aplicación y se escriben en el encabezado de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="31a97-109">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="31a97-110">Algunos de los atributos predefinidos son atributos codificados.</span><span class="sxs-lookup"><span data-stu-id="31a97-110">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="31a97-111">Estos atributos no se almacenan en el encabezado de un archivo ASF, pero se calculan mediante los objetos del SDK de Windows Media Format cuando se carga el archivo.</span><span class="sxs-lookup"><span data-stu-id="31a97-111">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="31a97-112">Dado que los atributos codificados siempre se calculan, son intrínsecamente de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="31a97-112">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="31a97-113">Este SDK incluye muchas definiciones de atributos que puede usar.</span><span class="sxs-lookup"><span data-stu-id="31a97-113">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="31a97-114">También puede crear atributos propios para describir el contenido.</span><span class="sxs-lookup"><span data-stu-id="31a97-114">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="31a97-115">En las secciones siguientes se describen los atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="31a97-115">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="31a97-116">Sección</span><span class="sxs-lookup"><span data-stu-id="31a97-116">Section</span></span>                                                                | <span data-ttu-id="31a97-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="31a97-117">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31a97-118">Lista de atributos</span><span class="sxs-lookup"><span data-stu-id="31a97-118">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="31a97-119">Proporciona una lista alfabética de todos los atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="31a97-119">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="31a97-120">Después de la lista, cada atributo se describe individualmente.</span><span class="sxs-lookup"><span data-stu-id="31a97-120">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="31a97-121">Atributos con varios valores</span><span class="sxs-lookup"><span data-stu-id="31a97-121">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="31a97-122">Muestra los atributos que se pueden agregar más de una vez a un archivo.</span><span class="sxs-lookup"><span data-stu-id="31a97-122">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="31a97-123">Atributos por tipo</span><span class="sxs-lookup"><span data-stu-id="31a97-123">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="31a97-124">Contiene listas de atributos ordenados por tipo.</span><span class="sxs-lookup"><span data-stu-id="31a97-124">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="31a97-125">Estos incluyen listas de atributos especiales (como los que se ocupan de la administración de derechos digitales) y listas de atributos sugeridos por tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="31a97-125">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="31a97-126">Compatibilidad con etiquetas ID3</span><span class="sxs-lookup"><span data-stu-id="31a97-126">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="31a97-127">Muestra los atributos que son compatibles con las etiquetas ID3.</span><span class="sxs-lookup"><span data-stu-id="31a97-127">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="31a97-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31a97-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31a97-129">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="31a97-129">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="31a97-130">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="31a97-130">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="31a97-131">**IWMHeaderInfo:: SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="31a97-131">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="31a97-132">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="31a97-132">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




