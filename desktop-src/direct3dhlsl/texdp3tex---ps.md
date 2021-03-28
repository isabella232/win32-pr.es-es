---
title: texdp3tex-PS
description: Realiza un producto de tres componentes y usa el resultado para realizar una búsqueda de texturas 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996856"
---
# <a name="texdp3tex---ps"></a><span data-ttu-id="9f5ed-103">texdp3tex-PS</span><span class="sxs-lookup"><span data-stu-id="9f5ed-103">texdp3tex - ps</span></span>

<span data-ttu-id="9f5ed-104">Realiza un producto de tres componentes y usa el resultado para realizar una búsqueda de texturas 1D.</span><span class="sxs-lookup"><span data-stu-id="9f5ed-104">Performs a three-component dot product and uses the result to do a 1D texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f5ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f5ed-105">Syntax</span></span>



| <span data-ttu-id="9f5ed-106">texdp3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="9f5ed-106">texdp3tex dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="9f5ed-107">, donde</span><span class="sxs-lookup"><span data-stu-id="9f5ed-107">where</span></span>

-   <span data-ttu-id="9f5ed-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9f5ed-108">dst is the destination register.</span></span>
-   <span data-ttu-id="9f5ed-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="9f5ed-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f5ed-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f5ed-110">Remarks</span></span>



| <span data-ttu-id="9f5ed-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9f5ed-111">Pixel shader versions</span></span> | <span data-ttu-id="9f5ed-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="9f5ed-112">1\_1</span></span> | <span data-ttu-id="9f5ed-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="9f5ed-113">1\_2</span></span> | <span data-ttu-id="9f5ed-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9f5ed-114">1\_3</span></span> | <span data-ttu-id="9f5ed-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="9f5ed-115">1\_4</span></span> | <span data-ttu-id="9f5ed-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f5ed-116">2\_0</span></span> | <span data-ttu-id="9f5ed-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9f5ed-117">2\_x</span></span> | <span data-ttu-id="9f5ed-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9f5ed-118">2\_sw</span></span> | <span data-ttu-id="9f5ed-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f5ed-119">3\_0</span></span> | <span data-ttu-id="9f5ed-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9f5ed-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9f5ed-121">texdp3tex</span><span class="sxs-lookup"><span data-stu-id="9f5ed-121">texdp3tex</span></span>             |      | <span data-ttu-id="9f5ed-122">x</span><span class="sxs-lookup"><span data-stu-id="9f5ed-122">x</span></span>    | <span data-ttu-id="9f5ed-123">x</span><span class="sxs-lookup"><span data-stu-id="9f5ed-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="9f5ed-124">Los registros de texturas deben usar la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="9f5ed-124">Texture registers must use the following sequence.</span></span>


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



<span data-ttu-id="9f5ed-125">Aquí encontrará más detalles sobre cómo se realiza la búsqueda de productos y texturas de punto.</span><span class="sxs-lookup"><span data-stu-id="9f5ed-125">Here is more detail about how the dot product and texture lookup are done.</span></span>

<span data-ttu-id="9f5ed-126">La instrucción texdp3tex realiza un producto de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="9f5ed-126">The texdp3tex instruction performs a three-component dot product.</span></span>

<span data-ttu-id="9f5ed-127">u ' = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="9f5ed-127">u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="9f5ed-128">El resultado se usa para el muestreo de la textura en la fase de textura m mediante la realización de una búsqueda 1D.</span><span class="sxs-lookup"><span data-stu-id="9f5ed-128">The result is used to sample the texture at texture stage m by performing a 1D lookup.</span></span>

<span data-ttu-id="9f5ed-129">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> mediante (u ', 0,0) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="9f5ed-129">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f5ed-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f5ed-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f5ed-131">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9f5ed-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




