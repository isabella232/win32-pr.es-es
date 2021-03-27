---
title: texreg2ar-PS
description: Interpreta los componentes de color alfa y rojo del registro de origen como datos de dirección de textura (u, v) para muestrear la textura en la fase correspondiente al número de registro de destino. El resultado se almacena en el registro de destino.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487890"
---
# <a name="texreg2ar---ps"></a><span data-ttu-id="37c99-104">texreg2ar-PS</span><span class="sxs-lookup"><span data-stu-id="37c99-104">texreg2ar - ps</span></span>

<span data-ttu-id="37c99-105">Interpreta los componentes de color alfa y rojo del registro de origen como datos de dirección de textura (u, v) para muestrear la textura en la fase correspondiente al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="37c99-105">Interprets the alpha and red color components of the source register as texture address data (u,v) to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="37c99-106">El resultado se almacena en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="37c99-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c99-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37c99-107">Syntax</span></span>



| <span data-ttu-id="37c99-108">texreg2ar DST, src</span><span class="sxs-lookup"><span data-stu-id="37c99-108">texreg2ar dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="37c99-109">, donde</span><span class="sxs-lookup"><span data-stu-id="37c99-109">where</span></span>

-   <span data-ttu-id="37c99-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="37c99-110">dst is the destination register.</span></span>
-   <span data-ttu-id="37c99-111">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="37c99-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="37c99-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37c99-112">Remarks</span></span>



| <span data-ttu-id="37c99-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="37c99-113">Pixel shader versions</span></span> | <span data-ttu-id="37c99-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="37c99-114">1\_1</span></span> | <span data-ttu-id="37c99-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="37c99-115">1\_2</span></span> | <span data-ttu-id="37c99-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="37c99-116">1\_3</span></span> | <span data-ttu-id="37c99-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="37c99-117">1\_4</span></span> | <span data-ttu-id="37c99-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37c99-118">2\_0</span></span> | <span data-ttu-id="37c99-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="37c99-119">2\_x</span></span> | <span data-ttu-id="37c99-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37c99-120">2\_sw</span></span> | <span data-ttu-id="37c99-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37c99-121">3\_0</span></span> | <span data-ttu-id="37c99-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37c99-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="37c99-123">texreg2ar</span><span class="sxs-lookup"><span data-stu-id="37c99-123">texreg2ar</span></span>             | <span data-ttu-id="37c99-124">x</span><span class="sxs-lookup"><span data-stu-id="37c99-124">x</span></span>    | <span data-ttu-id="37c99-125">x</span><span class="sxs-lookup"><span data-stu-id="37c99-125">x</span></span>    | <span data-ttu-id="37c99-126">x</span><span class="sxs-lookup"><span data-stu-id="37c99-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="37c99-127">Esta instrucción es útil para las operaciones de reasignación de espacio de color.</span><span class="sxs-lookup"><span data-stu-id="37c99-127">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="37c99-128">Este es un ejemplo de la secuencia que sigue la instrucción:</span><span class="sxs-lookup"><span data-stu-id="37c99-128">Here is an example of the sequence the instruction follows:</span></span>

<dl> <span data-ttu-id="37c99-129">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="37c99-129">tex t(n)</span></span>  
<span data-ttu-id="37c99-130">texreg2ar t (m), t (n), donde m > n</span><span class="sxs-lookup"><span data-stu-id="37c99-130">texreg2ar t(m), t(n) where m > n</span></span>  
<span data-ttu-id="37c99-131">La primera instrucción carga el color de la textura (RGBA)</span><span class="sxs-lookup"><span data-stu-id="37c99-131">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="37c99-132">en el registro TN</span><span class="sxs-lookup"><span data-stu-id="37c99-132">// into register tn</span></span>  
<span data-ttu-id="37c99-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="37c99-133">tex tn</span></span>  
<span data-ttu-id="37c99-134">La segunda instrucción reasigna el color</span><span class="sxs-lookup"><span data-stu-id="37c99-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="37c99-135">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> mediante t (n)<sub>ar</sub> como coordenadas</span><span class="sxs-lookup"><span data-stu-id="37c99-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="37c99-136">\_BX2 no se puede usar en la instrucción src Register para texreg2ar o [texreg2gb-PS](texreg2gb---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="37c99-136">\_bx2 cannot be used on the src register for texreg2ar or [texreg2gb - ps](texreg2gb---ps.md) instructions.</span></span>

<span data-ttu-id="37c99-137">Para esta instrucción, el registro de origen debe utilizar datos sin firmar.</span><span class="sxs-lookup"><span data-stu-id="37c99-137">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="37c99-138">El uso de datos firmados o mixtos en el registro de origen generará resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="37c99-138">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="37c99-139">Para obtener más información, vea [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="37c99-139">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="37c99-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37c99-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37c99-141">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="37c99-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 