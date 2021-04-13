---
title: Trabajar con el reproductor
description: Trabajar con el reproductor
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Máscaras de Windows Media Player, atributo Player en JScript
- máscaras, atributo Player en JScript
- atributos, reproductor
- atributo Player
- Archivos JScript para máscaras, atributo Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419150"
---
# <a name="working-with-the-player"></a><span data-ttu-id="c59ac-108">Trabajar con el reproductor</span><span class="sxs-lookup"><span data-stu-id="c59ac-108">Working with the Player</span></span>

<span data-ttu-id="c59ac-109">Al usar Microsoft JScript para tener acceso a los métodos y las propiedades de Windows Media Player, debe usar el nombre "Player" como nombre del control.</span><span class="sxs-lookup"><span data-stu-id="c59ac-109">When using Microsoft JScript to access methods and properties of Windows Media Player, you must use the name "player" for the name of the control.</span></span> <span data-ttu-id="c59ac-110">Por ejemplo, para hacer referencia al método STOP, debe escribir:</span><span class="sxs-lookup"><span data-stu-id="c59ac-110">For example, to reference the Stop method, you must type:</span></span>


```C++
player.Controls.Stop()

```



<span data-ttu-id="c59ac-111">El atributo global **Player** es la clave para tener acceso al control de Media Player de Windows a través de scripting de máscara.</span><span class="sxs-lookup"><span data-stu-id="c59ac-111">The **player** global attribute is the key to accessing the Windows Media Player control through skin scripting.</span></span> <span data-ttu-id="c59ac-112">A través de este atributo, se puede tener acceso a todos los objetos del control de Media Player de Windows para modificarlos en tiempo de ejecución a través de sus propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="c59ac-112">Through this attribute, all the objects of the Windows Media Player control become accessible for run-time modification through their properties and methods.</span></span> <span data-ttu-id="c59ac-113">Además, el elemento **Player** está disponible para que pueda especificar controladores de eventos y el atributo **URL** en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="c59ac-113">Additionally, the **PLAYER** element is available so that you can specify event handlers and the **url** attribute at design time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c59ac-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c59ac-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c59ac-115">**Usar JScript**</span><span class="sxs-lookup"><span data-stu-id="c59ac-115">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




