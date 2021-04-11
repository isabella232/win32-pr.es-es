---
description: El modo de dirección de textura de encapsulado, identificado por el \_ miembro D3DTADDRESS Wrap del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D repita la textura en cada unión de enteros.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Ajustar el modo de dirección de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274644"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a><span data-ttu-id="0cd24-103">Ajustar el modo de dirección de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cd24-103">Wrap Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="0cd24-104">El modo de dirección de textura de encapsulado, identificado por el \_ miembro D3DTADDRESS Wrap del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , hace que Direct3D repita la textura en cada unión de enteros.</span><span class="sxs-lookup"><span data-stu-id="0cd24-104">The wrap texture address mode, identified by the D3DTADDRESS\_WRAP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, makes Direct3D repeat the texture on every integer junction.</span></span> <span data-ttu-id="0cd24-105">Supongamos, por ejemplo, que la aplicación crea un primitivo cuadrado y especifica las coordenadas de textura de (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) y (3,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="0cd24-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="0cd24-106">Al establecer el modo de direccionamiento de textura en D3DTADDRESS \_ Wrap, la textura se aplica tres veces en las direcciones u-y v, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="0cd24-106">Setting the texture addressing mode to D3DTADDRESS\_WRAP results in the texture being applied three times in both the u-and v-directions, as shown in the following illustration.</span></span>

![Ilustración de una textura de caras ajustada en la dirección u y en la dirección de v](images/wrap.png)

<span data-ttu-id="0cd24-108">Los efectos de este modo de dirección de textura son similares a los del modo de reflejo.</span><span class="sxs-lookup"><span data-stu-id="0cd24-108">The effects of this texture address mode are similar to, but distinct from, those of the mirror mode.</span></span> <span data-ttu-id="0cd24-109">Para obtener más información, vea [modo de dirección de textura de reflejo (Direct3D 9)](mirror-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="0cd24-109">For more information, see [Mirror Texture Address Mode (Direct3D 9)](mirror-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cd24-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0cd24-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cd24-111">Modos de direccionamiento de textura</span><span class="sxs-lookup"><span data-stu-id="0cd24-111">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
