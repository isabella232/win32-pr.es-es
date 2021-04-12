---
title: Navegar a otras tiendas en línea
description: Navegar a otras tiendas en línea
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player tiendas en línea, navegar
- tiendas en línea, navegar
- Escriba 2 tiendas en línea, navegación
- navegar por las tiendas en línea de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356676"
---
# <a name="navigating-to-other-online-stores"></a><span data-ttu-id="20d65-107">Navegar a otras tiendas en línea</span><span class="sxs-lookup"><span data-stu-id="20d65-107">Navigating to Other Online Stores</span></span>

<span data-ttu-id="20d65-108">Puede crear vínculos a otras tiendas en línea que posea o entre vínculos cruzados de tiendas en línea proporcionadas por otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="20d65-108">You can create links to other online stores you own or cross-link to online stores provided by others.</span></span> <span data-ttu-id="20d65-109">Para ello, debe conocer el nombre de la clave de la tienda en línea a la que desea desplazarse.</span><span class="sxs-lookup"><span data-stu-id="20d65-109">To do this, you need to know the key name for the online store to which you want to navigate.</span></span>

<span data-ttu-id="20d65-110">En el ejemplo de código siguiente se muestra HTML que crea un vínculo para cambiar de la tienda en línea de Proseware a la característica "ServiceTask2" de la tienda Southridge video online:</span><span class="sxs-lookup"><span data-stu-id="20d65-110">The following example code shows HTML that creates a link to switch from the Proseware online store to the "ServiceTask2" feature of the Southridge Video online store:</span></span>


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



<span data-ttu-id="20d65-111">Cuando el usuario hace clic en el vínculo, Windows Media Player solicita al usuario que cambie al almacén de vídeo Southridge.</span><span class="sxs-lookup"><span data-stu-id="20d65-111">When the user clicks the link, Windows Media Player prompts the user to switch to the Southridge Video store.</span></span> <span data-ttu-id="20d65-112">Si el usuario lo permite, el reproductor cambia los almacenes y navega al panel de tareas especificado, anexando los parámetros de la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="20d65-112">If the user permits it, the Player then switches stores and navigates to the specified task pane, appending the query string parameters.</span></span> <span data-ttu-id="20d65-113">Los parámetros de cadena de consulta que se muestran en el ejemplo anterior son parámetros personalizados.</span><span class="sxs-lookup"><span data-stu-id="20d65-113">The query string parameters shown in the preceding example are custom parameters.</span></span> <span data-ttu-id="20d65-114">Esto significa que la tienda en línea que cambia a debe esperar estos valores y controlarlos.</span><span class="sxs-lookup"><span data-stu-id="20d65-114">This means that the online store you switch to must expect these values and handle them.</span></span> <span data-ttu-id="20d65-115">La tienda en línea (y cualquier tienda a la que cambie) puede usar los parámetros de cadena de consulta de la forma que elija.</span><span class="sxs-lookup"><span data-stu-id="20d65-115">Your online store (and any store you switch to) can use query string parameters any way you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20d65-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20d65-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20d65-117">**Desplazarse entre los paneles de tareas de servicio**</span><span class="sxs-lookup"><span data-stu-id="20d65-117">**Navigating between Service Task Panes**</span></span>](navigating-between-service-task-panes.md)
</dt> <dt>

[<span data-ttu-id="20d65-118">**Navegación para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="20d65-118">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




