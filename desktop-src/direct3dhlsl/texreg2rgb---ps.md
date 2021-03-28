---
title: texreg2rgb-PS
description: Interpreta los componentes de color rojo, verde y azul (RGB) del registro de origen como datos de dirección de textura para que muestren la textura en la fase correspondiente al número de registro de destino. El resultado se almacena en el registro de destino.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532878"
---
# <a name="texreg2rgb---ps"></a><span data-ttu-id="75146-104">texreg2rgb-PS</span><span class="sxs-lookup"><span data-stu-id="75146-104">texreg2rgb - ps</span></span>

<span data-ttu-id="75146-105">Interpreta los componentes de color rojo, verde y azul (RGB) del registro de origen como datos de dirección de textura para que muestren la textura en la fase correspondiente al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="75146-105">Interprets the red, green, and blue (RGB) color components of the source register as texture address data in order to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="75146-106">El resultado se almacena en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="75146-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="75146-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75146-107">Syntax</span></span>



| <span data-ttu-id="75146-108">texreg2rgb DST, src</span><span class="sxs-lookup"><span data-stu-id="75146-108">texreg2rgb dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="75146-109">, donde</span><span class="sxs-lookup"><span data-stu-id="75146-109">where</span></span>

-   <span data-ttu-id="75146-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="75146-110">dst is the destination register.</span></span>
-   <span data-ttu-id="75146-111">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="75146-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="75146-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75146-112">Remarks</span></span>



| <span data-ttu-id="75146-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="75146-113">Pixel shader versions</span></span> | <span data-ttu-id="75146-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="75146-114">1\_1</span></span> | <span data-ttu-id="75146-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="75146-115">1\_2</span></span> | <span data-ttu-id="75146-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="75146-116">1\_3</span></span> | <span data-ttu-id="75146-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="75146-117">1\_4</span></span> | <span data-ttu-id="75146-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75146-118">2\_0</span></span> | <span data-ttu-id="75146-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="75146-119">2\_x</span></span> | <span data-ttu-id="75146-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="75146-120">2\_sw</span></span> | <span data-ttu-id="75146-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75146-121">3\_0</span></span> | <span data-ttu-id="75146-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="75146-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="75146-123">texreg2rgb</span><span class="sxs-lookup"><span data-stu-id="75146-123">texreg2rgb</span></span>            |      | <span data-ttu-id="75146-124">x</span><span class="sxs-lookup"><span data-stu-id="75146-124">x</span></span>    | <span data-ttu-id="75146-125">x</span><span class="sxs-lookup"><span data-stu-id="75146-125">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="75146-126">Esta instrucción es útil para las operaciones de reasignación de espacio de color.</span><span class="sxs-lookup"><span data-stu-id="75146-126">This instruction is useful for color-space remapping operations.</span></span> <span data-ttu-id="75146-127">Admite coordenadas bidimensionales (2D) y tridimensionales (3D).</span><span class="sxs-lookup"><span data-stu-id="75146-127">It supports two-dimensional (2D) and three-dimensional (3D) coordinates.</span></span> <span data-ttu-id="75146-128">Se puede usar del mismo modo que [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md) para reasignar datos 2D.</span><span class="sxs-lookup"><span data-stu-id="75146-128">It can be used just like the [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md) to remap 2D data.</span></span> <span data-ttu-id="75146-129">Sin embargo, esta instrucción también admite datos 3D, por lo que se puede usar con mapas de cubos y texturas de volumen 3D.</span><span class="sxs-lookup"><span data-stu-id="75146-129">However, this instruction also supports 3D data so it can be used with cube maps and 3D volume textures.</span></span>

<span data-ttu-id="75146-130">Este es un ejemplo de la secuencia que sigue la instrucción.</span><span class="sxs-lookup"><span data-stu-id="75146-130">Here is an example of the sequence the instruction follows.</span></span>


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



<span data-ttu-id="75146-131">Aquí encontrará más detalles sobre cómo se realiza la reasignación.</span><span class="sxs-lookup"><span data-stu-id="75146-131">Here is more detail about how the remapping is accomplished.</span></span>

<dl> <span data-ttu-id="75146-132">La primera instrucción carga el color de textura (RGBA) en el registro TN</span><span class="sxs-lookup"><span data-stu-id="75146-132">// The first instruction loads the texture color (RGBA) into register tn</span></span>  
<span data-ttu-id="75146-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="75146-133">tex tn</span></span>  
<span data-ttu-id="75146-134">La segunda instrucción reasigna el color</span><span class="sxs-lookup"><span data-stu-id="75146-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="75146-135">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> mediante t (n)<sub>RGB</sub> como coordenadas</span><span class="sxs-lookup"><span data-stu-id="75146-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>RGB</sub> as coordinates</span></span>
</dl>

## <a name="related-topics"></a><span data-ttu-id="75146-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75146-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75146-137">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="75146-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




