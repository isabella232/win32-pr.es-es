---
title: Registro Float constante (referencia de PS de HLSL)
description: Registro de entrada del sombreador de píxeles para una constante de punto flotante 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421150"
---
# <a name="constant-float-register-hlsl-ps-reference"></a><span data-ttu-id="05093-103">Registro Float constante (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="05093-103">Constant float register (HLSL PS reference)</span></span>

<span data-ttu-id="05093-104">Registro de entrada del sombreador de píxeles para una constante de punto flotante 4D.</span><span class="sxs-lookup"><span data-stu-id="05093-104">Pixel shader input register for a 4D floating-point constant.</span></span>

<span data-ttu-id="05093-105">Se pueden establecer mediante [Def-PS](def---ps.md) o [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="05093-105">They can be set using [def - ps](def---ps.md) or [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="05093-106">El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="05093-106">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="05093-107">En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="05093-107">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="05093-108">La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="05093-108">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="05093-109">Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global.</span><span class="sxs-lookup"><span data-stu-id="05093-109">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="05093-110">Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="05093-110">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="05093-111">En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="05093-111">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="05093-112">Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.</span><span class="sxs-lookup"><span data-stu-id="05093-112">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="examples"></a><span data-ttu-id="05093-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="05093-113">Examples</span></span>

<span data-ttu-id="05093-114">Este es un ejemplo en el que se declaran dos constantes de punto flotante dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="05093-114">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="05093-115">Estas constantes se cargan cada vez que se llama a [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) .</span><span class="sxs-lookup"><span data-stu-id="05093-115">These constants are loaded every time [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) is called.</span></span>

<span data-ttu-id="05093-116">Si está estableciendo valores constantes con la API, no se requiere ninguna declaración de sombreador.</span><span class="sxs-lookup"><span data-stu-id="05093-116">If you are setting constant values with the API, there is no shader declaration required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05093-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05093-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05093-118">Registra</span><span class="sxs-lookup"><span data-stu-id="05093-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 