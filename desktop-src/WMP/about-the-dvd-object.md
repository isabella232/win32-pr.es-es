---
title: Acerca del objeto de DVD
description: Acerca del objeto de DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Media Player de Windows, objeto de DVD
- Modelo de objetos de Windows Media Player, objeto de DVD
- modelo de objetos, objeto de DVD
- Control ActiveX de Windows Media Player, objeto de DVD
- Control ActiveX, objeto DVD
- Control ActiveX móvil de Windows Media Player, objeto de DVD
- Windows Media Player Mobile, objeto de DVD
- Objeto de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356734"
---
# <a name="about-the-dvd-object"></a><span data-ttu-id="362ba-111">Acerca del objeto de DVD</span><span class="sxs-lookup"><span data-stu-id="362ba-111">About the DVD Object</span></span>

<span data-ttu-id="362ba-112">El objeto de **DVD** agrega funcionalidad específica de los medios de DVD.</span><span class="sxs-lookup"><span data-stu-id="362ba-112">The **DVD** object adds functionality specific to DVD media.</span></span> <span data-ttu-id="362ba-113">En general, los medios de DVD se tratan igual que otros medios digitales de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="362ba-113">In a general sense, DVD media is treated just like other digital media in Windows Media Player.</span></span> <span data-ttu-id="362ba-114">Por ejemplo, las unidades de DVD se enumeran mediante el objeto **CdromCollection** y los títulos y capítulos de DVD se manipulan mediante objetos de **lista de reproducción** y objetos **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="362ba-114">For instance, DVD drives are enumerated using the **CdromCollection** object and DVD titles and chapters are manipulated using **Playlist** objects and **Media** objects.</span></span> <span data-ttu-id="362ba-115">Sin embargo, algunas funciones son específicas del DVD y el objeto de **DVD** lo proporciona.</span><span class="sxs-lookup"><span data-stu-id="362ba-115">Some functionality is DVD-specific, however, and the **DVD** object provides this.</span></span> <span data-ttu-id="362ba-116">Por ejemplo, DVD tiene un concepto denominado dominio.</span><span class="sxs-lookup"><span data-stu-id="362ba-116">For example, DVD has a concept called domain.</span></span> <span data-ttu-id="362ba-117">Para recuperar el dominio actual para los medios de DVD, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="362ba-117">To retrieve the current domain for DVD media, type the following:</span></span>


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a><span data-ttu-id="362ba-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="362ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="362ba-119">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="362ba-119">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="362ba-120">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="362ba-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




