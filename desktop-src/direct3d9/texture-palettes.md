---
description: Direct3D 9 admite texturas con paletas a través de un conjunto de 256 paletas de entradas asociadas al objeto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Paletas de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705205"
---
# <a name="texture-palettes-direct3d-9"></a><span data-ttu-id="445ea-103">Paletas de texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="445ea-103">Texture Palettes (Direct3D 9)</span></span>

<span data-ttu-id="445ea-104">Direct3D 9 admite texturas con paletas a través de un conjunto de 256 paletas de entradas asociadas al objeto [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="445ea-104">Direct3D 9 supports paletted textures through a set of 256 entry palettes associated with the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) object.</span></span> <span data-ttu-id="445ea-105">Una paleta se convierte en actual llamando al método [**IDirect3DDevice9:: SetCurrentTexturePalette**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="445ea-105">A palette is made current by calling the [**IDirect3DDevice9::SetCurrentTexturePalette**](/windows/desktop/api) method.</span></span> <span data-ttu-id="445ea-106">La paleta actual se usa para traducir todas las texturas de paleta para todas las fases de textura activas.</span><span class="sxs-lookup"><span data-stu-id="445ea-106">The current palette is used for translating all paletted textures for all active texture stages.</span></span> <span data-ttu-id="445ea-107">[**IDirect3DDevice9:: SetPaletteEntries**](/windows/desktop/api) actualiza todas las entradas 256 de la paleta.</span><span class="sxs-lookup"><span data-stu-id="445ea-107">[**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) updates all of a palette's 256 entries.</span></span> <span data-ttu-id="445ea-108">Cada entrada es una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) con el formato D3DFMT \_ A8R8G8B8.</span><span class="sxs-lookup"><span data-stu-id="445ea-108">Each entry is a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure of the format D3DFMT\_A8R8G8B8.</span></span> <span data-ttu-id="445ea-109">De forma predeterminada, todas las entradas son 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="445ea-109">All entries default to 0xFFFFFFFF.</span></span>

<span data-ttu-id="445ea-110">Las paletas [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contienen un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="445ea-110">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) palettes contain an alpha channel.</span></span> <span data-ttu-id="445ea-111">Este canal alfa se puede usar cuando \_ se establece la marca de capacidad del dispositivo D3DPTEXTURECAPS ALPHAPALETTE, lo que indica que el dispositivo admite Alpha de la paleta.</span><span class="sxs-lookup"><span data-stu-id="445ea-111">This alpha channel can be used when the D3DPTEXTURECAPS\_ALPHAPALETTE device capability flag is set, indicating that the device supports alpha from the palette.</span></span> <span data-ttu-id="445ea-112">El canal alfa de la paleta se utiliza cuando el formato de la textura no tiene un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="445ea-112">The palette alpha channel is used when the texture format does not have an alpha channel.</span></span> <span data-ttu-id="445ea-113">Si el dispositivo no admite alfa de la paleta y el formato de textura no tiene un canal alfa, se usa un valor de 0xFF para alpha.</span><span class="sxs-lookup"><span data-stu-id="445ea-113">If the device does not support alpha from the palette and the texture format does not have an alpha channel, then a value of 0xFF is used for alpha.</span></span>

<span data-ttu-id="445ea-114">Hay un máximo de 65.536 (0x0000FFFF).</span><span class="sxs-lookup"><span data-stu-id="445ea-114">There is a maximum of 65,536 (0x0000FFFF) palettes.</span></span> <span data-ttu-id="445ea-115">Dado que los recursos de memoria asociados al conjunto de paletas son proporcionales al número de paleta máximo al que hace referencia una aplicación, use números de paleta contiguos a partir de cero.</span><span class="sxs-lookup"><span data-stu-id="445ea-115">Because memory resources associated with the set of palettes are proportional to the maximum palette number that an application references, use contiguous palette numbers starting at zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="445ea-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="445ea-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="445ea-117">Conceptos básicos de la texturización</span><span class="sxs-lookup"><span data-stu-id="445ea-117">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
