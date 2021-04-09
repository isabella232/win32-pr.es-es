---
title: Catálogo de música
description: Catálogo de música
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player tiendas en línea, catálogos de música
- tiendas en línea, catálogos de música
- tipo 1 almacenes en línea, catálogos de música
- Windows Media Player tiendas en línea, compilador de catálogos
- tiendas en línea, compilador de catálogos
- tipo 1 almacenes en línea, compilador de catálogos
- catálogos de música
- compilador de catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077286"
---
# <a name="music-catalog"></a><span data-ttu-id="ad7b9-111">Catálogo de música</span><span class="sxs-lookup"><span data-stu-id="ad7b9-111">Music Catalog</span></span>

<span data-ttu-id="ad7b9-112">Un almacén en línea de tipo 1 crea su catálogo de música como un conjunto de archivos de valores separados por tabulaciones (TSV).</span><span class="sxs-lookup"><span data-stu-id="ad7b9-112">A type 1 online store creates its music catalog as a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="ad7b9-113">A continuación, la tienda en línea usa el [compilador de catálogo](catalog-compiler-for-type-1-online-stores.md) de Microsoft para compilar los archivos TSV en un catálogo comprimido que se puede descargar mediante Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-113">Then the online store uses Microsoft's [catalog compiler](catalog-compiler-for-type-1-online-stores.md) to compile the TSV files into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="ad7b9-114">Windows Media Player puede descargar archivos de catálogo completos o archivos de actualización de catálogo.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-114">Windows Media Player can download full catalog files or catalog update files.</span></span> <span data-ttu-id="ad7b9-115">Las actualizaciones del catálogo solo contienen la información del catálogo que ha cambiado desde la última actualización del catálogo.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-115">Catalog updates contain only the catalog information that has changed since the last catalog update.</span></span> <span data-ttu-id="ad7b9-116">Es el complemento de asociado de contenido el que determina si se debe descargar un catálogo completo o una actualización.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-116">It is up to the content partner plug-in to determine whether to download a full catalog or an update.</span></span> <span data-ttu-id="ad7b9-117">En cualquier caso, Windows Media Player aplica los cambios al catálogo actual después de la notificación del complemento.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-117">In either case, Windows Media Player applies the changes to the current catalog upon notification from the plug-in.</span></span>

<span data-ttu-id="ad7b9-118">Si la tienda en línea tiene un catálogo nuevo preparado, el complemento puede notificar al reproductor llamando a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) y pasando wmpcnNewCatalogAvailable como valor para el parámetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="ad7b9-118">If the online store has a new catalog prepared, the plug-in can notify the Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) and passing wmpcnNewCatalogAvailable as the value for the *type* parameter.</span></span>

<span data-ttu-id="ad7b9-119">Cuando Windows Media Player está listo para descargar un catálogo o una actualización, el reproductor llama a [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="ad7b9-119">When Windows Media Player is ready to download a catalog or update, the Player calls [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> <span data-ttu-id="ad7b9-120">Este método proporciona al complemento información sobre el catálogo actual, como la versión del catálogo y el identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-120">This method provides the plug-in with information about the current catalog, such as the catalog version and locale identifier.</span></span> <span data-ttu-id="ad7b9-121">El complemento responde proporcionando el localizador uniforme de recursos (URL) de la actualización o el catálogo completo correctos, así como un número de versión actualizado y una fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-121">The plug-in responds by supplying the uniform resource locator (URL) of the correct full catalog or update, as well as an updated version number and expiration date.</span></span> <span data-ttu-id="ad7b9-122">Windows Media Player solicitará periódicamente actualizaciones de catálogo basadas en la información proporcionada por el complemento en **GetCatalogURL**.</span><span class="sxs-lookup"><span data-stu-id="ad7b9-122">Windows Media Player will periodically request catalog updates based upon the information provided by the plug-in in **GetCatalogURL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad7b9-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad7b9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad7b9-124">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="ad7b9-124">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ad7b9-125">**Compilador de catálogo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="ad7b9-125">**Catalog Compiler for Type 1 Online Stores**</span></span>](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ad7b9-126">**Interfaz IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="ad7b9-126">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




