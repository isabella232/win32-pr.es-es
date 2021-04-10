---
description: Una fase de combinación es un conjunto de operaciones de textura y sus argumentos que definen cómo se combinan las texturas.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Crear fases de fusión (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153128"
---
# <a name="creating-blending-stages-direct3d-9"></a><span data-ttu-id="edbfa-103">Crear fases de fusión (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="edbfa-103">Creating Blending Stages (Direct3D 9)</span></span>

<span data-ttu-id="edbfa-104">Una fase de combinación es un conjunto de operaciones de textura y sus argumentos que definen cómo se combinan las texturas.</span><span class="sxs-lookup"><span data-stu-id="edbfa-104">A blending stage is a set of texture operations and their arguments that define how textures are blended.</span></span> <span data-ttu-id="edbfa-105">Al realizar una fase de combinación, las aplicaciones de C++ invocan el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="edbfa-105">When making a blending stage, C++ applications invoke the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="edbfa-106">La primera llamada especifica la operación que se realiza.</span><span class="sxs-lookup"><span data-stu-id="edbfa-106">The first call specifies the operation that is performed.</span></span> <span data-ttu-id="edbfa-107">Dos llamadas adicionales definen los argumentos a los que se aplica la operación.</span><span class="sxs-lookup"><span data-stu-id="edbfa-107">Two additional invocations define the arguments to which the operation is applied.</span></span> <span data-ttu-id="edbfa-108">En el ejemplo de código siguiente se muestra la creación de una fase de fusión.</span><span class="sxs-lookup"><span data-stu-id="edbfa-108">The following code example illustrates the creation of a blending stage.</span></span>


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



<span data-ttu-id="edbfa-109">Los datos de textura en las texturas contienen valores de color y alfa.</span><span class="sxs-lookup"><span data-stu-id="edbfa-109">Texel data in textures contain color and alpha values.</span></span> <span data-ttu-id="edbfa-110">Las aplicaciones pueden definir operaciones independientes para los valores de color y alfa en una sola fase de mezcla.</span><span class="sxs-lookup"><span data-stu-id="edbfa-110">Applications can define separate operations for both color and alpha values in a single blending stage.</span></span> <span data-ttu-id="edbfa-111">Cada operación, color y alfa tienen sus propios argumentos.</span><span class="sxs-lookup"><span data-stu-id="edbfa-111">Each operation, color, and alpha, has its own arguments.</span></span> <span data-ttu-id="edbfa-112">Para obtener más información, consulte [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="edbfa-112">For details, see [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

<span data-ttu-id="edbfa-113">Aunque no forme parte de la API de Direct3D, puede insertar las siguientes macros en la aplicación para abreviar el código necesario para crear fases de fusión de texturas.</span><span class="sxs-lookup"><span data-stu-id="edbfa-113">Although not part of the Direct3D API, you can insert the following macros into your application to abbreviate the code required for creating texture blending stages.</span></span>


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a><span data-ttu-id="edbfa-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edbfa-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edbfa-115">Combinación de texturas</span><span class="sxs-lookup"><span data-stu-id="edbfa-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
