---
description: El comprobador de tipo de archivo es una herramienta que permite a los fabricantes de software independientes (ISV) comprobar que los tipos de archivo únicos se implementan correctamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Comprobador de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909566"
---
# <a name="file-type-verifier"></a><span data-ttu-id="f69f8-103">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f69f8-103">File Type Verifier</span></span>

<span data-ttu-id="f69f8-104">El comprobador de tipo de archivo es una herramienta que permite a los fabricantes de software independientes (ISV) comprobar que los tipos de archivo únicos se implementan correctamente.</span><span class="sxs-lookup"><span data-stu-id="f69f8-104">The File Type Verifier is a tool that enables independent software vendors (ISVs) to verify that their unique file types are implemented correctly.</span></span> <span data-ttu-id="f69f8-105">Las implementaciones de alta calidad de los controladores de tipo de archivo son cruciales para una buena experiencia del usuario, ya que los usuarios interactúan con el formato de archivo de muchas maneras en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="f69f8-105">High quality implementations of your file type handlers are crucial for a good user experience because users interact with your file format in many ways in Windows Explorer.</span></span> <span data-ttu-id="f69f8-106">Los usuarios pueden realizar búsquedas de texto completo, ordenar por metadatos personalizados o ver miniaturas enriquecidas y vistas previas del formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="f69f8-106">Users can do full-text searches, sort by custom metadata, or view rich thumbnails and previews of your file format.</span></span>

<span data-ttu-id="f69f8-107">Para obtener instrucciones sobre el uso del comprobador de tipo de archivo, consulte [Cómo usar el comprobador de tipo de archivo](how-to-use-the-file-type-verifier.md).</span><span class="sxs-lookup"><span data-stu-id="f69f8-107">For instructions on using the File Type Verifier, see [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).</span></span>

## <a name="about-the-file-type-verifier-tool"></a><span data-ttu-id="f69f8-108">Acerca de la herramienta Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f69f8-108">About the File Type Verifier Tool</span></span>

<span data-ttu-id="f69f8-109">Comprobador de tipo de archivo es un programa que está disponible como parte del [SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f69f8-109">File Type Verifier is a program that is available as part of the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f69f8-110">Está diseñado para ayudar a los desarrolladores que crean [tipos de archivo](fa-file-types.md) de Windows personalizados para detectar posibles problemas con sus tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f69f8-110">It is designed to help developers who create custom Windows [File Types](fa-file-types.md) to detect potential issues with their file types.</span></span> <span data-ttu-id="f69f8-111">Aunque el comprobador de tipo de archivo solo se ejecuta en Windows 7 y versiones posteriores, las reglas que el comprobador de tipo de archivo aplica a todas las versiones de Windows en las que están disponibles las características que comprueba.</span><span class="sxs-lookup"><span data-stu-id="f69f8-111">Although the File Type Verifier runs only on Windows 7 and later, the rules that the File Type Verifier enforces apply to all versions of Windows where the features it checks are available.</span></span>

<span data-ttu-id="f69f8-112">El comprobador de tipo de archivo ejecuta varias pruebas en el tipo de archivo para comprobar que se ha registrado correctamente, y que proporciona los [controladores de tipo de archivo](fa-file-extensions.md) adecuados para mostrar el tipo de archivo correctamente en el explorador de Windows y, cuando sea necesario, que admita la indización del contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="f69f8-112">The File Type Verifier runs several tests on the file type to verify that it is properly registered, and that it provides the appropriate [File Type Handlers](fa-file-extensions.md) to display the file type properly in Windows Explorer, and when appropriate, that it supports indexing the file content.</span></span>

<span data-ttu-id="f69f8-113">El comprobador de tipo de archivo prueba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f69f8-113">The File Type Verifier tests the following things:</span></span>

-   [<span data-ttu-id="f69f8-114">Controladores de vista previa</span><span class="sxs-lookup"><span data-stu-id="f69f8-114">Preview Handlers</span></span>](building-preview-handlers.md)
-   [<span data-ttu-id="f69f8-115">Controladores en miniatura</span><span class="sxs-lookup"><span data-stu-id="f69f8-115">Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
-   [<span data-ttu-id="f69f8-116">Controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="f69f8-116">Property Handlers</span></span>](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="f69f8-117">Controladores de verbos</span><span class="sxs-lookup"><span data-stu-id="f69f8-117">Verb Handlers</span></span>](fa-verbs.md)
-   [<span data-ttu-id="f69f8-118">Filtros (IFilter)</span><span class="sxs-lookup"><span data-stu-id="f69f8-118">Filters (IFilter)</span></span>](../search/-search-3x-wds-extidx-filters.md)
-   [<span data-ttu-id="f69f8-119">Asociaciones de tipo</span><span class="sxs-lookup"><span data-stu-id="f69f8-119">Kind Associations</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="f69f8-120">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="f69f8-120">Perceived Types</span></span>](fa-perceivedtypes.md)
-   [<span data-ttu-id="f69f8-121">Propiedades importantes</span><span class="sxs-lookup"><span data-stu-id="f69f8-121">Important Properties</span></span>](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a><span data-ttu-id="f69f8-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f69f8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f69f8-123">Cómo usar el comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f69f8-123">How To Use the File Type Verifier</span></span>](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="f69f8-124">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f69f8-124">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="f69f8-125">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="f69f8-125">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="f69f8-126">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="f69f8-126">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="f69f8-127">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="f69f8-127">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="f69f8-128">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f69f8-128">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="f69f8-129">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="f69f8-129">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="f69f8-130">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="f69f8-130">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="f69f8-131">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="f69f8-131">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
