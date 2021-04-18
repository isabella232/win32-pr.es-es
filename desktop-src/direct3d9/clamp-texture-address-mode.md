---
description: El modo de dirección de textura de abrazadera, identificado por el \_ miembro D3DTADDRESS clamp del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D Sujete las coordenadas de textura al \[ intervalo 0,0, 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Modo de dirección de textura de abrazadera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714878"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a><span data-ttu-id="0370f-103">Modo de dirección de textura de abrazadera (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0370f-103">Clamp Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="0370f-104">El modo de dirección de textura de abrazadera, identificado por el \_ miembro D3DTADDRESS clamp del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , hace que Direct3D Sujete las coordenadas de textura al \[ intervalo 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="0370f-104">The clamp texture address mode, identified by the D3DTADDRESS\_CLAMP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to clamp your texture coordinates to the \[0.0, 1.0\] range.</span></span> <span data-ttu-id="0370f-105">Es decir, aplica la textura una vez y después difumina el color de los píxeles del borde.</span><span class="sxs-lookup"><span data-stu-id="0370f-105">That is, it applies the texture once, then smears the color of edge pixels.</span></span> <span data-ttu-id="0370f-106">Por ejemplo, supongamos que la aplicación crea un primitivo cuadrado y asigna coordenadas de textura de (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) y (3,0, 0,0) a los vértices del primitivo.</span><span class="sxs-lookup"><span data-stu-id="0370f-106">For example, suppose that your application creates a square primitive and assigns texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0) to the primitive's vertices.</span></span> <span data-ttu-id="0370f-107">Al establecer el modo de direccionamiento de textura en D3DTADDRESS \_ Clamp, la textura se aplica una vez.</span><span class="sxs-lookup"><span data-stu-id="0370f-107">Setting the texture addressing mode to D3DTADDRESS\_CLAMP results in the texture being applied once.</span></span> <span data-ttu-id="0370f-108">Los colores de píxeles en la parte superior de las columnas y el final de las filas se extienden a la parte superior y derecha de la primitiva, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0370f-108">The pixel colors at the top of the columns and the end of the rows are extended to the top and right of the primitive respectively.</span></span>

<span data-ttu-id="0370f-109">En la ilustración siguiente se muestra una textura fija.</span><span class="sxs-lookup"><span data-stu-id="0370f-109">The following illustration shows a clamped texture.</span></span>

![Ilustración de una textura y una textura fija](images/clamp.png)

## <a name="related-topics"></a><span data-ttu-id="0370f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0370f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0370f-112">Modos de direccionamiento de textura</span><span class="sxs-lookup"><span data-stu-id="0370f-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
