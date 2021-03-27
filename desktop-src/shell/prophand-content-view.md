---
description: En este tema se describe una nueva vista en el explorador de Windows, denominada vista de contenido, que muestra el contenido más relevante para cada elemento.
title: Vista de contenido por tipo de archivo o tipo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814838"
---
# <a name="content-view-by-file-type-or-kind"></a><span data-ttu-id="17930-103">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="17930-103">Content View By File Type or Kind</span></span>

<span data-ttu-id="17930-104">En este tema se describe una nueva vista en el explorador de Windows, denominada vista de contenido, que muestra el contenido más relevante para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="17930-104">This topic describes a new view in Windows Explorer, called the Content view, that displays the most relevant content for each item.</span></span> <span data-ttu-id="17930-105">Con un conjunto de claves del registro, los elementos pueden definir una lista de propiedades y un diseño que el shell utiliza para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="17930-105">Using a set of registry keys, items can define a property list and a layout that the Shell uses for Content view.</span></span> <span data-ttu-id="17930-106">El shell recupera las claves del registro mediante la [matriz de asociaciones](fa-perceivedtypes.md)del elemento.</span><span class="sxs-lookup"><span data-stu-id="17930-106">The Shell retrieves the registry keys by using the item's [association array](fa-perceivedtypes.md).</span></span>

## <a name="how-does-the-content-view-work"></a><span data-ttu-id="17930-107">¿Cómo funciona la vista de contenido?</span><span class="sxs-lookup"><span data-stu-id="17930-107">How Does the Content View Work?</span></span>

<span data-ttu-id="17930-108">En Windows 7 y versiones posteriores, la vista de contenido usa una lógica de cambio de tamaño que quita las propiedades cuando se reduce el tamaño de la ventana, para asegurarse de que las propiedades más críticas todavía tienen espacio para ser legibles claramente.</span><span class="sxs-lookup"><span data-stu-id="17930-108">In Windows 7 and later, the Content view uses a resizing logic that drops properties when the window size decreases, to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="17930-109">En la captura de pantalla siguiente se muestra la vista de contenido de los resultados de la búsqueda que contienen música, imágenes y documentos.</span><span class="sxs-lookup"><span data-stu-id="17930-109">The following screen shot illustrates the Content view of search results containing music, pictures, and documents.</span></span>

![vista de contenido de los resultados de la búsqueda que contienen música, imágenes y documentos](images/content-view/contentviewsearchresults.png)

<span data-ttu-id="17930-111">Algunos orígenes de datos de Shell usan la vista de contenido de forma predeterminada, pero los usuarios pueden seleccionar la vista de contenido haciendo clic en el botón **Ver control** en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="17930-111">Some Shell data sources use Content view by default, but users can select the Content view by clicking the **View Control** button in Windows Explorer.</span></span> <span data-ttu-id="17930-112">Un origen de datos de Shell extiende el espacio de nombres del shell y expone elementos en un almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="17930-112">A Shell data source extends the Shell namespace and exposes items in a data store.</span></span> <span data-ttu-id="17930-113">El sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="17930-113">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

## <a name="how-to-implement-the-content-view"></a><span data-ttu-id="17930-114">Cómo implementar la vista de contenido</span><span class="sxs-lookup"><span data-stu-id="17930-114">How to Implement the Content View</span></span>

<span data-ttu-id="17930-115">Al registrar un nuevo [tipo de archivo](fa-file-types.md) o [controlador de protocolo](../search/-search-3x-wds-extidx-prot-implementing.md), puede aprovechar la vista de contenido mediante uno de dos enfoques diferentes.</span><span class="sxs-lookup"><span data-stu-id="17930-115">When registering a new [file type](fa-file-types.md) or [protocol handler](../search/-search-3x-wds-extidx-prot-implementing.md), you can take advantage of the Content view by using either of two different approaches.</span></span> <span data-ttu-id="17930-116">Puede usar un conjunto de propiedades y un patrón de diseño existente, o puede crear su propia combinación.</span><span class="sxs-lookup"><span data-stu-id="17930-116">You can use an existing set of properties and layout pattern, or you can create your own combination.</span></span>

<span data-ttu-id="17930-117">Puede usar una entrada del registro para asociar el tipo de archivo o el elemento a [un tipo predefinido,](../properties/building-property-handlers-user-friendly-kind-names.md)que es una propiedad que se puede considerar como una categoría de contenido.</span><span class="sxs-lookup"><span data-stu-id="17930-117">You can use a registry entry to associate your file type or item with a predefined [Kind](../properties/building-property-handlers-user-friendly-kind-names.md), which is a property that you can think of as a content category.</span></span> <span data-ttu-id="17930-118">Al asociar el tipo de archivo o el elemento con algunos de estos tipos, se heredan automáticamente los patrones de diseño y las listas de propiedades de la vista de contenido de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="17930-118">By associating your file type or item with certain of these Kinds, you automatically inherit that Kind's Content view layout patterns and property lists.</span></span> <span data-ttu-id="17930-119">Windows define los patrones de diseño y las listas de propiedades de la vista de contenido para los siguientes tipos: documentos, correo electrónico, carpeta, música, imagen y genérico.</span><span class="sxs-lookup"><span data-stu-id="17930-119">Windows defines Content view layout patterns and property lists for the following Kinds: documents, email, folder, music, picture, and generic.</span></span> <span data-ttu-id="17930-120">Se recomienda este tipo de asociación.</span><span class="sxs-lookup"><span data-stu-id="17930-120">This type of association is encouraged.</span></span> <span data-ttu-id="17930-121">Permite proporcionar la experiencia coherente que un usuario espera para elementos similares.</span><span class="sxs-lookup"><span data-stu-id="17930-121">It lets you provide the consistent experience that a user expects for similar items.</span></span>

<span data-ttu-id="17930-122">Para obtener más información, vea [tipos de archivo](fa-file-types.md) y nombres de [tipo](../properties/building-property-handlers-user-friendly-kind-names.md) y [Cómo registrar un conjunto de vistas de contenido único de propiedades y patrones de diseño para el tipo de archivo o el elemento](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span><span class="sxs-lookup"><span data-stu-id="17930-122">For more information, see [File Types](fa-file-types.md) and [Kind Names](../properties/building-property-handlers-user-friendly-kind-names.md) and [How To Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17930-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="17930-123">Additional Resources</span></span>

-   <span data-ttu-id="17930-124">Para obtener documentación de referencia de propiedades, vea [System. Kind](../properties/props-system-kind.md)y [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="17930-124">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>
-   <span data-ttu-id="17930-125">Para obtener documentación de referencia de proplist, vea [System. proplist. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)y [System. proplist. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span><span class="sxs-lookup"><span data-stu-id="17930-125">For PropList reference documentation, see [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md), and [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="17930-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17930-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17930-127">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="17930-127">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="17930-128">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="17930-128">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="17930-129">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="17930-129">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="17930-130">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="17930-130">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="17930-131">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="17930-131">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="17930-132">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="17930-132">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="17930-133">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="17930-133">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="17930-134">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="17930-134">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
