---
title: texcoord-PS
description: Interpreta los datos de coordenadas de textura (UVW1) como datos de color (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792195"
---
# <a name="texcoord---ps"></a><span data-ttu-id="c900d-103">texcoord-PS</span><span class="sxs-lookup"><span data-stu-id="c900d-103">texcoord - ps</span></span>

<span data-ttu-id="c900d-104">Interpreta los datos de coordenadas de textura (UVW1) como datos de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="c900d-104">Interprets texture coordinate data (UVW1) as color data (RGBA).</span></span>

## <a name="syntax"></a><span data-ttu-id="c900d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c900d-105">Syntax</span></span>



| <span data-ttu-id="c900d-106">texcoord DST</span><span class="sxs-lookup"><span data-stu-id="c900d-106">texcoord dst</span></span> |
|--------------|



 

<span data-ttu-id="c900d-107">, donde</span><span class="sxs-lookup"><span data-stu-id="c900d-107">where</span></span>

-   <span data-ttu-id="c900d-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c900d-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c900d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c900d-109">Remarks</span></span>



| <span data-ttu-id="c900d-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c900d-110">Pixel shader versions</span></span> | <span data-ttu-id="c900d-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="c900d-111">1\_1</span></span> | <span data-ttu-id="c900d-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="c900d-112">1\_2</span></span> | <span data-ttu-id="c900d-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c900d-113">1\_3</span></span> | <span data-ttu-id="c900d-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="c900d-114">1\_4</span></span> | <span data-ttu-id="c900d-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c900d-115">2\_0</span></span> | <span data-ttu-id="c900d-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c900d-116">2\_x</span></span> | <span data-ttu-id="c900d-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c900d-117">2\_sw</span></span> | <span data-ttu-id="c900d-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c900d-118">3\_0</span></span> | <span data-ttu-id="c900d-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c900d-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c900d-120">texcoord</span><span class="sxs-lookup"><span data-stu-id="c900d-120">texcoord</span></span>              | <span data-ttu-id="c900d-121">x</span><span class="sxs-lookup"><span data-stu-id="c900d-121">x</span></span>    | <span data-ttu-id="c900d-122">x</span><span class="sxs-lookup"><span data-stu-id="c900d-122">x</span></span>    | <span data-ttu-id="c900d-123">x</span><span class="sxs-lookup"><span data-stu-id="c900d-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="c900d-124">Esta instrucción interpreta el conjunto de coordenadas de textura (UVW1) correspondiente al número de registro de destino como datos de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="c900d-124">This instruction interprets the texture coordinate set (UVW1) corresponding to the destination register number as color data (RGBA).</span></span> <span data-ttu-id="c900d-125">Si el conjunto de coordenadas de textura contiene menos de tres componentes, los componentes que faltan se establecen en 0.</span><span class="sxs-lookup"><span data-stu-id="c900d-125">If the texture coordinate set contains fewer than three components, the missing components are set to 0.</span></span> <span data-ttu-id="c900d-126">El cuarto componente siempre se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="c900d-126">The fourth component is always set to 1.</span></span> <span data-ttu-id="c900d-127">Todos los valores se fijan entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="c900d-127">All values are clamped between 0 and 1.</span></span>

<span data-ttu-id="c900d-128">La ventaja de texcoord es que proporciona una manera de pasar datos de vértice interpolados a alta precisión directamente en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c900d-128">The advantage of texcoord is that it provides a way to pass vertex data interpolated at high precision directly into the pixel shader.</span></span> <span data-ttu-id="c900d-129">Sin embargo, cuando los datos se escriben en el registro de destino, se perderá cierta precisión, dependiendo del número de bits que use el hardware para los registros.</span><span class="sxs-lookup"><span data-stu-id="c900d-129">However, when the data is written into the destination register, some precision will be lost, depending on the number of bits used by the hardware for registers.</span></span>

<span data-ttu-id="c900d-130">Esta instrucción no muestrea ninguna textura.</span><span class="sxs-lookup"><span data-stu-id="c900d-130">No texture is sampled by this instruction.</span></span> <span data-ttu-id="c900d-131">Solo se aplican las coordenadas de textura establecidas en esta fase de textura.</span><span class="sxs-lookup"><span data-stu-id="c900d-131">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="c900d-132">Los datos de textura (como la posición, la normal y la dirección de origen de la luz) pueden ser asignados por un sombreador de vértices en una coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="c900d-132">Any texture data (such as position, normal, and light source direction) can be mapped by a vertex shader into a texture coordinate.</span></span> <span data-ttu-id="c900d-133">Esto se hace asociando una textura con un registro de textura mediante [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) y especificando cómo se realiza el muestreo de textura con [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="c900d-133">This is done by associating a texture with a texture register using [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) and by specifying how the texture sampling is done using [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span> <span data-ttu-id="c900d-134">Si se usa la canalización de función fija, asegúrese de proporcionar la \_ marca TSS TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="c900d-134">If the fixed function pipeline is used, be sure to supply the TSS\_TEXCOORDINDEX flag.</span></span>

<span data-ttu-id="c900d-135">Esta instrucción se utiliza como sigue:</span><span class="sxs-lookup"><span data-stu-id="c900d-135">This instruction is used as follows:</span></span>


```
texcoord tn
```



<span data-ttu-id="c900d-136">Un [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) contiene cuatro valores de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="c900d-136">An [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contains four color values (RGBA).</span></span> <span data-ttu-id="c900d-137">Los datos también se pueden considerar como datos vectoriales (xyzw).</span><span class="sxs-lookup"><span data-stu-id="c900d-137">The data can also be thought of as vector data (xyzw).</span></span> <span data-ttu-id="c900d-138">texcoord recuperará tres de estos valores (XYZ) del conjunto de coordenadas de textura x y el cuarto componente (w) se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="c900d-138">texcoord will retrieve three of these values (xyz) from texture coordinate set x, and the fourth component (w) is set to 1.</span></span> <span data-ttu-id="c900d-139">La dirección de la textura se copia desde el conjunto de coordenadas de textura n.</span><span class="sxs-lookup"><span data-stu-id="c900d-139">The texture address is copied from the texture coordinate set n.</span></span> <span data-ttu-id="c900d-140">El resultado se fija entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="c900d-140">The result is clamped between 0 and 1.</span></span>

<span data-ttu-id="c900d-141">Este ejemplo solo tiene propósitos ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="c900d-141">This example is for illustration only.</span></span> <span data-ttu-id="c900d-142">El código de C que acompaña al sombreador no se ha optimizado para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c900d-142">The C code accompanying the shader has not been optimized for performance.</span></span>

<span data-ttu-id="c900d-143">A continuación se muestra un sombreador de ejemplo que usa texcoord.</span><span class="sxs-lookup"><span data-stu-id="c900d-143">Here is an example shader using texcoord.</span></span>


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



<span data-ttu-id="c900d-144">En la ilustración siguiente se muestra la salida representada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c900d-144">The rendered output from the pixel shader is shown in the following illustration.</span></span> <span data-ttu-id="c900d-145">Los valores de coordenadas (u, v, w, 1) se asignan a los canales (RGB).</span><span class="sxs-lookup"><span data-stu-id="c900d-145">The (u,v,w,1) coordinate values map to the (rgb) channels.</span></span> <span data-ttu-id="c900d-146">El canal alfa está establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="c900d-146">The alpha channel is set to 1.</span></span> <span data-ttu-id="c900d-147">En las esquinas de la ilustración, la coordenada (0, 0, 0, 1) se interpreta como negro; (1, 0, 0, 1) es rojo; (0, 1, 0, 1) es verde; y (1, 1, 0, 1) contiene verde y rojo, lo que produce amarillo.</span><span class="sxs-lookup"><span data-stu-id="c900d-147">At the corners of the illustration, coordinate (0,0,0,1) is interpreted as black; (1,0,0,1) is red; (0,1,0,1) is green; and (1,1,0,1) contains green and red, producing yellow.</span></span>

![Ilustración de la salida representada del sombreador de píxeles de ejemplo](images/pstexcoord.jpg)

<span data-ttu-id="c900d-149">Se requiere código adicional para usar este sombreador y se muestra un escenario de ejemplo a continuación.</span><span class="sxs-lookup"><span data-stu-id="c900d-149">Additional code is required to use this shader and an example scenario is shown below.</span></span>


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a><span data-ttu-id="c900d-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c900d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c900d-151">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c900d-151">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 