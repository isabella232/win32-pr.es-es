---
description: Define las operaciones de combinación de texturas por fase.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Enumeración D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362502"
---
# <a name="d3dtextureop-enumeration"></a><span data-ttu-id="2feb6-103">Enumeración D3DTEXTUREOP</span><span class="sxs-lookup"><span data-stu-id="2feb6-103">D3DTEXTUREOP enumeration</span></span>

<span data-ttu-id="2feb6-104">Define las operaciones de combinación de texturas por fase.</span><span class="sxs-lookup"><span data-stu-id="2feb6-104">Defines per-stage texture-blending operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="2feb6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2feb6-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a><span data-ttu-id="2feb6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2feb6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2feb6-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**Deshabilitación de D3DTOP \_**</span><span class="sxs-lookup"><span data-stu-id="2feb6-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-108">Deshabilita la salida de esta fase de textura y todas las fases con un índice superior.</span><span class="sxs-lookup"><span data-stu-id="2feb6-108">Disables output from this texture stage and all stages with a higher index.</span></span> <span data-ttu-id="2feb6-109">Para deshabilitar la asignación de texturas, establezca este valor como la operación de color para la primera fase de textura (fase 0).</span><span class="sxs-lookup"><span data-stu-id="2feb6-109">To disable texture mapping, set this as the color operation for the first texture stage (stage 0).</span></span> <span data-ttu-id="2feb6-110">Las operaciones alfa no se pueden deshabilitar cuando se habilitan las operaciones de color.</span><span class="sxs-lookup"><span data-stu-id="2feb6-110">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="2feb6-111">La configuración de la operación Alpha en D3DTOP \_ se deshabilita cuando la combinación de colores está habilitada provoca un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="2feb6-111">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

</dd> <dt>

<span data-ttu-id="2feb6-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**</span><span class="sxs-lookup"><span data-stu-id="2feb6-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP\_SELECTARG1**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-113">Use el primer argumento de color o alfa de esta fase de textura, sin modificar, como salida.</span><span class="sxs-lookup"><span data-stu-id="2feb6-113">Use this texture stage's first color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="2feb6-114">Esta operación afecta al argumento de color cuando se usa con el \_ Estado D3DTSS COLOROP Texture-Stage y el argumento alfa cuando se usa con D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="2feb6-114">This operation affects the color argument when used with the D3DTSS\_COLOROP texture-stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![ecuación de este argumento (1) = arg1)](images/topfrm1.png)

</dd> <dt>

<span data-ttu-id="2feb6-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**</span><span class="sxs-lookup"><span data-stu-id="2feb6-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP\_SELECTARG2**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-117">Use el segundo argumento de color o alfa de esta fase de textura, sin modificar, como salida.</span><span class="sxs-lookup"><span data-stu-id="2feb6-117">Use this texture stage's second color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="2feb6-118">Esta operación afecta al argumento de color cuando se usa con el estado de fase de textura de D3DTSS \_ COLOROP y el argumento alfa cuando se usa con D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="2feb6-118">This operation affects the color argument when used with the D3DTSS\_COLOROP texture stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![ecuación de este argumento (1) = arg2)](images/topfrm2.png)

</dd> <dt>

<span data-ttu-id="2feb6-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP \_ modular**</span><span class="sxs-lookup"><span data-stu-id="2feb6-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP\_MODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-121">Multiplique los componentes de los argumentos.</span><span class="sxs-lookup"><span data-stu-id="2feb6-121">Multiply the components of the arguments.</span></span>

![ecuación de las operaciones modulares (RGBA) = arg1 x Arg 2)](images/topfrm3.png)

</dd> <dt>

<span data-ttu-id="2feb6-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**</span><span class="sxs-lookup"><span data-stu-id="2feb6-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP\_MODULATE2X**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-124">Multiplique los componentes de los argumentos y desplace los productos a la izquierda de 1 bit (de forma eficaz, multiplíquelo por 2) para aclararlos.</span><span class="sxs-lookup"><span data-stu-id="2feb6-124">Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening.</span></span>

![ecuación de las operaciones modulate2x (RGBA) = (arg1 x Arg 2) then Shift Left 1)](images/topfrm4.png)

</dd> <dt>

<span data-ttu-id="2feb6-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**</span><span class="sxs-lookup"><span data-stu-id="2feb6-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP\_MODULATE4X**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-127">Multiplique los componentes de los argumentos y desplace los productos a los 2 bits de la izquierda (de forma eficaz, multiplíquelo por 4) para aclararlos.</span><span class="sxs-lookup"><span data-stu-id="2feb6-127">Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening.</span></span>

![ecuación de las operaciones modulate4x (RGBA) = (arg1 x Arg 2) then Shift Left 2)](images/topfrm5.png)

