---
title: texkill-PS
description: Cancela la representación del píxel actual si alguno de los tres primeros componentes (UVW) de las coordenadas de textura es menor que cero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358465"
---
# <a name="texkill---ps"></a><span data-ttu-id="c5753-103">texkill-PS</span><span class="sxs-lookup"><span data-stu-id="c5753-103">texkill - ps</span></span>

<span data-ttu-id="c5753-104">Cancela la representación del píxel actual si alguno de los tres primeros componentes (UVW) de las coordenadas de textura es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="c5753-104">Cancels rendering of the current pixel if any of the first three components (UVW) of the texture coordinates is less than zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5753-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5753-105">Syntax</span></span>



| <span data-ttu-id="c5753-106">texkill DST</span><span class="sxs-lookup"><span data-stu-id="c5753-106">texkill dst</span></span> |
|-------------|



 

<span data-ttu-id="c5753-107">, donde</span><span class="sxs-lookup"><span data-stu-id="c5753-107">where</span></span>

-   <span data-ttu-id="c5753-108">DST es un registro de destino</span><span class="sxs-lookup"><span data-stu-id="c5753-108">dst is a destination register</span></span>

## <a name="remarks"></a><span data-ttu-id="c5753-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5753-109">Remarks</span></span>



| <span data-ttu-id="c5753-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c5753-110">Pixel shader versions</span></span> | <span data-ttu-id="c5753-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="c5753-111">1\_1</span></span> | <span data-ttu-id="c5753-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="c5753-112">1\_2</span></span> | <span data-ttu-id="c5753-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c5753-113">1\_3</span></span> | <span data-ttu-id="c5753-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="c5753-114">1\_4</span></span> | <span data-ttu-id="c5753-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5753-115">2\_0</span></span> | <span data-ttu-id="c5753-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c5753-116">2\_x</span></span> | <span data-ttu-id="c5753-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c5753-117">2\_sw</span></span> | <span data-ttu-id="c5753-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5753-118">3\_0</span></span> | <span data-ttu-id="c5753-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c5753-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c5753-120">texkill</span><span class="sxs-lookup"><span data-stu-id="c5753-120">texkill</span></span>               | <span data-ttu-id="c5753-121">x</span><span class="sxs-lookup"><span data-stu-id="c5753-121">x</span></span>    | <span data-ttu-id="c5753-122">x</span><span class="sxs-lookup"><span data-stu-id="c5753-122">x</span></span>    | <span data-ttu-id="c5753-123">x</span><span class="sxs-lookup"><span data-stu-id="c5753-123">x</span></span>    | <span data-ttu-id="c5753-124">x</span><span class="sxs-lookup"><span data-stu-id="c5753-124">x</span></span>    | <span data-ttu-id="c5753-125">x</span><span class="sxs-lookup"><span data-stu-id="c5753-125">x</span></span>    | <span data-ttu-id="c5753-126">x</span><span class="sxs-lookup"><span data-stu-id="c5753-126">x</span></span>    | <span data-ttu-id="c5753-127">x</span><span class="sxs-lookup"><span data-stu-id="c5753-127">x</span></span>     | <span data-ttu-id="c5753-128">x</span><span class="sxs-lookup"><span data-stu-id="c5753-128">x</span></span>    | <span data-ttu-id="c5753-129">x</span><span class="sxs-lookup"><span data-stu-id="c5753-129">x</span></span>     |



 

<span data-ttu-id="c5753-130">Esta instrucción corresponde a la función de [**recorte**](dx-graphics-hlsl-clip.md) de HLSL.</span><span class="sxs-lookup"><span data-stu-id="c5753-130">This instruction corresponds to the HLSL's [**clip**](dx-graphics-hlsl-clip.md) function.</span></span>

<span data-ttu-id="c5753-131">texkill no muestra ninguna textura.</span><span class="sxs-lookup"><span data-stu-id="c5753-131">texkill does not sample any texture.</span></span> <span data-ttu-id="c5753-132">Opera en los tres primeros componentes de las coordenadas de textura especificadas por el número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c5753-132">It operates on the first three components of the texture coordinates given by the destination register number.</span></span> <span data-ttu-id="c5753-133">En el caso de PS \_ 1 \_ 4, texkill funciona en los datos de los tres primeros componentes del registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c5753-133">For ps\_1\_4, texkill operates on the data in the first three components of the destination register.</span></span>

<span data-ttu-id="c5753-134">Puede usar esta instrucción para implementar planos de clips arbitrarios en el rasterizador.</span><span class="sxs-lookup"><span data-stu-id="c5753-134">You can use this instruction to implement arbitrary clip planes in the rasterizer.</span></span>

<span data-ttu-id="c5753-135">Al usar sombreadores de vértices, la aplicación es responsable de aplicar la transformación de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="c5753-135">When using vertex shaders, the application is responsible for applying the perspective transform.</span></span> <span data-ttu-id="c5753-136">Esto puede causar problemas en los planos de recorte arbitrarios porque, si contiene factores de escala de anisomorphic, también es necesario transformar los planos de clips.</span><span class="sxs-lookup"><span data-stu-id="c5753-136">This can cause problems for the arbitrary clipping planes because if it contains anisomorphic scale factors, the clip planes need to be transformed as well.</span></span> <span data-ttu-id="c5753-137">Por lo tanto, es mejor proporcionar una posición de vértice sin proyecto para usarla en el Clipper arbitrario, que es el conjunto de coordenadas de textura identificado por el operador texkill.</span><span class="sxs-lookup"><span data-stu-id="c5753-137">Therefore, it is best to provide an unprojected vertex position to use in the arbitrary clipper, which is the texture coordinate set identified by the texkill operator.</span></span>

