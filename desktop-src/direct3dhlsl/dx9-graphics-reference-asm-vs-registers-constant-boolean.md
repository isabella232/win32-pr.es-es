---
title: Registro booleano constante (referencia de HLSL VS)
description: Este registro es una colección de bits utilizada en las instrucciones de control de flujo estático (por ejemplo, si es bool-vs-else-vs-endif-vs).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984035"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a><span data-ttu-id="ba23c-103">Registro booleano constante (referencia de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="ba23c-103">Constant Boolean register (HLSL VS reference)</span></span>

<span data-ttu-id="ba23c-104">Este registro es una colección de bits utilizada en las instrucciones de control de flujo estático (por ejemplo, [si es bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [endif-vs](endif---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="ba23c-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - vs](if-bool---vs.md) - [else - vs](else---vs.md) - [endif - vs](endif---vs.md)).</span></span> <span data-ttu-id="ba23c-105">Hay 16 de ellos, por lo tanto, un sombreador puede tener 16 condiciones de rama independientes.</span><span class="sxs-lookup"><span data-stu-id="ba23c-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="ba23c-106">Se pueden establecer mediante [defb-vs](defb---vs.md) o [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="ba23c-106">They can be set using [defb - vs](defb---vs.md) or [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span></span>

<span data-ttu-id="ba23c-107">El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ba23c-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="ba23c-108">En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ba23c-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="ba23c-109">La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="ba23c-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="ba23c-110">Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global.</span><span class="sxs-lookup"><span data-stu-id="ba23c-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="ba23c-111">Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="ba23c-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="ba23c-112">En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ba23c-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="ba23c-113">Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.</span><span class="sxs-lookup"><span data-stu-id="ba23c-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba23c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba23c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba23c-115">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ba23c-115">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 