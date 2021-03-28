---
description: Un tipo percibido es una categoría de tipos de archivo que le permite identificar el tipo de archivo en Windows (y aplicaciones) como imagen, audio, documento u otro tipo.
title: Tipos percibidos (el shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998005"
---
# <a name="perceived-types-the-windows-shell"></a><span data-ttu-id="72205-103">Tipos percibidos (el shell de Windows)</span><span class="sxs-lookup"><span data-stu-id="72205-103">Perceived Types (The Windows Shell)</span></span>

<span data-ttu-id="72205-104">Un tipo percibido es una categoría de tipos de archivo que le permite identificar el tipo de archivo en Windows (y aplicaciones) como imagen, audio, documento u otro tipo.</span><span class="sxs-lookup"><span data-stu-id="72205-104">A perceived type is a category of file types that lets you identify your file type to Windows (and applications) as being an image, audio, document, or other type.</span></span> <span data-ttu-id="72205-105">Los tipos percibidos se usan para varios propósitos, incluida la determinación del tipo de carpeta, que se usa para establecer la configuración de vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="72205-105">Perceived types are used for several purposes, including the determination of the folder type, which is then used to set the default view settings.</span></span> <span data-ttu-id="72205-106">Por ejemplo, una carpeta llena de archivos de la imagen de tipo percibida tiene asignado un modo de vista predeterminada de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="72205-106">For example, a folder full of files that are of the perceived type image is assigned a default view mode of thumbnails.</span></span>

<span data-ttu-id="72205-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="72205-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="72205-108">Acerca de los tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="72205-108">About Perceived Types</span></span>](#about-perceived-types)
-   [<span data-ttu-id="72205-109">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="72205-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="72205-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72205-110">Related topics</span></span>](#related-topics)

## <a name="about-perceived-types"></a><span data-ttu-id="72205-111">Acerca de los tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="72205-111">About Perceived Types</span></span>

<span data-ttu-id="72205-112">Los tipos percibidos, definidos como valores PerceivedType, son similares a los tipos de archivo, salvo que hacen referencia a amplias categorías de tipos de formato de archivo en lugar de tipos de archivo específicos.</span><span class="sxs-lookup"><span data-stu-id="72205-112">Perceived types, defined as PerceivedType values, are similar to file types except that they refer to broad categories of file format types rather than specific file types.</span></span> <span data-ttu-id="72205-113">Por ejemplo, imágenes, texto, audio y comprimidos son tipos que se perciben.</span><span class="sxs-lookup"><span data-stu-id="72205-113">For example, image, text, audio, and compressed are perceived types.</span></span> <span data-ttu-id="72205-114">A los tipos de archivo (generalmente tipos de archivo públicos) se les puede asignar un tipo percibido y siempre se les debe asignar uno cada vez que haya uno que sea adecuado.</span><span class="sxs-lookup"><span data-stu-id="72205-114">File types (generally public file types) can be assigned a perceived type, and should always be assigned one whenever there is one that is appropriate.</span></span> <span data-ttu-id="72205-115">Por ejemplo, los tipos de archivo de imagen. bmp,. png,. jpg y. gif son también de tipo de imagen percibida.</span><span class="sxs-lookup"><span data-stu-id="72205-115">For example, the image file types .bmp, .png, .jpg, and .gif are also of perceived type image.</span></span>

<span data-ttu-id="72205-116">Los tipos percibidos predeterminados son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="72205-116">The default perceived types are as follows:</span></span>

-   <span data-ttu-id="72205-117">Carpeta</span><span class="sxs-lookup"><span data-stu-id="72205-117">Folder</span></span>
-   <span data-ttu-id="72205-118">Texto</span><span class="sxs-lookup"><span data-stu-id="72205-118">Text</span></span>
-   <span data-ttu-id="72205-119">Imagen</span><span class="sxs-lookup"><span data-stu-id="72205-119">Image</span></span>
-   <span data-ttu-id="72205-120">Audio</span><span class="sxs-lookup"><span data-stu-id="72205-120">Audio</span></span>
-   <span data-ttu-id="72205-121">Vídeo</span><span class="sxs-lookup"><span data-stu-id="72205-121">Video</span></span>
-   <span data-ttu-id="72205-122">Compressed</span><span class="sxs-lookup"><span data-stu-id="72205-122">Compressed</span></span>
-   <span data-ttu-id="72205-123">Documento</span><span class="sxs-lookup"><span data-stu-id="72205-123">Document</span></span>
-   <span data-ttu-id="72205-124">Sistema</span><span class="sxs-lookup"><span data-stu-id="72205-124">System</span></span>
-   <span data-ttu-id="72205-125">Application</span><span class="sxs-lookup"><span data-stu-id="72205-125">Application</span></span>
-   <span data-ttu-id="72205-126">Gamemedia</span><span class="sxs-lookup"><span data-stu-id="72205-126">Gamemedia</span></span>
-   <span data-ttu-id="72205-127">Contactos</span><span class="sxs-lookup"><span data-stu-id="72205-127">Contacts</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72205-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="72205-128">Additional Resources</span></span>

-   <span data-ttu-id="72205-129">Para obtener información sobre cómo registrar los tipos percibidos, consulte [registro de aplicaciones](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="72205-129">For information about how to register perceived types, see [Application Registration](app-registration.md).</span></span>
-   <span data-ttu-id="72205-130">Para obtener una lista de los tipos percibidos predeterminados, vea la enumeración [**percibida**](/windows/win32/api/shtypes/ne-shtypes-perceived) .</span><span class="sxs-lookup"><span data-stu-id="72205-130">For a list of default perceived types, see the [**PERCEIVED**](/windows/win32/api/shtypes/ne-shtypes-perceived) enumeration.</span></span>
-   <span data-ttu-id="72205-131">Para recuperar el tipo percibido de un archivo en función de su extensión de nombre de archivo, consulte la función [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .</span><span class="sxs-lookup"><span data-stu-id="72205-131">To retrieves a file's perceived type based on its file name extension, see the [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72205-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72205-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72205-133">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="72205-133">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="72205-134">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="72205-134">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="72205-135">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="72205-135">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="72205-136">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="72205-136">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="72205-137">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="72205-137">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="72205-138">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="72205-138">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="72205-139">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="72205-139">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="72205-140">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="72205-140">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



