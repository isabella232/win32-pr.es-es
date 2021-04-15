---
description: El modo de dirección de textura reflejada, identificado por el \_ miembro reflejado D3DTADDRESS del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D refleje la textura en cada límite de entero.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modo de dirección de textura de reflejo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422856"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a><span data-ttu-id="e0dc5-103">Modo de dirección de textura de reflejo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e0dc5-103">Mirror Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="e0dc5-104">El modo de dirección de textura reflejada, identificado por el \_ miembro reflejado D3DTADDRESS del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , hace que Direct3D refleje la textura en cada límite de entero.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-104">The mirror texture address mode, identified by the D3DTADDRESS\_MIRROR member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to mirror the texture at every integer boundary.</span></span> <span data-ttu-id="e0dc5-105">Supongamos, por ejemplo, que la aplicación crea un primitivo cuadrado y especifica las coordenadas de textura de (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) y (3,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e0dc5-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="e0dc5-106">Al establecer el modo de direccionamiento de textura en el \_ reflejo de D3DTADDRESS, la textura se aplica tres veces en ambas direcciones u-y.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-106">Setting the texture addressing mode to D3DTADDRESS\_MIRROR results in the texture being applied three times in both the u- and v-directions.</span></span> <span data-ttu-id="e0dc5-107">Cada una de las demás filas y columnas a las que se aplica es una imagen reflejada de la fila o columna anterior, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-107">Every other row and column that it is applied to is a mirror image of the preceding row or column, as shown in the following illustration.</span></span>

![Ilustración de imágenes reflejadas en una cuadrícula de 3x3](images/mirror.png)

<span data-ttu-id="e0dc5-109">Los efectos de este modo de dirección de textura son similares a los del modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-109">The effects of this texture address mode are similar to, but distinct from, those of the wrap mode.</span></span> <span data-ttu-id="e0dc5-110">Para obtener más información, vea [ajustar el modo de dirección de textura (Direct3D 9)](wrap-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e0dc5-110">For more information, see [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0dc5-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0dc5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0dc5-112">Modos de direccionamiento de textura</span><span class="sxs-lookup"><span data-stu-id="e0dc5-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
