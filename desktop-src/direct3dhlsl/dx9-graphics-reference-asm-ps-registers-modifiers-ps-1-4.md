---
title: '\_ \_ modificadores de registro de origen de PS 1 4 para texld, texcrd'
description: Dos \_ instrucciones de dirección de textura del sombreador de píxeles versión 1 4, texld-PS \_ 1 \_ 4 y texcrd-PS, tienen una sintaxis personalizada.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "104149023"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a><span data-ttu-id="b7af8-103">\_ \_ modificadores de registro de origen de PS 1 4 para texld, texcrd</span><span class="sxs-lookup"><span data-stu-id="b7af8-103">ps\_1\_4 source register modifiers for texld, texcrd</span></span>

<span data-ttu-id="b7af8-104">Dos \_ instrucciones de dirección de textura del sombreador de píxeles versión 1 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) y [texcrd-PS](texcrd---ps.md), tienen una sintaxis personalizada.</span><span class="sxs-lookup"><span data-stu-id="b7af8-104">Two pixel shader version 1\_4 texture address instructions, [texld - ps\_1\_4](texld---ps-1-4.md) and [texcrd - ps](texcrd---ps.md), have custom syntax.</span></span> <span data-ttu-id="b7af8-105">Estas instrucciones admiten su propio conjunto de modificadores de registro de origen, selectores de registro de origen y máscaras de escritura de registro de destino, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="b7af8-105">These instructions support their own set of source register modifiers, source register selectors, and destination-register write masks, as shown here.</span></span>

## <a name="source-register-modifiers-for-texld-and-texcrd"></a><span data-ttu-id="b7af8-106">Modificadores de registro de origen para texld y texcrd</span><span class="sxs-lookup"><span data-stu-id="b7af8-106">Source Register Modifiers for texld and texcrd</span></span>

<span data-ttu-id="b7af8-107">Estos modificadores proporcionan funcionalidad de división proyectada dividiendo los valores x e y por los valores z o w.</span><span class="sxs-lookup"><span data-stu-id="b7af8-107">These modifiers provide projective divide functionality by dividing the x and y values by either the z or w values.</span></span>



| <span data-ttu-id="b7af8-108">Modificadores de registro de origen</span><span class="sxs-lookup"><span data-stu-id="b7af8-108">Source register modifiers</span></span> | <span data-ttu-id="b7af8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7af8-109">Description</span></span>                | <span data-ttu-id="b7af8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7af8-110">Syntax</span></span>       |
|---------------------------|----------------------------|--------------|
| <span data-ttu-id="b7af8-111">\_DZ</span><span class="sxs-lookup"><span data-stu-id="b7af8-111">\_dz</span></span>                      | <span data-ttu-id="b7af8-112">Dividir componentes x, y por z</span><span class="sxs-lookup"><span data-stu-id="b7af8-112">Divide x,y components by z</span></span> | <span data-ttu-id="b7af8-113">registrar \_ DZ</span><span class="sxs-lookup"><span data-stu-id="b7af8-113">register\_dz</span></span> |
| <span data-ttu-id="b7af8-114">\_db</span><span class="sxs-lookup"><span data-stu-id="b7af8-114">\_db</span></span>                      | <span data-ttu-id="b7af8-115">Dividir componentes x, y por z</span><span class="sxs-lookup"><span data-stu-id="b7af8-115">Divide x,y components by z</span></span> | <span data-ttu-id="b7af8-116">registrar \_ base de registros</span><span class="sxs-lookup"><span data-stu-id="b7af8-116">register\_db</span></span> |
| <span data-ttu-id="b7af8-117">\_almacenamiento</span><span class="sxs-lookup"><span data-stu-id="b7af8-117">\_dw</span></span>                      | <span data-ttu-id="b7af8-118">Dividir componentes x, y en w</span><span class="sxs-lookup"><span data-stu-id="b7af8-118">Divide x,y components by w</span></span> | <span data-ttu-id="b7af8-119">registrar \_ DW</span><span class="sxs-lookup"><span data-stu-id="b7af8-119">register\_dw</span></span> |
| <span data-ttu-id="b7af8-120">\_da</span><span class="sxs-lookup"><span data-stu-id="b7af8-120">\_da</span></span>                      | <span data-ttu-id="b7af8-121">Dividir componentes x, y en w</span><span class="sxs-lookup"><span data-stu-id="b7af8-121">Divide x,y components by w</span></span> | <span data-ttu-id="b7af8-122">registrar \_ da</span><span class="sxs-lookup"><span data-stu-id="b7af8-122">register\_da</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="b7af8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7af8-123">Remarks</span></span>

<span data-ttu-id="b7af8-124">El \_ \_ modificador DZ o DB hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b7af8-124">The \_dz or \_db modifier does the following:</span></span>


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



<span data-ttu-id="b7af8-125">El \_ \_ modificador DW o da hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b7af8-125">The \_dw or \_da modifier does the following:</span></span>


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a><span data-ttu-id="b7af8-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7af8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7af8-127">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b7af8-127">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




