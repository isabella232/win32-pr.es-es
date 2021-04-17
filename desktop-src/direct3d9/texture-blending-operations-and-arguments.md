---
description: Las aplicaciones asocian una fase de combinación con cada textura del conjunto de texturas actuales. Direct3D evalúa cada fase de combinación en orden, comenzando por la primera textura del conjunto y terminando por el octavo.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operaciones y argumentos de combinación de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714741"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a><span data-ttu-id="59807-104">Operaciones y argumentos de combinación de texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="59807-104">Texture Blending Operations and Arguments (Direct3D 9)</span></span>

<span data-ttu-id="59807-105">Las aplicaciones asocian una fase de combinación con cada textura del conjunto de texturas actuales.</span><span class="sxs-lookup"><span data-stu-id="59807-105">Applications associate a blending stage with each texture in the set of current textures.</span></span> <span data-ttu-id="59807-106">Direct3D evalúa cada fase de combinación en orden, comenzando por la primera textura del conjunto y terminando por el octavo.</span><span class="sxs-lookup"><span data-stu-id="59807-106">Direct3D evaluates each blending stage in order, beginning with the first texture in the set and ending with the eighth.</span></span>

<span data-ttu-id="59807-107">Direct3D aplica la información de cada textura en el conjunto de texturas actuales a la fase de fusión que está asociada con ella.</span><span class="sxs-lookup"><span data-stu-id="59807-107">Direct3D applies the information from each texture in the set of current textures to the blending stage that is associated with it.</span></span> <span data-ttu-id="59807-108">Las aplicaciones controlan qué información de una fase de textura se usa llamando a [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="59807-108">Applications control what information from a texture stage is used by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api).</span></span> <span data-ttu-id="59807-109">Puede establecer operaciones independientes para los canales alfa y de color, y cada operación utiliza dos argumentos.</span><span class="sxs-lookup"><span data-stu-id="59807-109">You can set separate operations for the color and alpha channels, and each operation uses two arguments.</span></span> <span data-ttu-id="59807-110">Especifique las operaciones del canal de color mediante el estado de fase de D3DTSS \_ COLOROP; especifique las operaciones alfa mediante D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="59807-110">Specify color channel operations by using the D3DTSS\_COLOROP stage state; specify alpha operations by using D3DTSS\_ALPHAOP.</span></span> <span data-ttu-id="59807-111">Ambos Estados de fase usan valores del tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="59807-111">Both stage states use values from the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span>

<span data-ttu-id="59807-112">Los argumentos de combinación de texturas usan los \_ miembros D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 y D3DTSS \_ ALPHARG2 del tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="59807-112">Texture blending arguments use the D3DTSS\_COLORARG1, D3DTSS\_COLORARG2, D3DTSS\_ALPHARG1, and D3DTSS\_ALPHARG2 members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="59807-113">Los valores de argumento correspondientes se identifican mediante [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="59807-113">The corresponding argument values are identified using [D3DTA](d3dta.md).</span></span>

> [!Note]  
> <span data-ttu-id="59807-114">Puede deshabilitar una fase de textura (y todas las fases de fusión de texturas posteriores en cascada) estableciendo la operación de color para esa fase en D3DTOP \_ deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="59807-114">You can disable a texture stage - and any subsequent texture blending stages in the cascade - by setting the color operation for that stage to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="59807-115">Deshabilitar la operación de color realmente deshabilita también la operación alfa.</span><span class="sxs-lookup"><span data-stu-id="59807-115">Disabling the color operation effectively disables the alpha operation as well.</span></span> <span data-ttu-id="59807-116">Las operaciones alfa no se pueden deshabilitar cuando se habilitan las operaciones de color.</span><span class="sxs-lookup"><span data-stu-id="59807-116">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="59807-117">La configuración de la operación Alpha en D3DTOP \_ se deshabilita cuando la combinación de colores está habilitada provoca un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="59807-117">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

 

<span data-ttu-id="59807-118">Para determinar las operaciones admitidas de mezcla de texturas de un dispositivo, consulte el miembro TextureCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="59807-118">To determine the supported texture blending operations of a device, query the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59807-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59807-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59807-120">Combinación de texturas</span><span class="sxs-lookup"><span data-stu-id="59807-120">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