<span data-ttu-id="c5753-138">Esta instrucción se utiliza como sigue:</span><span class="sxs-lookup"><span data-stu-id="c5753-138">This instruction is used as follows:</span></span>

<dl> <span data-ttu-id="c5753-139">texkill TN</span><span class="sxs-lookup"><span data-stu-id="c5753-139">texkill tn</span></span>  
<span data-ttu-id="c5753-140">El enmascaramiento de píxeles se realiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c5753-140">// The pixel masking is accomplished as follows:</span></span>  
<span data-ttu-id="c5753-141">if (los componentes x, y, z de TextureCoordinates (Stage n)<sub>UVWQ</sub>< 0)</span><span class="sxs-lookup"><span data-stu-id="c5753-141">if ( the x,y,z components of TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )</span></span>  
<span data-ttu-id="c5753-142">cancelar representación de píxeles</span><span class="sxs-lookup"><span data-stu-id="c5753-142">cancel pixel render</span></span>
</dl>

<span data-ttu-id="c5753-143">Para el sombreador de píxeles 1 \_ 1, 1 \_ 2 y 1 \_ 3, texkill funciona en el conjunto de coordenadas de textura proporcionado por el número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c5753-143">For pixel shader 1\_1, 1\_2, and 1\_3, texkill operates on the texture coordinate set given by the destination register number.</span></span> <span data-ttu-id="c5753-144">En la versión 1 \_ 4, sin embargo, texkill funciona en los datos contenidos en el [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) o en el registro temporal (RN) que se ha especificado como destino.</span><span class="sxs-lookup"><span data-stu-id="c5753-144">In version 1\_4, however, texkill operates on the data contained in the [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) or in the temporary register (rn) that has been specified as the destination.</span></span>

<span data-ttu-id="c5753-145">Cuando se habilita el muestreo múltiple, el efecto de suavizado de contorno que se consigue en los bordes de polígono debido al muestreo múltiple no se logrará en los bordes generados por texkill.</span><span class="sxs-lookup"><span data-stu-id="c5753-145">When multisampling is enabled, any antialiasing effect achieved on polygon edges due to multisampling will not be achieved along any edge that has been generated by texkill.</span></span> <span data-ttu-id="c5753-146">El sombreador de píxeles se ejecuta una vez por píxel.</span><span class="sxs-lookup"><span data-stu-id="c5753-146">The pixel shader runs once per pixel.</span></span>

<span data-ttu-id="c5753-147">Este ejemplo solo tiene propósitos ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="c5753-147">This example is for illustration only.</span></span>

<span data-ttu-id="c5753-148">Este ejemplo enmascara los píxeles que tienen coordenadas de textura negativas.</span><span class="sxs-lookup"><span data-stu-id="c5753-148">This example masks out pixels that have negative texture coordinates.</span></span> <span data-ttu-id="c5753-149">Los colores de píxeles se interpolan a partir de los colores de los vértices proporcionados en los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="c5753-149">The pixel colors are interpolated from vertex colors provided in the vertex data.</span></span>


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



<span data-ttu-id="c5753-150">Las coordenadas de textura van de-0,5 a 0,5 en u y 0,0 a 1,0 en v.</span><span class="sxs-lookup"><span data-stu-id="c5753-150">The texture coordinates range from -0.5 to 0.5 in u, and 0.0 to 1.0 in v.</span></span> <span data-ttu-id="c5753-151">Esta instrucción hace que los valores de u negativos queden enmascarados. En la primera ilustración siguiente se muestra el color de vértice aplicado a la cuádruple sin aplicar la instrucción texkill.</span><span class="sxs-lookup"><span data-stu-id="c5753-151">This instruction causes the negative u values to get masked out. The first illustration below shows the vertex color applied to the quad without the texkill instruction applied.</span></span> <span data-ttu-id="c5753-152">En la segunda ilustración siguiente se muestra el resultado de la instrucción texkill.</span><span class="sxs-lookup"><span data-stu-id="c5753-152">The second illustration below shows the result of the texkill instruction.</span></span> <span data-ttu-id="c5753-153">Los colores de píxeles de las coordenadas de textura inferiores a 0 (donde x va de-0,5 a 0,0) se enmascaran. El color de fondo (blanco) se usa cuando se enmascara el color de píxel.</span><span class="sxs-lookup"><span data-stu-id="c5753-153">The pixel colors from the texture coordinates below 0 (where x goes from -0.5 to 0.0) are masked out. The background color (white) is used where the pixel color is masked.</span></span>

![Ilustración de la salida con el color de vértice aplicado a la cuádruple sin la instrucción texkill](images/pstexkill-in.jpg)![Ilustración de la salida con la instrucción texkill aplicada](images/pstexkill-out.jpg)

<span data-ttu-id="c5753-156">Los datos de coordenadas de textura se declaran en la declaración de datos de vértice en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c5753-156">The texture coordinate data is declared in the vertex data declaration in this example.</span></span>


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a><span data-ttu-id="c5753-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5753-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5753-158">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c5753-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




