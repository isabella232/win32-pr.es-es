---
title: Objeto del editor de metadatos
description: Objeto del editor de metadatos
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- SDK de Windows Media Format, objetos de editor de metadatos
- Advanced Systems Format (ASF), objetos de editor de metadatos
- ASF (formato de sistemas avanzados), objetos de editor de metadatos
- objetos, objetos de editor de metadatos
- objetos de editor de metadatos, acerca de
- metadatos, objetos de editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789220"
---
# <a name="metadata-editor-object"></a><span data-ttu-id="fde60-109">Objeto del editor de metadatos</span><span class="sxs-lookup"><span data-stu-id="fde60-109">Metadata Editor Object</span></span>

<span data-ttu-id="fde60-110">El objeto editor de metadatos se usa para editar la información almacenada en la sección de encabezado de los archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="fde60-110">The metadata editor object is used to edit information stored in the header section of ASF files.</span></span> <span data-ttu-id="fde60-111">Los elementos más comunes manipulados por este objeto son atributos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="fde60-111">The most common things manipulated by this object are metadata attributes.</span></span> <span data-ttu-id="fde60-112">Además, el editor de metadatos trata los [*marcadores*](wmformat-glossary.md) y los comandos de script.</span><span class="sxs-lookup"><span data-stu-id="fde60-112">Additionally, the metadata editor deals with [*markers*](wmformat-glossary.md) and script commands.</span></span> <span data-ttu-id="fde60-113">La única vez que necesita usar el editor de metadatos es cuando desea editar el encabezado de un archivo existente sin reproducirlo.</span><span class="sxs-lookup"><span data-stu-id="fde60-113">The only time you need to use the metadata editor is when you want to edit the header of an existing file without playing it.</span></span>

<span data-ttu-id="fde60-114">La función [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)crea el objeto de editor de metadatos, que establece un puntero a una interfaz **IWMMetadataEditor** .</span><span class="sxs-lookup"><span data-stu-id="fde60-114">The metadata editor object is created by the function [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), which sets a pointer to an **IWMMetadataEditor** interface.</span></span> <span data-ttu-id="fde60-115">Las demás interfaces del objeto de editor de metadatos se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="fde60-115">The other interfaces of the metadata editor object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="fde60-116">El objeto del editor de metadatos admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="fde60-116">The following interfaces are supported by the metadata editor object.</span></span>



| <span data-ttu-id="fde60-117">Interfaz</span><span class="sxs-lookup"><span data-stu-id="fde60-117">Interface</span></span>                                        | <span data-ttu-id="fde60-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fde60-118">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fde60-119">**IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="fde60-119">**IWMDRMEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | <span data-ttu-id="fde60-120">Permite que las aplicaciones de edición examinen las propiedades [*DRM*](wmformat-glossary.md) de un archivo ASF sin tener ningún derecho para reproducir el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="fde60-120">Enables editing applications to examine the [*DRM*](wmformat-glossary.md) properties of an ASF file without having any rights to play the protected content.</span></span> |
| [<span data-ttu-id="fde60-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="fde60-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="fde60-122">Manipula atributos, marcadores y comandos de script en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="fde60-122">Manipulates attributes, markers, and script commands in the header.</span></span>                                                                                                                                    |
| [<span data-ttu-id="fde60-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="fde60-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | <span data-ttu-id="fde60-124">Recupera información del códec.</span><span class="sxs-lookup"><span data-stu-id="fde60-124">Retrieves codec information.</span></span> <span data-ttu-id="fde60-125">Hereda todos los métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="fde60-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                                                         |
| [<span data-ttu-id="fde60-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="fde60-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | <span data-ttu-id="fde60-127">Proporciona compatibilidad avanzada con atributos, incluidos atributos grandes, varios lenguajes y nombres de atributos duplicados.</span><span class="sxs-lookup"><span data-stu-id="fde60-127">Provides advanced support for attributes, including large attributes, multiple languages, and duplicate attribute names.</span></span> <span data-ttu-id="fde60-128">Hereda todos los métodos de **IWMHeaderInfo** y **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="fde60-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>      |
| [<span data-ttu-id="fde60-129">**IWMMetadataEditor**</span><span class="sxs-lookup"><span data-stu-id="fde60-129">**IWMMetadataEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | <span data-ttu-id="fde60-130">Abre, cierra y guarda los cambios realizados en el encabezado de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="fde60-130">Opens, closes, and saves changes to the header of an ASF file.</span></span>                                                                                                                                         |
| [<span data-ttu-id="fde60-131">**IWMMetadataEditor2**</span><span class="sxs-lookup"><span data-stu-id="fde60-131">**IWMMetadataEditor2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | <span data-ttu-id="fde60-132">Abre un archivo ASF para la edición de encabezados con varias opciones de acceso y uso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="fde60-132">Opens an ASF file for header editing with multiple file access and sharing options.</span></span> <span data-ttu-id="fde60-133">Hereda todos los métodos de **IWMMetadataEditor**.</span><span class="sxs-lookup"><span data-stu-id="fde60-133">Inherits all of the methods of **IWMMetadataEditor**.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="fde60-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fde60-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fde60-135">**Marcadores**</span><span class="sxs-lookup"><span data-stu-id="fde60-135">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="fde60-136">**Repositorio**</span><span class="sxs-lookup"><span data-stu-id="fde60-136">**Metadata**</span></span>](metadata.md)
</dt> <dt>

[<span data-ttu-id="fde60-137">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="fde60-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="fde60-138">**Comandos de script**</span><span class="sxs-lookup"><span data-stu-id="fde60-138">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="fde60-139">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="fde60-139">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




