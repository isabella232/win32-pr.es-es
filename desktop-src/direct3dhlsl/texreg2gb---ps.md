---
title: texreg2gb-PS
description: Interpreta los componentes de color verde y azul del registro de origen como datos de dirección de textura para muestrear la textura en la fase correspondiente al número de registro de destino.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984006"
---
# <a name="texreg2gb---ps"></a><span data-ttu-id="32ca7-103">texreg2gb-PS</span><span class="sxs-lookup"><span data-stu-id="32ca7-103">texreg2gb - ps</span></span>

<span data-ttu-id="32ca7-104">Interpreta los componentes de color verde y azul del registro de origen como datos de dirección de textura para muestrear la textura en la fase correspondiente al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="32ca7-104">Interprets the green and blue color components of the source register as texture address data to sample the texture at the stage corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ca7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32ca7-105">Syntax</span></span>



| <span data-ttu-id="32ca7-106">texreg2gb DST, src</span><span class="sxs-lookup"><span data-stu-id="32ca7-106">texreg2gb dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="32ca7-107">, donde</span><span class="sxs-lookup"><span data-stu-id="32ca7-107">where</span></span>

-   <span data-ttu-id="32ca7-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="32ca7-108">dst is the destination register.</span></span>
-   <span data-ttu-id="32ca7-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="32ca7-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ca7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32ca7-110">Remarks</span></span>



| <span data-ttu-id="32ca7-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="32ca7-111">Pixel shader versions</span></span> | <span data-ttu-id="32ca7-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="32ca7-112">1\_1</span></span> | <span data-ttu-id="32ca7-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="32ca7-113">1\_2</span></span> | <span data-ttu-id="32ca7-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="32ca7-114">1\_3</span></span> | <span data-ttu-id="32ca7-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="32ca7-115">1\_4</span></span> | <span data-ttu-id="32ca7-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="32ca7-116">2\_0</span></span> | <span data-ttu-id="32ca7-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="32ca7-117">2\_x</span></span> | <span data-ttu-id="32ca7-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="32ca7-118">2\_sw</span></span> | <span data-ttu-id="32ca7-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="32ca7-119">3\_0</span></span> | <span data-ttu-id="32ca7-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="32ca7-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="32ca7-121">texreg2gb</span><span class="sxs-lookup"><span data-stu-id="32ca7-121">texreg2gb</span></span>             |      | <span data-ttu-id="32ca7-122">x</span><span class="sxs-lookup"><span data-stu-id="32ca7-122">x</span></span>    | <span data-ttu-id="32ca7-123">x</span><span class="sxs-lookup"><span data-stu-id="32ca7-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="32ca7-124">Esta instrucción es útil para las operaciones de reasignación de espacio de color.</span><span class="sxs-lookup"><span data-stu-id="32ca7-124">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="32ca7-125">Este es un ejemplo de la secuencia que sigue la instrucción.</span><span class="sxs-lookup"><span data-stu-id="32ca7-125">Here is an example of the sequence the instruction follows.</span></span>

<dl> <span data-ttu-id="32ca7-126">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="32ca7-126">tex t(n)</span></span>  
<span data-ttu-id="32ca7-127">texreg2gb t (m), t (n), donde m > n</span><span class="sxs-lookup"><span data-stu-id="32ca7-127">texreg2gb t(m), t(n) where m > n</span></span>  
<span data-ttu-id="32ca7-128">La primera instrucción carga el color de la textura (RGBA)</span><span class="sxs-lookup"><span data-stu-id="32ca7-128">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="32ca7-129">en el registro TN</span><span class="sxs-lookup"><span data-stu-id="32ca7-129">// into register tn</span></span>  
<span data-ttu-id="32ca7-130">Tex TN</span><span class="sxs-lookup"><span data-stu-id="32ca7-130">tex tn</span></span>  
<span data-ttu-id="32ca7-131">La segunda instrucción reasigna el color</span><span class="sxs-lookup"><span data-stu-id="32ca7-131">// The second instruction remaps the color</span></span>  
<span data-ttu-id="32ca7-132">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> mediante t (n)<sub>GB</sub> como coordenadas</span><span class="sxs-lookup"><span data-stu-id="32ca7-132">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="32ca7-133">\_no se puede usar BX2 en el registro src para instrucciones [texreg2ar-PS](texreg2ar---ps.md) o texreg2gb.</span><span class="sxs-lookup"><span data-stu-id="32ca7-133">\_bx2 cannot be used on the src register for [texreg2ar - ps](texreg2ar---ps.md) or texreg2gb instructions.</span></span>

<span data-ttu-id="32ca7-134">Para esta instrucción, el registro de origen debe utilizar datos sin firmar.</span><span class="sxs-lookup"><span data-stu-id="32ca7-134">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="32ca7-135">El uso de datos firmados o mixtos en el registro de origen generará resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="32ca7-135">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="32ca7-136">Para obtener más información, vea [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="32ca7-136">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32ca7-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32ca7-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32ca7-138">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="32ca7-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 