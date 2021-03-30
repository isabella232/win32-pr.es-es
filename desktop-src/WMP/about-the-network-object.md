---
title: Acerca del objeto de red
description: Acerca del objeto de red
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Media Player de Windows, objeto de red
- Modelo de objetos de Windows Media Player, objeto de red
- modelo de objetos, objeto de red
- Control ActiveX de Windows Media Player, objeto de red
- Control ActiveX, objeto de red
- Control ActiveX móvil de Windows Media Player, objeto de red
- Windows Media Player Mobile, objeto de red
- Objeto de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773338"
---
# <a name="about-the-network-object"></a><span data-ttu-id="9c2f1-111">Acerca del objeto de red</span><span class="sxs-lookup"><span data-stu-id="9c2f1-111">About the Network Object</span></span>

<span data-ttu-id="9c2f1-112">El objeto de **red** rige las propiedades que le permiten determinar la forma en que el contenido se transmite por secuencias a través de la red.</span><span class="sxs-lookup"><span data-stu-id="9c2f1-112">The **Network** object governs the properties that allow you to determine how well the content is streaming through the network.</span></span> <span data-ttu-id="9c2f1-113">Por ejemplo, puede averiguar si los paquetes se están perdido y tomar las medidas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="9c2f1-113">For example, you can find out whether packets are being lost and take appropriate action.</span></span> <span data-ttu-id="9c2f1-114">Solo se tiene acceso al objeto de **red** a través de la propiedad **Network** del objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="9c2f1-114">The **Network** object is accessed only through the **network** property of the **Player** object.</span></span> <span data-ttu-id="9c2f1-115">La propiedad de **red** devuelve el objeto de **red** .</span><span class="sxs-lookup"><span data-stu-id="9c2f1-115">The **network** property returns the **Network** object.</span></span> <span data-ttu-id="9c2f1-116">Solo puede acceder a las propiedades del objeto de **red** una vez creado.</span><span class="sxs-lookup"><span data-stu-id="9c2f1-116">You can only access the properties of the **Network** object after you have created it.</span></span> <span data-ttu-id="9c2f1-117">Por ejemplo, para utilizar la propiedad **ancho de banda** , debe usar el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c2f1-117">For example, to use the **Bandwidth** property, you must use the following code:</span></span>


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a><span data-ttu-id="9c2f1-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c2f1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c2f1-119">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="9c2f1-119">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="9c2f1-120">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="9c2f1-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




