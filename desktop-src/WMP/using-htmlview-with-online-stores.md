---
title: Uso de HTMLView con tiendas en línea
description: Uso de HTMLView con tiendas en línea
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player tiendas en línea, HTMLView
- tiendas en línea, HTMLView
- Escriba 1 tiendas en línea, HTMLView
- tipo 2 tiendas en línea, HTMLView
- HTMLView, tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695466"
---
# <a name="using-htmlview-with-online-stores"></a><span data-ttu-id="aa323-108">Uso de HTMLView con tiendas en línea</span><span class="sxs-lookup"><span data-stu-id="aa323-108">Using HTMLView with Online Stores</span></span>

<span data-ttu-id="aa323-109">Windows Media Player solicita permiso a los usuarios para mostrar el contenido de HTMLView en **reproducción** en curso.</span><span class="sxs-lookup"><span data-stu-id="aa323-109">Windows Media Player prompts users for permission to display HTMLView content in **Now Playing**.</span></span> <span data-ttu-id="aa323-110">Las tiendas en línea pueden deshabilitar este símbolo del sistema especificando un valor de dirección URL base en el elemento **HTMLView** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="aa323-110">Online stores can disable this prompt by specifying a base URL value in the **HTMLView** element of the ServiceInfo document.</span></span> <span data-ttu-id="aa323-111">Cuando Windows Media Player abre una lista de reproducción que especifica el contenido de HTMLView que se va a mostrar, el reproductor compara la dirección URL base del documento ServiceInfo de la tienda en línea activa actual con la dirección URL base del contenido de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="aa323-111">When Windows Media Player opens a playlist that specifies HTMLView content to display, the Player compares the base URL from the ServiceInfo document of the current active online store to the base URL of the HTMLView content.</span></span> <span data-ttu-id="aa323-112">Si coinciden, Windows Media Player muestra el contenido de HTMLView sin preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="aa323-112">If they match, Windows Media Player displays the HTMLView content without prompting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa323-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa323-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa323-114">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="aa323-114">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="aa323-115">**Elemento HTMLView**</span><span class="sxs-lookup"><span data-stu-id="aa323-115">**HTMLView Element**</span></span>](htmlview-element.md)
</dt> <dt>

[<span data-ttu-id="aa323-116">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="aa323-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




