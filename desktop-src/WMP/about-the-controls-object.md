---
title: Acerca del objeto Controls
description: Acerca del objeto Controls
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Windows Media Player, Controls (objeto)
- Modelo de objetos de Windows Media Player, objetos Controls
- modelo de objetos, controles (objeto)
- Control ActiveX de Windows Media Player, controles (objeto)
- Control ActiveX, controles (objeto)
- Control ActiveX móvil de Windows Media Player, controles (objeto)
- Windows Media Player Mobile, objetos Controls
- Controls (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418382"
---
# <a name="about-the-controls-object"></a><span data-ttu-id="dc8b9-111">Acerca del objeto Controls</span><span class="sxs-lookup"><span data-stu-id="dc8b9-111">About the Controls Object</span></span>

<span data-ttu-id="dc8b9-112">El objeto **Controls** rige el transporte de contenido multimedia digital a través del control mediante métodos como **Play** y **Stop**.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-112">The **Controls** object governs the transport of digital media content through the control by using methods such as **Play** and **Stop**.</span></span> <span data-ttu-id="dc8b9-113">Solo se tiene acceso a ella a través de la propiedad **Controls** del objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="dc8b9-113">It is accessed only through the **Controls** property of the **Player** object.</span></span> <span data-ttu-id="dc8b9-114">La propiedad **Controls** devuelve el objeto **Controls** .</span><span class="sxs-lookup"><span data-stu-id="dc8b9-114">The **Controls** property returns the **Controls** object.</span></span> <span data-ttu-id="dc8b9-115">Solo se puede tener acceso a las propiedades del objeto **Controls** una vez creado.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-115">You can only access the properties of the **Controls** object after you have created it.</span></span> <span data-ttu-id="dc8b9-116">Por ejemplo, para usar el método **Play** , debe usar el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="dc8b9-116">For example, to use the **Play** method, you must use the following code:</span></span>


```C++
player.controls.play();

```



## <a name="related-topics"></a><span data-ttu-id="dc8b9-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc8b9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc8b9-118">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="dc8b9-118">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="dc8b9-119">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="dc8b9-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




