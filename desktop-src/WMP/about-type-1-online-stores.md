---
title: Acerca de las tiendas en línea de tipo 1
description: Acerca de las tiendas en línea de tipo 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player tiendas en línea, escriba 1 tiendas en línea
- tiendas en línea, tipo 1 tiendas en línea
- tipo 1 tiendas en línea, acerca de
- Windows Media Player, escriba 1 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695556"
---
# <a name="about-type-1-online-stores"></a><span data-ttu-id="d3bb6-107">Acerca de las tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="d3bb6-107">About Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="d3bb6-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d3bb6-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d3bb6-110">Microsoft Windows Media Player 11 admite dos tipos de tiendas en línea: tipo 1 y tipo 2.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-110">Microsoft Windows Media Player 11 supports two kinds of online stores: type 1 and type 2.</span></span> <span data-ttu-id="d3bb6-111">Los almacenes de tipo 1 se integran más profundamente en Windows Media Player que los almacenes de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-111">Type 1 stores are more deeply integrated into Windows Media Player than type 2 stores.</span></span> <span data-ttu-id="d3bb6-112">Una tienda en línea de tipo 1 proporciona un catálogo de música descargable para que Windows Media Player pueda hacer que el contenido de la tienda esté disponible para el usuario como si estuviera en la biblioteca multimedia local del usuario.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-112">A type 1 online store provides a downloadable music catalog so that Windows Media Player can make the store's content available to the user as if the content were in the user's local media library.</span></span>

