---
title: Integración de información de álbumes
description: Integración de información de álbumes
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player tiendas en línea, integración de información de álbumes
- tiendas en línea, integración de información de álbumes
- tipo 2 tiendas en línea, integración de información de álbumes
- Windows Media Player tiendas en línea, integración de información de álbumes
- tiendas en línea, integración de información de álbumes
- tipo 2 tiendas en línea, información de álbumes de integración
- Windows Media Player, integración de la información del álbum
- Windows Media Player, integración de información de álbumes
- integración de información de álbumes
- integración de la información del álbum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075641"
---
# <a name="album-info-integration"></a><span data-ttu-id="f6067-113">Integración de información de álbumes</span><span class="sxs-lookup"><span data-stu-id="f6067-113">Album Info Integration</span></span>

<span data-ttu-id="f6067-114">Windows Media Player permite a los usuarios solicitar información detallada sobre el CD o DVD desde el que se origina el contenido multimedia digital al hacer clic en un botón, como **más información**.</span><span class="sxs-lookup"><span data-stu-id="f6067-114">Windows Media Player enables users to request detailed information about the CD or DVD from which digital media content originated by clicking a button, such as **More Info**.</span></span> <span data-ttu-id="f6067-115">Cuando el usuario hace clic en el botón, Windows Media Player 10 o una versión posterior llama a en la tienda de música actual para mostrar los detalles del álbum.</span><span class="sxs-lookup"><span data-stu-id="f6067-115">When the user clicks the button, Windows Media Player 10 or later calls on the current music store to display the album details.</span></span> <span data-ttu-id="f6067-116">Cuando esto ocurre, el reproductor abre el panel de información del álbum y muestra la Página Web especificada por el atributo **URL** del elemento **AlbumInfo** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="f6067-116">When this happens, the Player opens the album information pane and displays the webpage specified by the **URL** attribute of the **AlbumInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="f6067-117">Windows Media Player anexa una cadena de consulta a la dirección URL para proporcionar información a la tienda en línea sobre el contenido solicitado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f6067-117">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user requested.</span></span> <span data-ttu-id="f6067-118">La cadena de consulta incluye atributos como el **título**, el **álbum** y el **artista**, que la tienda en línea puede usar para determinar el álbum correcto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="f6067-118">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to display.</span></span> <span data-ttu-id="f6067-119">La documentación de referencia para el elemento **AlbumInfo** proporciona la lista completa de atributos de cadena de consulta y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="f6067-119">The reference documentation for the **AlbumInfo** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-album-info"></a><span data-ttu-id="f6067-120">Directrices para la información del álbum</span><span class="sxs-lookup"><span data-stu-id="f6067-120">Guidelines for Album Info</span></span>

<span data-ttu-id="f6067-121">Al crear la Página Web de información del álbum, siga estas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="f6067-121">When creating your album information webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="f6067-122">La página debe identificar claramente la tienda en línea que proporciona la información.</span><span class="sxs-lookup"><span data-stu-id="f6067-122">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="f6067-123">Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f6067-123">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="f6067-124">La página debe incluir un vínculo a la declaración de privacidad de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f6067-124">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="f6067-125">Evite la navegación por la página dentro de la característica información del álbum siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="f6067-125">Avoid page navigation within the album information feature whenever possible.</span></span> <span data-ttu-id="f6067-126">Debe navegar a la tienda en línea para la mayoría de las actividades.</span><span class="sxs-lookup"><span data-stu-id="f6067-126">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="f6067-127">Le recomendamos que proporcione información valiosa sin necesidad de que el usuario instale programas o inicie sesión en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f6067-127">We recommend that you provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6067-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6067-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6067-129">**Acerca de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="f6067-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f6067-130">**Elemento AlbumInfo**</span><span class="sxs-lookup"><span data-stu-id="f6067-130">**AlbumInfo Element**</span></span>](albuminfo-element.md)
</dt> </dl>

 

 