</dd> <dt>

<span data-ttu-id="2feb6-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Agregar**</span><span class="sxs-lookup"><span data-stu-id="2feb6-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-130">Agregue los componentes de los argumentos.</span><span class="sxs-lookup"><span data-stu-id="2feb6-130">Add the components of the arguments.</span></span>

![ecuación de las operaciones de adición (RGBA) = arg1 + Arg 2)](images/topfrm6.png)

</dd> <dt>

<span data-ttu-id="2feb6-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDSIGNED**</span><span class="sxs-lookup"><span data-stu-id="2feb6-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP\_ADDSIGNED**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-133">Agregue los componentes de los argumentos con una diferencia de-0,5, lo que convierte el intervalo efectivo de valores entre-0,5 y 0,5.</span><span class="sxs-lookup"><span data-stu-id="2feb6-133">Add the components of the arguments with a - 0.5 bias, making the effective range of values from - 0.5 through 0.5.</span></span>

![ecuación de la operación agregar firma (es decir, RGBA) = arg1 + Arg 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span data-ttu-id="2feb6-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**</span><span class="sxs-lookup"><span data-stu-id="2feb6-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP\_ADDSIGNED2X**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-136">Agregue los componentes de los argumentos con una diferencia de-0,5 y desplace los productos a la izquierda 1 bit.</span><span class="sxs-lookup"><span data-stu-id="2feb6-136">Add the components of the arguments with a - 0.5 bias, and shift the products to the left 1 bit.</span></span>

![ecuación de la operación agregar 2x con signo ((s (RGBA) = arg1 + Arg 2-0,5) then Shift Left 1)](images/topfrm8.png)

</dd> <dt>

<span data-ttu-id="2feb6-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**Resta de D3DTOP \_**</span><span class="sxs-lookup"><span data-stu-id="2feb6-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-139">Reste los componentes del segundo argumento de los del primer argumento.</span><span class="sxs-lookup"><span data-stu-id="2feb6-139">Subtract the components of the second argument from those of the first argument.</span></span>

![ecuación de la operación de resta (s (RGBA) = arg1-Arg 2)](images/topfrm9.png)

</dd> <dt>

<span data-ttu-id="2feb6-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDSMOOTH**</span><span class="sxs-lookup"><span data-stu-id="2feb6-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP\_ADDSMOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-142">Agregue el primer y el segundo argumento; a continuación, reste su producto a la suma.</span><span class="sxs-lookup"><span data-stu-id="2feb6-142">Add the first and second arguments; then subtract their product from the sum.</span></span>

![ecuación de la operación agregar Smooth (es decir, RGBA) = arg1 + Arg 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span data-ttu-id="2feb6-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**</span><span class="sxs-lookup"><span data-stu-id="2feb6-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP\_BLENDDIFFUSEALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-145">Mezcle linealmente esta fase de textura con el alfa interpolado de cada vértice.</span><span class="sxs-lookup"><span data-stu-id="2feb6-145">Linearly blend this texture stage, using the interpolated alpha from each vertex.</span></span>

![ecuación de las operaciones alfa difusas de Blend (RGBA) = arg1 x alfa + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="2feb6-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**</span><span class="sxs-lookup"><span data-stu-id="2feb6-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP\_BLENDTEXTUREALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-148">Mezcle linealmente esta fase de textura con el alfa de la textura de esta fase.</span><span class="sxs-lookup"><span data-stu-id="2feb6-148">Linearly blend this texture stage, using the alpha from this stage's texture.</span></span>

![ecuación de la operación alfa de textura de mezcla (es decir, RGBA) = arg1 x alfa + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="2feb6-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**</span><span class="sxs-lookup"><span data-stu-id="2feb6-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP\_BLENDFACTORALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-151">Mezcle linealmente esta fase de textura mediante un conjunto de alfa escalar con el estado de representación de TEXTUREFACTOR de D3DRS \_ .</span><span class="sxs-lookup"><span data-stu-id="2feb6-151">Linearly blend this texture stage, using a scalar alpha set with the D3DRS\_TEXTUREFACTOR render state.</span></span>

![ecuación de la operación alfa del factor de mezcla ((RGBA) = arg1 x alfa + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="2feb6-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**</span><span class="sxs-lookup"><span data-stu-id="2feb6-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP\_BLENDTEXTUREALPHAPM**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-154">Mezcle linealmente una fase de textura que utiliza un alfa premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="2feb6-154">Linearly blend a texture stage that uses a premultiplied alpha.</span></span>

![ecuación de la operación de mezcla Alpha PM Operation (s (RGBA) = arg1 + Arg 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span data-ttu-id="2feb6-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**</span><span class="sxs-lookup"><span data-stu-id="2feb6-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP\_BLENDCURRENTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-157">Mezcle linealmente esta fase de textura con el alfa tomado de la fase de textura anterior.</span><span class="sxs-lookup"><span data-stu-id="2feb6-157">Linearly blend this texture stage, using the alpha taken from the previous texture stage.</span></span>

![ecuación de la operación alfa actual de Blend (es decir, RGBA) = arg1 x alfa + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="2feb6-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PREmodulado**</span><span class="sxs-lookup"><span data-stu-id="2feb6-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP\_PREMODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-160">D3DTOP \_ PREmodulado está establecido en la fase n.</span><span class="sxs-lookup"><span data-stu-id="2feb6-160">D3DTOP\_PREMODULATE is set in stage n.</span></span> <span data-ttu-id="2feb6-161">La salida de la fase n es arg1.</span><span class="sxs-lookup"><span data-stu-id="2feb6-161">The output of stage n is arg1.</span></span> <span data-ttu-id="2feb6-162">Además, si hay una textura en la fase n + 1, cualquier D3DTA \_ actual de la fase n + 1 se multiplica por la textura en la fase n + 1.</span><span class="sxs-lookup"><span data-stu-id="2feb6-162">Additionally, if there is a texture in stage n + 1, any D3DTA\_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.</span></span>

</dd> <dt>

<span data-ttu-id="2feb6-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="2feb6-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP\_MODULATEALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-164">Modula el color del segundo argumento, utilizando el alfa del primer argumento; a continuación, agregue el resultado al argumento uno.</span><span class="sxs-lookup"><span data-stu-id="2feb6-164">Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one.</span></span> <span data-ttu-id="2feb6-165">Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="2feb6-165">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![ecuación de las operaciones alfa de la modular de colores de agregar (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span data-ttu-id="2feb6-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="2feb6-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP\_MODULATECOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-168">Modula los argumentos; a continuación, agregue el alfa del primer argumento.</span><span class="sxs-lookup"><span data-stu-id="2feb6-168">Modulate the arguments; then add the alpha of the first argument.</span></span> <span data-ttu-id="2feb6-169">Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="2feb6-169">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![ecuación de la operación de adición de color alfa modular (es decir, RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span data-ttu-id="2feb6-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="2feb6-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP\_MODULATEINVALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-172">Similar a D3DTOP \_ MODULATEALPHA \_ ADDCOLOR, pero use el inverso del alfa del primer argumento.</span><span class="sxs-lookup"><span data-stu-id="2feb6-172">Similar to D3DTOP\_MODULATEALPHA\_ADDCOLOR, but use the inverse of the alpha of the first argument.</span></span> <span data-ttu-id="2feb6-173">Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="2feb6-173">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![ecuación de la operación de alfa inversa del modulador de color (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span data-ttu-id="2feb6-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="2feb6-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP\_MODULATEINVCOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-176">Similar a D3DTOP \_ MODULATECOLOR \_ ADDALPHA, pero usa el inverso del color del primer argumento.</span><span class="sxs-lookup"><span data-stu-id="2feb6-176">Similar to D3DTOP\_MODULATECOLOR\_ADDALPHA, but use the inverse of the color of the first argument.</span></span> <span data-ttu-id="2feb6-177">Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="2feb6-177">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![ecuación de la operación agregar color inverso alfa modular (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span data-ttu-id="2feb6-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**</span><span class="sxs-lookup"><span data-stu-id="2feb6-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP\_BUMPENVMAP**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-180">Realice la asignación de rugosidad por píxel mediante el mapa de entorno en la siguiente fase de textura, sin luminancia.</span><span class="sxs-lookup"><span data-stu-id="2feb6-180">Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance.</span></span> <span data-ttu-id="2feb6-181">Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="2feb6-181">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="2feb6-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**</span><span class="sxs-lookup"><span data-stu-id="2feb6-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP\_BUMPENVMAPLUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-183">Realice la asignación de rugosidad por píxel mediante el mapa de entorno en la siguiente fase de textura, con luminancia.</span><span class="sxs-lookup"><span data-stu-id="2feb6-183">Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance.</span></span> <span data-ttu-id="2feb6-184">Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="2feb6-184">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="2feb6-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**</span><span class="sxs-lookup"><span data-stu-id="2feb6-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP\_DOTPRODUCT3**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-186">Modula los componentes de cada argumento como componentes firmados, agrega sus productos; a continuación, replique la suma en todos los canales de color, incluido alfa.</span><span class="sxs-lookup"><span data-stu-id="2feb6-186">Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha.</span></span> <span data-ttu-id="2feb6-187">Esta operación se admite para las operaciones de color y alfa.</span><span class="sxs-lookup"><span data-stu-id="2feb6-187">This operation is supported for color and alpha operations.</span></span>

![ecuación de las operaciones de producto de punto 3 (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

<span data-ttu-id="2feb6-189">En DirectX 6 y DirectX 7, las operaciones de múltiples texturas las entradas anteriores se desplazan hacia abajo a la mitad (y = x-0,5) antes de usarlas para simular los datos firmados, y el resultado escalar se fija automáticamente en valores positivos y se replica en los tres canales de salida.</span><span class="sxs-lookup"><span data-stu-id="2feb6-189">In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels.</span></span> <span data-ttu-id="2feb6-190">Además, tenga en cuenta que, como operación de color, no se actualiza el Alpha; simplemente, se actualizan los componentes RGB.</span><span class="sxs-lookup"><span data-stu-id="2feb6-190">Also, note that as a color operation this does not updated the alpha it just updates the RGB components.</span></span>

<span data-ttu-id="2feb6-191">Sin embargo, en los sombreadores de DirectX 8,1 puede especificar que la salida se enrute a los componentes. RGB o. a, o a ambos (el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="2feb6-191">However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default).</span></span> <span data-ttu-id="2feb6-192">También puede especificar una operación escalar independiente en el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="2feb6-192">You can also specify a separate scalar operation on the alpha channel.</span></span>

</dd> <dt>

<span data-ttu-id="2feb6-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**</span><span class="sxs-lookup"><span data-stu-id="2feb6-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP\_MULTIPLYADD**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-194">Realiza una operación de multiplicación acumulada.</span><span class="sxs-lookup"><span data-stu-id="2feb6-194">Performs a multiply-accumulate operation.</span></span> <span data-ttu-id="2feb6-195">Toma los dos últimos argumentos, los multiplica juntos y los agrega al argumento de entrada/origen restante y lo coloca en el resultado.</span><span class="sxs-lookup"><span data-stu-id="2feb6-195">It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result.</span></span>

<span data-ttu-id="2feb6-196">S<sub>RGBA</sub> = arg1 + arg2 \* Arg3</span><span class="sxs-lookup"><span data-stu-id="2feb6-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span></span>

</dd> <dt>

<span data-ttu-id="2feb6-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ lerp**</span><span class="sxs-lookup"><span data-stu-id="2feb6-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP\_LERP**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-198">Interpola linealmente entre el segundo y tercer argumento de origen mediante una proporción especificada en el primer argumento de origen.</span><span class="sxs-lookup"><span data-stu-id="2feb6-198">Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.</span></span>

<span data-ttu-id="2feb6-199">S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* Arg3.</span><span class="sxs-lookup"><span data-stu-id="2feb6-199">S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.</span></span>

</dd> <dt>

<span data-ttu-id="2feb6-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2feb6-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2feb6-201">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="2feb6-201">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2feb6-202">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2feb6-202">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2feb6-203">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2feb6-203">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2feb6-204">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2feb6-204">Remarks</span></span>

<span data-ttu-id="2feb6-205">Los miembros de este tipo se usan al establecer operaciones de color o alfa mediante los valores de D3DTSS \_ COLOROP o D3DTSS \_ ALPHAOP con el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="2feb6-205">The members of this type are used when setting color or alpha operations by using the D3DTSS\_COLOROP or D3DTSS\_ALPHAOP values with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span>

<span data-ttu-id="2feb6-206">En las fórmulas anteriores, S<sub>RGBA</sub> es el color RGBA generado por una operación de textura, y arg1, arg2 y Arg3 representan el color RGBA completo de los argumentos de textura.</span><span class="sxs-lookup"><span data-stu-id="2feb6-206">In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments.</span></span> <span data-ttu-id="2feb6-207">Los componentes individuales de un argumento se muestran con subíndices.</span><span class="sxs-lookup"><span data-stu-id="2feb6-207">Individual components of an argument are shown with subscripts.</span></span> <span data-ttu-id="2feb6-208">Por ejemplo, el componente alfa para el argumento 1 se mostraría como arg1<sub>A</sub>.</span><span class="sxs-lookup"><span data-stu-id="2feb6-208">For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.</span></span>

## <a name="requirements"></a><span data-ttu-id="2feb6-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2feb6-209">Requirements</span></span>



| <span data-ttu-id="2feb6-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="2feb6-210">Requirement</span></span> | <span data-ttu-id="2feb6-211">Value</span><span class="sxs-lookup"><span data-stu-id="2feb6-211">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2feb6-212">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2feb6-212">Header</span></span><br/> | <dl> <span data-ttu-id="2feb6-213"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2feb6-213"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2feb6-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="2feb6-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2feb6-215">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2feb6-215">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2feb6-216">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="2feb6-216">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
