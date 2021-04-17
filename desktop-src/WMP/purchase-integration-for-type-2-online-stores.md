---
title: Compra de la integración para las tiendas en línea de tipo 2
description: Compra de la integración para las tiendas en línea de tipo 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player tiendas en línea, integración de compras
- tiendas en línea, integración de compras
- tipo 2 tiendas en línea, integración de compras
- Windows Media Player tiendas en línea, integración de compras
- tiendas en línea, integración de compras
- tipo 2 tiendas en línea, integración de compras
- Windows Media Player, integración de compras
- Windows Media Player, integración de compras
- adquirir integración
- integración de compras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704719"
---
# <a name="purchase-integration-for-type-2-online-stores"></a><span data-ttu-id="fb388-113">Compra de la integración para las tiendas en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="fb388-113">Purchase Integration for Type 2 Online Stores</span></span>

<span data-ttu-id="fb388-114">Cuando Windows Media Player reproduce contenido multimedia digital o el usuario elige **Buscar información de álbum**, el reproductor ofrece al usuario un vínculo para comprar el CD o DVD desde el que se originó el contenido si dicho vínculo está disponible.</span><span class="sxs-lookup"><span data-stu-id="fb388-114">When Windows Media Player plays digital media content or the user chooses **Find Album Info**, the Player offers the user a link to buy the CD or DVD from which the content originated if such a link is available.</span></span> <span data-ttu-id="fb388-115">Cuando el usuario hace clic en el vínculo, Windows Media Player 10 o una versión posterior llama a en la tienda de música actual para controlar la solicitud de compra.</span><span class="sxs-lookup"><span data-stu-id="fb388-115">When the user clicks the link, Windows Media Player 10 or later calls on the current music store to handle the purchase request.</span></span> <span data-ttu-id="fb388-116">Cuando esto ocurre, el reproductor navega al primer panel de tareas de servicio (en Windows Media Player 10) o a la pestaña de tiendas en línea (en Windows Media Player 11) y muestra la Página Web especificada por el atributo **MediaPlayerURL** del elemento **BuyCD** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="fb388-116">When this happens, the Player navigates to the first service task pane (in Windows Media Player 10) or the Online Stores tab (in Windows Media Player 11) and displays the webpage specified by the **MediaPlayerURL** attribute of the **BuyCD** element of the ServiceInfo document.</span></span> <span data-ttu-id="fb388-117">(Los atributos **MediaCenterURL** y **BrowserURL** se usan de forma similar para controlar las llamadas de Windows xp Media Center Edition 2004 y Windows XP Service Pack 2).</span><span class="sxs-lookup"><span data-stu-id="fb388-117">(The **MediaCenterURL** and **BrowserURL** attributes are used in a similar manner to handle calls from Windows XP Media Center Edition 2004 and Windows XP Service Pack 2).</span></span>

<span data-ttu-id="fb388-118">Windows Media Player anexa una cadena de consulta a la dirección URL para proporcionar información a la tienda en línea sobre el contenido que el usuario decidió comprar.</span><span class="sxs-lookup"><span data-stu-id="fb388-118">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user chose to purchase.</span></span> <span data-ttu-id="fb388-119">La cadena de consulta incluye atributos como el **título**, el **álbum** y el **artista**, que la tienda en línea puede usar para determinar el álbum correcto que se va a vender.</span><span class="sxs-lookup"><span data-stu-id="fb388-119">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to sell.</span></span> <span data-ttu-id="fb388-120">La documentación de referencia para el elemento **BuyCD** proporciona la lista completa de atributos de cadena de consulta y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="fb388-120">The reference documentation for the **BuyCD** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-the-buycd-page"></a><span data-ttu-id="fb388-121">Instrucciones para la página BuyCD</span><span class="sxs-lookup"><span data-stu-id="fb388-121">Guidelines for the BuyCD Page</span></span>

<span data-ttu-id="fb388-122">Al crear la Página Web de BuyCD, use las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="fb388-122">When creating your BuyCD webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="fb388-123">La página debe identificar claramente la tienda en línea que proporciona la información.</span><span class="sxs-lookup"><span data-stu-id="fb388-123">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="fb388-124">Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fb388-124">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="fb388-125">La página debe incluir un vínculo a la declaración de privacidad de la empresa.</span><span class="sxs-lookup"><span data-stu-id="fb388-125">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="fb388-126">Es mejor proporcionar información de compra inicial sin necesidad de que el usuario instale programas o inicie sesión en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb388-126">It is best to provide initial purchasing information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb388-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb388-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb388-128">**Acerca de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="fb388-128">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fb388-129">**Elemento BuyCD**</span><span class="sxs-lookup"><span data-stu-id="fb388-129">**BuyCD Element**</span></span>](buycd-element.md)
</dt> </dl>

 

 




