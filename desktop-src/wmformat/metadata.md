---
title: Metadatos
description: Los metadatos, para los fines de este SDK, son información que describe un archivo ASF o el contenido del archivo.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- SDK de Windows Media Format, información general sobre metadatos
- Advanced Systems Format (ASF), información general sobre metadatos
- ASF (formato de sistemas avanzados), información general sobre metadatos
- metadatos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357677"
---
# <a name="metadata"></a><span data-ttu-id="dad38-107">Metadatos</span><span class="sxs-lookup"><span data-stu-id="dad38-107">Metadata</span></span>

<span data-ttu-id="dad38-108">Los metadatos, para los fines de este SDK, son información que describe un archivo ASF o el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="dad38-108">Metadata, for the purposes of this SDK, is information that describes an ASF file or the contents of the file.</span></span> <span data-ttu-id="dad38-109">La sección de encabezado de un archivo ASF contiene todos los metadatos asociados a ese archivo.</span><span class="sxs-lookup"><span data-stu-id="dad38-109">The header section of an ASF file contains all of the metadata associated with that file.</span></span> <span data-ttu-id="dad38-110">Los elementos individuales de los metadatos de un archivo ASF se denominan atributos.</span><span class="sxs-lookup"><span data-stu-id="dad38-110">Individual items of metadata in an ASF file are called attributes.</span></span> <span data-ttu-id="dad38-111">Cada atributo tiene un nombre y un valor.</span><span class="sxs-lookup"><span data-stu-id="dad38-111">Each attribute has a name and a value.</span></span> <span data-ttu-id="dad38-112">A lo largo de esta documentación, se utilizan constantes globales para identificar atributos.</span><span class="sxs-lookup"><span data-stu-id="dad38-112">Throughout this documentation, global constants are used to identify attributes.</span></span> <span data-ttu-id="dad38-113">Por ejemplo, el título de un archivo ASF se almacena en el atributo **g \_ wszWMTitle** .</span><span class="sxs-lookup"><span data-stu-id="dad38-113">For example, the title of an ASF file is stored in the **g\_wszWMTitle** attribute.</span></span>

<span data-ttu-id="dad38-114">En el SDK de Windows Media Format se definen varios atributos para controlar las necesidades de metadatos más comunes.</span><span class="sxs-lookup"><span data-stu-id="dad38-114">A number of attributes are defined in the Windows Media Format SDK to handle the most common metadata needs.</span></span> <span data-ttu-id="dad38-115">Además, puede crear sus propios atributos.</span><span class="sxs-lookup"><span data-stu-id="dad38-115">In addition, you can create your own attributes.</span></span> <span data-ttu-id="dad38-116">Sin embargo, debe tener cuidado al asignar nombres a los atributos personalizados, ya que otros desarrolladores de aplicaciones pueden usar los mismos nombres y pueden producirse conflictos.</span><span class="sxs-lookup"><span data-stu-id="dad38-116">You should take care when naming custom attributes, however, because other application developers can use the same names, and conflicts can occur.</span></span>

<span data-ttu-id="dad38-117">Algunos atributos se establecen mediante el SDK y no se pueden cambiar manualmente.</span><span class="sxs-lookup"><span data-stu-id="dad38-117">Some attributes are set by the SDK and cannot be changed manually.</span></span> <span data-ttu-id="dad38-118">Por ejemplo, al indexar un archivo ASF, el SDK establece el atributo **g \_ wszWMSeekable** para mostrar que el archivo se puede leer ahora desde cualquier punto especificado.</span><span class="sxs-lookup"><span data-stu-id="dad38-118">For example, when you index an ASF file, the SDK sets the **g\_wszWMSeekable** attribute to show that the file can now be read from any specified point.</span></span>

<span data-ttu-id="dad38-119">Otros atributos son meramente informativos y deben establecerse manualmente.</span><span class="sxs-lookup"><span data-stu-id="dad38-119">Other attributes are purely informational and must be set manually.</span></span> <span data-ttu-id="dad38-120">Por ejemplo, si desea realizar un seguimiento del autor de un archivo, debe establecer **g \_ wszWMAuthor**.</span><span class="sxs-lookup"><span data-stu-id="dad38-120">For example, if you want to keep track of the author of a file, you should set **g\_wszWMAuthor**.</span></span>

<span data-ttu-id="dad38-121">El SDK de Windows Media Format proporciona compatibilidad con atributos que se aplican a todo el archivo y atributos que se aplican a flujos individuales.</span><span class="sxs-lookup"><span data-stu-id="dad38-121">The Windows Media Format SDK provides support for attributes that apply to the entire file, and attributes that apply to individual streams.</span></span>

<span data-ttu-id="dad38-122">Puede usar el SDK de Windows Media Format para editar los metadatos en archivos MP3, aunque siempre debe usar atributos compatibles con ID3 en archivos MP3 para mantener la compatibilidad con otros programas de manipulación de MP3.</span><span class="sxs-lookup"><span data-stu-id="dad38-122">You can use the Windows Media Format SDK to edit the metadata in MP3 files, though you should always use ID3-compliant attributes in MP3 files to maintain compatibility with other MP3 manipulation programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dad38-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dad38-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dad38-124">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="dad38-124">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="dad38-125">**Objeto del editor de metadatos**</span><span class="sxs-lookup"><span data-stu-id="dad38-125">**Metadata Editor Object**</span></span>](metadata-editor-object.md)
</dt> <dt>

[<span data-ttu-id="dad38-126">**Características de metadatos**</span><span class="sxs-lookup"><span data-stu-id="dad38-126">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="dad38-127">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="dad38-127">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




