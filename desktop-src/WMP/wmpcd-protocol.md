---
title: Protocolo WMPCD
description: Protocolo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolos
- Modelo de objetos de Windows Media Player, protocolos
- modelo de objetos, protocolos
- Control ActiveX de Windows Media Player, protocolos para el modelo de objetos
- Control ActiveX, protocolos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, protocolos para el modelo de objetos
- Windows Media Player Mobile, protocolos para el modelo de objetos
- protocolos, modelo de objetos de Windows Media Player
- protocolos, WMPCD
- Protocolo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268724"
---
# <a name="wmpcd-protocol"></a><span data-ttu-id="39a08-113">Protocolo WMPCD</span><span class="sxs-lookup"><span data-stu-id="39a08-113">WMPCD Protocol</span></span>

<span data-ttu-id="39a08-114">El protocolo WMPCD le permite especificar pistas en un disco compacto mediante la sintaxis de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="39a08-114">The WMPCD protocol enables you to specify tracks on a compact disc using URL syntax.</span></span> <span data-ttu-id="39a08-115">Esta es la sintaxis general del Protocolo:</span><span class="sxs-lookup"><span data-stu-id="39a08-115">This is the general syntax of the protocol:</span></span>


```C++
wmpcd://drive/track
```



<span data-ttu-id="39a08-116">El segmento de la *unidad* es el índice de la unidad de CD.</span><span class="sxs-lookup"><span data-stu-id="39a08-116">The *drive* segment is the index of the CD drive.</span></span> <span data-ttu-id="39a08-117">El segmento de *seguimiento* es el número de la pista. En el siguiente ejemplo se muestra el uso del protocolo WMPCD.</span><span class="sxs-lookup"><span data-stu-id="39a08-117">The *track* segment is the number of the track. The following example demonstrates using the WMPCD protocol.</span></span>


```C++
player.url = "wmpcd://0/4";
```



<span data-ttu-id="39a08-118">En el ejemplo se reproduce la cuarta pista del disco en la primera unidad de CD (la unidad cuyo índice es 0).</span><span class="sxs-lookup"><span data-stu-id="39a08-118">The example plays the fourth track on the disc in the first CD drive (the drive whose index is 0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="39a08-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39a08-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39a08-120">**Tipos de archivos y protocolos admitidos**</span><span class="sxs-lookup"><span data-stu-id="39a08-120">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




