---
title: Registro de coordenadas de textura (referencia de PS de HLSL)
description: Registro de entrada del sombreador de píxeles que contiene coordenadas de textura.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104983915"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a><span data-ttu-id="0d8d2-103">Registro de coordenadas de textura (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d8d2-103">Texture coordinate register (HLSL PS reference)</span></span>

<span data-ttu-id="0d8d2-104">Registro de entrada del sombreador de píxeles que contiene coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-104">Pixel shader input register containing texture coordinates.</span></span>



| <span data-ttu-id="0d8d2-105">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="0d8d2-105">Pixel shader versions</span></span>       | <span data-ttu-id="0d8d2-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="0d8d2-106">1\_1</span></span> | <span data-ttu-id="0d8d2-107">1\_2</span><span class="sxs-lookup"><span data-stu-id="0d8d2-107">1\_2</span></span> | <span data-ttu-id="0d8d2-108">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0d8d2-108">1\_3</span></span> | <span data-ttu-id="0d8d2-109">1\_4</span><span class="sxs-lookup"><span data-stu-id="0d8d2-109">1\_4</span></span> | <span data-ttu-id="0d8d2-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0d8d2-110">2\_0</span></span> | <span data-ttu-id="0d8d2-111">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0d8d2-111">2\_sw</span></span> | <span data-ttu-id="0d8d2-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0d8d2-112">2\_x</span></span> | <span data-ttu-id="0d8d2-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0d8d2-113">3\_0</span></span> | <span data-ttu-id="0d8d2-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0d8d2-114">3\_sw</span></span> |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="0d8d2-115">Registro de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="0d8d2-115">Texture Coordinate Register</span></span> |      |      |      |      | <span data-ttu-id="0d8d2-116">x</span><span class="sxs-lookup"><span data-stu-id="0d8d2-116">x</span></span>    | <span data-ttu-id="0d8d2-117">x</span><span class="sxs-lookup"><span data-stu-id="0d8d2-117">x</span></span>     | <span data-ttu-id="0d8d2-118">x</span><span class="sxs-lookup"><span data-stu-id="0d8d2-118">x</span></span>    | <span data-ttu-id="0d8d2-119">x</span><span class="sxs-lookup"><span data-stu-id="0d8d2-119">x</span></span>    | <span data-ttu-id="0d8d2-120">x</span><span class="sxs-lookup"><span data-stu-id="0d8d2-120">x</span></span>     |



 

<span data-ttu-id="0d8d2-121">Un registro de coordenadas de textura contiene datos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-121">A texture coordinate register contains texture coordinate data.</span></span> <span data-ttu-id="0d8d2-122">Antes de utilizar un registro de coordenadas de textura, se debe declarar mediante una declaración de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-122">Before a texture coordinate register is used, it must be declared by a pixel shader declaration.</span></span> <span data-ttu-id="0d8d2-123">Para obtener más información sobre cómo declarar un registro de textura, consulte [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="0d8d2-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span></span>

<span data-ttu-id="0d8d2-124">Además, estas son otras propiedades de los registros de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-124">In addition, here are some other properties of texture coordinate registers.</span></span>

-   <span data-ttu-id="0d8d2-125">Hay ocho registros de coordenadas de textura del sombreador de píxeles, T0 a T7.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-125">There are eight pixel-shader texture coordinate registers, t0 to t7.</span></span>
-   <span data-ttu-id="0d8d2-126">Se trata de registros de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-126">These are read-only registers.</span></span>
-   <span data-ttu-id="0d8d2-127">Contienen valores RGBA de cuatro componentes que se iteran desde los vértices de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-127">They contain four-component RGBA values iterated from input vertices.</span></span>
-   <span data-ttu-id="0d8d2-128">Contienen valores de datos de rango dinámico alto y alta precisión interpolados a partir de los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-128">They contain high precision, high dynamic range data values interpolated from the vertex data.</span></span> <span data-ttu-id="0d8d2-129">Los valores se generan con la interpolación correcta de la perspectiva.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-129">Values are generated with perspective-correct interpolation.</span></span> <span data-ttu-id="0d8d2-130">Los datos son una precisión de punto flotante y están firmados.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-130">Data is floating-point precision, and is signed.</span></span>
-   <span data-ttu-id="0d8d2-131">Hay un máximo de uno en una sola instrucción.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-131">There is a maximum of one in a single instruction.</span></span>
-   <span data-ttu-id="0d8d2-132">Varias lecturas de un registro de coordenadas de textura dentro de un sombreador deben usar la misma [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="0d8d2-132">Multiple reads of a texture coordinate register within a shader must use identical [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="0d8d2-133">El modificador de precisión parcial opcional \[ \_ PP \] se aplica a las lecturas dependientes.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-133">The optional partial precision modifier \[\_pp\] applies to dependent reads.</span></span> <span data-ttu-id="0d8d2-134">Esto se debe a que la precisión parcial afecta a las operaciones aritméticas que implican el registro de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-134">This is because partial precision affects arithmetic operations involving the texture coordinate register.</span></span> <span data-ttu-id="0d8d2-135">No afectará a la precisión de las instrucciones de dirección de textura, ya que no afecta a los iteradores de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d2-135">It will not affect the precision of texture address instructions because it does not affect the texture coordinate iterators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d8d2-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d8d2-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d8d2-137">Registra</span><span class="sxs-lookup"><span data-stu-id="0d8d2-137">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




