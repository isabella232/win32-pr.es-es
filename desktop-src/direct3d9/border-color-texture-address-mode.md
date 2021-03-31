---
description: El modo de dirección de textura de color de borde, identificado por el \_ miembro de borde D3DTADDRESS del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D use un color arbitrario, conocido como color de borde, para las coordenadas de textura fuera del intervalo de 0,0 a 1,0, ambos incluidos.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Modo de dirección de textura de color de borde (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423435"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a><span data-ttu-id="bf9f8-103">Modo de dirección de textura de color de borde (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bf9f8-103">Border Color Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="bf9f8-104">El modo de dirección de textura de color de borde, identificado por el \_ miembro de borde D3DTADDRESS del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , hace que Direct3D use un color arbitrario, conocido como color de borde, para las coordenadas de textura fuera del intervalo de 0,0 a 1,0, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="bf9f8-104">The border color texture address mode, identified by the D3DTADDRESS\_BORDER member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to use an arbitrary color, known as the border color, for any texture coordinates outside the range of 0.0 through 1.0, inclusive.</span></span>

<span data-ttu-id="bf9f8-105">En la ilustración siguiente, la aplicación especifica que la textura se aplique a la primitiva mediante un borde rojo.</span><span class="sxs-lookup"><span data-stu-id="bf9f8-105">In the following illustration, the application specifies that the texture be applied to the primitive using a red border.</span></span>

![Ilustración de una textura y una textura con un borde rojo](images/border.png)

<span data-ttu-id="bf9f8-107">Las aplicaciones establecen el color del borde mediante una llamada a [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="bf9f8-107">Applications set the border color by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="bf9f8-108">Establezca el primer parámetro para la llamada al identificador de la fase de textura deseada, el segundo parámetro al valor de estado de la \_ fase D3DSAMP BORDERCOLOR y el tercer parámetro al nuevo color del borde RGBA.</span><span class="sxs-lookup"><span data-stu-id="bf9f8-108">Set the first parameter for the call to the desired texture stage identifier, the second parameter to the D3DSAMP\_BORDERCOLOR stage state value, and the third parameter to the new RGBA border color.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf9f8-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf9f8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9f8-110">Modos de direccionamiento de textura</span><span class="sxs-lookup"><span data-stu-id="bf9f8-110">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
