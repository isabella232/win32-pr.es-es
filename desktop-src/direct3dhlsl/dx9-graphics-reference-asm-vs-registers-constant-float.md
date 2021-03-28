---
title: Registro Float constante (HLSL VS Reference)
description: Registro de entrada del sombreador de vértices para una constante de punto flotante de cuatro componentes. Establezca un registro constante con Def-vs o SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420863"
---
# <a name="constant-float-register-hlsl-vs-reference"></a><span data-ttu-id="c7bb3-104">Registro Float constante (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="c7bb3-104">Constant float register (HLSL VS reference)</span></span>

<span data-ttu-id="c7bb3-105">Registro de entrada del sombreador de vértices para una constante de punto flotante de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-105">Vertex shader input register for a four component floating-point constant.</span></span> <span data-ttu-id="c7bb3-106">Establezca un registro constante con [Def-vs](def---vs.md) o [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="c7bb3-106">Set a constant register with either [def - vs](def---vs.md) or [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span></span>

<span data-ttu-id="c7bb3-107">El archivo de registro de constantes es de solo lectura desde la perspectiva del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-107">The constant register file is read-only from the perspective of the vertex shader.</span></span> <span data-ttu-id="c7bb3-108">Cualquier instrucción única solo puede tener acceso a un registro de constante.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-108">Any single instruction may access only one constant register.</span></span> <span data-ttu-id="c7bb3-109">Sin embargo, cada origen de esa instrucción puede swizzle de forma independiente y negar ese vector a medida que se lee.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-109">However, each source in that instruction may independently swizzle and negate that vector as it is read.</span></span>

<span data-ttu-id="c7bb3-110">El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-110">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="c7bb3-111">En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-111">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="c7bb3-112">La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-112">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="c7bb3-113">Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-113">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="c7bb3-114">Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-114">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="c7bb3-115">En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-115">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="c7bb3-116">Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-116">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

<span data-ttu-id="c7bb3-117">Un registro constante se designa como absoluto o relativo:</span><span class="sxs-lookup"><span data-stu-id="c7bb3-117">A constant register is designated as either absolute or relative:</span></span>


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



<span data-ttu-id="c7bb3-118">El registro constante se puede leer, por lo tanto, mediante un índice absoluto o con un índice relativo de un registro de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-118">The constant register can be read, therefore, either by using an absolute index or with a relative index from an address register.</span></span> <span data-ttu-id="c7bb3-119">Las lecturas de registros fuera del intervalo devuelven (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="c7bb3-119">Reads from out-of-range registers return (0.0, 0.0, 0.0, 0.0).</span></span>

## <a name="examples"></a><span data-ttu-id="c7bb3-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7bb3-120">Examples</span></span>

<span data-ttu-id="c7bb3-121">Este es un ejemplo en el que se declaran dos constantes de punto flotante dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-121">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="c7bb3-122">Estas constantes se cargan cada vez que se llama a [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="c7bb3-122">These constants are loaded every time [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) is called.</span></span>

<span data-ttu-id="c7bb3-123">Este es un ejemplo de uso de la API.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-123">Here is an example using the API.</span></span>


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



<span data-ttu-id="c7bb3-124">Si está estableciendo valores constantes con la API, no se requiere ninguna declaración de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7bb3-124">If you are setting constant values with the API, there is no shader declaration required.</span></span>



| <span data-ttu-id="c7bb3-125">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c7bb3-125">Vertex shader versions</span></span> | <span data-ttu-id="c7bb3-126">1\_1</span><span class="sxs-lookup"><span data-stu-id="c7bb3-126">1\_1</span></span> | <span data-ttu-id="c7bb3-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7bb3-127">2\_0</span></span> | <span data-ttu-id="c7bb3-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c7bb3-128">2\_sw</span></span> | <span data-ttu-id="c7bb3-129">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c7bb3-129">2\_x</span></span> | <span data-ttu-id="c7bb3-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7bb3-130">3\_0</span></span> | <span data-ttu-id="c7bb3-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c7bb3-131">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="c7bb3-132">Registro de constantes</span><span class="sxs-lookup"><span data-stu-id="c7bb3-132">Constant Register</span></span>      | <span data-ttu-id="c7bb3-133">x</span><span class="sxs-lookup"><span data-stu-id="c7bb3-133">x</span></span>    | <span data-ttu-id="c7bb3-134">x</span><span class="sxs-lookup"><span data-stu-id="c7bb3-134">x</span></span>    | <span data-ttu-id="c7bb3-135">x</span><span class="sxs-lookup"><span data-stu-id="c7bb3-135">x</span></span>     | <span data-ttu-id="c7bb3-136">x</span><span class="sxs-lookup"><span data-stu-id="c7bb3-136">x</span></span>    | <span data-ttu-id="c7bb3-137">x</span><span class="sxs-lookup"><span data-stu-id="c7bb3-137">x</span></span>    | <span data-ttu-id="c7bb3-138">x</span><span class="sxs-lookup"><span data-stu-id="c7bb3-138">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="c7bb3-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7bb3-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7bb3-140">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c7bb3-140">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 