<span data-ttu-id="d3bb6-113">Una tienda en línea de tipo 1 debe proporcionar un complemento que implemente la interfaz [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="d3bb6-113">A type 1 online store must provide a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="d3bb6-114">Cuando el usuario navega en la interfaz de usuario de Windows Media Player, el reproductor llama al complemento para que la tienda en línea pueda mejorar la experiencia del usuario al proporcionar páginas web que se muestran en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-114">As the user navigates in the Windows Media Player user interface, the Player calls the plug-in so that the online store can enhance the user's experience by providing webpages that are displayed in the Player.</span></span>

<span data-ttu-id="d3bb6-115">Entre las características de las tiendas en línea de tipo 1 que las distinguen de los almacenes de tipo 2 se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3bb6-115">Features of type 1 online stores that distinguish them from type 2 stores include the following:</span></span>

-   <span data-ttu-id="d3bb6-116">**Facilidad de uso.**</span><span class="sxs-lookup"><span data-stu-id="d3bb6-116">**Ease of use.**</span></span> <span data-ttu-id="d3bb6-117">Los usuarios pueden buscar música desde el catálogo de la tienda en línea con la misma interfaz de usuario conocida de Windows Media Player que usan actualmente para administrar su biblioteca personal.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-117">Users can browse for music from the online store catalog using the same, familiar Windows Media Player user interface that they currently use to manage their personal library.</span></span> <span data-ttu-id="d3bb6-118">Los usuarios solo pueden ver un catálogo de la tienda en línea en la característica de exploración en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-118">Users can view only a single online store catalog in the Browse feature at any particular time.</span></span>
-   <span data-ttu-id="d3bb6-119">**Prácticos.**</span><span class="sxs-lookup"><span data-stu-id="d3bb6-119">**Convenience.**</span></span> <span data-ttu-id="d3bb6-120">Los usuarios pueden hacer un muestreo o comprar música sin cambiar de la característica de exploración a otra parte de la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-120">Users can sample or purchase music without switching from the Browse feature to another part of the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="d3bb6-121">**Características enriquecidas.**</span><span class="sxs-lookup"><span data-stu-id="d3bb6-121">**Rich features.**</span></span> <span data-ttu-id="d3bb6-122">Dado que el catálogo de la tienda en línea se almacena de manera similar a la biblioteca del usuario, muchas de las características de la biblioteca de Windows Media Player se pueden aplicar al catálogo.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-122">Because the online store catalog is stored in a fashion similar to the user's library, many of the Windows Media Player library features can be applied to the catalog.</span></span> <span data-ttu-id="d3bb6-123">Por ejemplo, los usuarios pueden usar la rueda de palabras de la característica examinar para filtrar el catálogo de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-123">For example, users can use the Browse feature's word wheel to filter the online store catalog.</span></span>

<span data-ttu-id="d3bb6-124">Para un proveedor de tienda en línea, las ventajas de proporcionar un almacén de tipo 1 en lugar de un almacén de tipo 2 incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d3bb6-124">For an online store provider, the advantages of providing a type 1 store rather than a type 2 store include the following:</span></span>

-   <span data-ttu-id="d3bb6-125">Un nodo personalizado muy visible en el árbol de la biblioteca de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-125">A highly visible custom node in the Windows Media Player library tree.</span></span>
-   <span data-ttu-id="d3bb6-126">Un sistema diseñado para compras de música.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-126">A system designed for music purchases.</span></span>
-   <span data-ttu-id="d3bb6-127">Conexiones mejoradas para los procesos del reproductor.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-127">Improved connections to Player processes.</span></span>
-   <span data-ttu-id="d3bb6-128">Un administrador de descargas mejor y más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-128">A better, easier-to-use download manager.</span></span>
-   <span data-ttu-id="d3bb6-129">La capacidad de navegar entre varias características del reproductor (incluida la apertura de nodos de árbol de biblioteca específicos).</span><span class="sxs-lookup"><span data-stu-id="d3bb6-129">The ability to navigate between various features in the Player (including opening specific library tree nodes).</span></span>
-   <span data-ttu-id="d3bb6-130">Notificaciones sobre la expiración de la licencia para el contenido de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-130">Notifications about license expiration for subscription content.</span></span>
-   <span data-ttu-id="d3bb6-131">Notificaciones para trabajar con reproductores de música portátiles conectados.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-131">Notifications for working with connected portable music players.</span></span>

<span data-ttu-id="d3bb6-132">En las secciones siguientes se proporciona información general sobre las tiendas en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-132">The following sections provide overview information about type 1 online stores.</span></span>



| <span data-ttu-id="d3bb6-133">Sección</span><span class="sxs-lookup"><span data-stu-id="d3bb6-133">Section</span></span>                                                                                              | <span data-ttu-id="d3bb6-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3bb6-134">Description</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3bb6-135">Catálogo de música</span><span class="sxs-lookup"><span data-stu-id="d3bb6-135">Music Catalog</span></span>](music-catalog.md)                                                                   | <span data-ttu-id="d3bb6-136">Describe el catálogo de música proporcionado por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-136">Describes the music catalog provided by the online store.</span></span> <span data-ttu-id="d3bb6-137">Describe el compilador de catálogo proporcionado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-137">Describes the catalog compiler provided by Microsoft.</span></span>                                                                     |
| [<span data-ttu-id="d3bb6-138">Contenedores de contenido</span><span class="sxs-lookup"><span data-stu-id="d3bb6-138">Content Containers</span></span>](content-containers.md)                                                         | <span data-ttu-id="d3bb6-139">Describe la interfaz de contenedor de contenido ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), que se usa para representar una colección de elementos multimedia que se van a comprar o descargar.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-139">Describes the content container interface ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), which is used to represent a collection of media items to be purchased or downloaded.</span></span> |
| [<span data-ttu-id="d3bb6-140">Integración de biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3bb6-140">Library Integration</span></span>](library-integration.md)                                                       | <span data-ttu-id="d3bb6-141">Describe cómo se integra el catálogo de música de la tienda en línea en la vista biblioteca del reproductor.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-141">Describes how the online store's music catalog is integrated into the Player's library view.</span></span>                                                                                        |
| [<span data-ttu-id="d3bb6-142">Páginas de detección</span><span class="sxs-lookup"><span data-stu-id="d3bb6-142">Discovery Pages</span></span>](discovery-pages.md)                                                               | <span data-ttu-id="d3bb6-143">Describe la interacción entre Windows Media Player y las páginas web proporcionadas por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-143">Describes the interaction between Windows Media Player and webpages provided by the online store.</span></span>                                                                                   |
| [<span data-ttu-id="d3bb6-144">Menús contextuales</span><span class="sxs-lookup"><span data-stu-id="d3bb6-144">Context Menus</span></span>](context-menus.md)                                                                   | <span data-ttu-id="d3bb6-145">Describe cómo la tienda en línea puede proporcionar menús contextuales a medida que el usuario navega por la interfaz de usuario del reproductor.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-145">Describes how the online store can provide context menus as the user navigates the Player's user interface.</span></span>                                                                         |
| [<span data-ttu-id="d3bb6-146">Secuencias de audio</span><span class="sxs-lookup"><span data-stu-id="d3bb6-146">Audio Streams</span></span>](audio-streams.md)                                                                   | <span data-ttu-id="d3bb6-147">Describe cómo la tienda en línea proporciona Windows Media Player con la dirección URL para el contenido de audio de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-147">Describes how the online store provides Windows Media Player with the URL for streaming audio content.</span></span>                                                                              |
| [<span data-ttu-id="d3bb6-148">Documento ServiceInfo para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="d3bb6-148">ServiceInfo Document for a Type 1 Online Store</span></span>](serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="d3bb6-149">Describe el documento XML ServiceInfo proporcionado por un almacén en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-149">Describes the ServiceInfo XML document provided by a type 1 online store.</span></span>                                                                                                           |
| [<span data-ttu-id="d3bb6-150">Escriba 1 complemento de tienda en línea</span><span class="sxs-lookup"><span data-stu-id="d3bb6-150">Type 1 Online Store Plug-in</span></span>](type-1-online-store-plug-in.md)                                       | <span data-ttu-id="d3bb6-151">Describe el complemento que debe proporcionar un almacén en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-151">Describes the plug-in that a type 1 online store must provide.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d3bb6-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3bb6-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3bb6-153">**Tipo 1 tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="d3bb6-153">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




