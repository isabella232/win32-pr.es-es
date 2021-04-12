---
description: Las aplicaciones de Direct3D pueden lograr numerosos efectos especiales aplicando varias texturas a una primitiva en el transcurso de varias fases de representación.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Combinación de texturas de Multipass (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152320"
---
# <a name="multipass-texture-blending-direct3d-9"></a><span data-ttu-id="f30f3-103">Combinación de texturas de Multipass (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f30f3-103">Multipass Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="f30f3-104">Las aplicaciones de Direct3D pueden lograr numerosos efectos especiales aplicando varias texturas a una primitiva en el transcurso de varias fases de representación.</span><span class="sxs-lookup"><span data-stu-id="f30f3-104">Direct3D applications can achieve numerous special effects by applying various textures to a primitive over the course of multiple rendering passes.</span></span> <span data-ttu-id="f30f3-105">El término común para esto es Multipass Texture blending.</span><span class="sxs-lookup"><span data-stu-id="f30f3-105">The common term for this is multipass texture blending.</span></span> <span data-ttu-id="f30f3-106">Un uso típico de la combinación de texturas de Multipass es emular los efectos de los modelos de iluminación y sombreado complejos mediante la aplicación de varios colores de varias texturas diferentes.</span><span class="sxs-lookup"><span data-stu-id="f30f3-106">A typical use for multipass texture blending is to emulate the effects of complex lighting and shading models by applying multiple colors from several different textures.</span></span> <span data-ttu-id="f30f3-107">Una de estas aplicaciones se denomina asignación ligera.</span><span class="sxs-lookup"><span data-stu-id="f30f3-107">One such application is called light mapping.</span></span> <span data-ttu-id="f30f3-108">Para obtener más información, vea [asignación de luz con texturas (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="f30f3-108">For more information, see [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

> [!Note]  
> <span data-ttu-id="f30f3-109">Algunos dispositivos pueden aplicar varias texturas a primitivos en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="f30f3-109">Some devices are capable of applying multiple textures to primitives in a single pass.</span></span> <span data-ttu-id="f30f3-110">Para obtener más información, vea [combinación de texturas (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="f30f3-110">For details, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

 

<span data-ttu-id="f30f3-111">Si el hardware del usuario no admite varias combinaciones de texturas, la aplicación puede usar la combinación de texturas Multipass para lograr los mismos efectos visuales.</span><span class="sxs-lookup"><span data-stu-id="f30f3-111">If the user's hardware does not support multiple texture blending, your application can use multipass texture blending to achieve the same visual effects.</span></span> <span data-ttu-id="f30f3-112">Sin embargo, la aplicación no puede admitir las velocidades de fotogramas que son posibles cuando se usa la combinación de texturas múltiples.</span><span class="sxs-lookup"><span data-stu-id="f30f3-112">However, the application cannot sustain the frame rates that are possible when using multiple texture blending.</span></span>

<span data-ttu-id="f30f3-113">Para realizar la combinación de texturas de Multipass en una aplicación de C/C++.</span><span class="sxs-lookup"><span data-stu-id="f30f3-113">To perform multipass texture blending in a C/C++ application.</span></span>

1.  <span data-ttu-id="f30f3-114">Establezca una textura en la fase de textura 0 llamando al método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="f30f3-114">Set a texture in texture stage 0 by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span>
2.  <span data-ttu-id="f30f3-115">Seleccione el color deseado y los argumentos y las operaciones de combinación alfa con el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="f30f3-115">Select the desired color and alpha blending arguments and operations with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="f30f3-116">La configuración predeterminada es adecuada para la combinación de texturas de Multipass.</span><span class="sxs-lookup"><span data-stu-id="f30f3-116">The default settings are well-suited for multipass texture blending.</span></span>
3.  <span data-ttu-id="f30f3-117">Representar los objetos adecuados en la escena.</span><span class="sxs-lookup"><span data-stu-id="f30f3-117">Render the appropriate objects in the scene.</span></span>
4.  <span data-ttu-id="f30f3-118">Establezca la siguiente textura en la fase de textura 0.</span><span class="sxs-lookup"><span data-stu-id="f30f3-118">Set the next texture in texture stage 0.</span></span>
5.  <span data-ttu-id="f30f3-119">Establezca los \_ Estados de representación D3DRS SRCBLEND y D3DRS \_ DESTBLEND para ajustar los factores de mezcla de origen y destino según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f30f3-119">Set the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states to adjust the source and destination blending factors as needed.</span></span> <span data-ttu-id="f30f3-120">El sistema combina las nuevas texturas con los píxeles existentes en la superficie de representación-destino según estos parámetros.</span><span class="sxs-lookup"><span data-stu-id="f30f3-120">The system blends the new textures with the existing pixels in the render-target surface according to these parameters.</span></span>
6.  <span data-ttu-id="f30f3-121">Repita los pasos 3, 4 y 5 con tantas texturas como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f30f3-121">Repeat Steps 3, 4, and 5 with as many textures as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f30f3-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f30f3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f30f3-123">Combinación de texturas</span><span class="sxs-lookup"><span data-stu-id="f30f3-123">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
