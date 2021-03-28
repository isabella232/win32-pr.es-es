---
title: defi-vs
description: Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533393"
---
# <a name="defi---vs"></a><span data-ttu-id="5b6b1-103">defi-vs</span><span class="sxs-lookup"><span data-stu-id="5b6b1-103">defi - vs</span></span>

<span data-ttu-id="5b6b1-104">Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-104">Defines an integer constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b6b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b6b1-105">Syntax</span></span>



| <span data-ttu-id="5b6b1-106">defi DST, integerValue0, integerValue1, integerValue2, integerValue3</span><span class="sxs-lookup"><span data-stu-id="5b6b1-106">defi dst, integerValue0, integerValue1, integerValue2, integerValue3</span></span> |
|----------------------------------------------------------------------|



 

-   <span data-ttu-id="5b6b1-107">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-107">dst is the destination register.</span></span>
-   <span data-ttu-id="5b6b1-108">integerValue \# es un valor entero constante.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-108">integerValue\# is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b6b1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b6b1-109">Remarks</span></span>



| <span data-ttu-id="5b6b1-110">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5b6b1-110">Vertex shader versions</span></span> | <span data-ttu-id="5b6b1-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b6b1-111">1\_1</span></span> | <span data-ttu-id="5b6b1-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b6b1-112">2\_0</span></span> | <span data-ttu-id="5b6b1-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b6b1-113">2\_x</span></span> | <span data-ttu-id="5b6b1-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b6b1-114">2\_sw</span></span> | <span data-ttu-id="5b6b1-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b6b1-115">3\_0</span></span> | <span data-ttu-id="5b6b1-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b6b1-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5b6b1-117">defi</span><span class="sxs-lookup"><span data-stu-id="5b6b1-117">defi</span></span>                   |      | <span data-ttu-id="5b6b1-118">x</span><span class="sxs-lookup"><span data-stu-id="5b6b1-118">x</span></span>    | <span data-ttu-id="5b6b1-119">x</span><span class="sxs-lookup"><span data-stu-id="5b6b1-119">x</span></span>    | <span data-ttu-id="5b6b1-120">x</span><span class="sxs-lookup"><span data-stu-id="5b6b1-120">x</span></span>     | <span data-ttu-id="5b6b1-121">x</span><span class="sxs-lookup"><span data-stu-id="5b6b1-121">x</span></span>    | <span data-ttu-id="5b6b1-122">x</span><span class="sxs-lookup"><span data-stu-id="5b6b1-122">x</span></span>     |



 

<span data-ttu-id="5b6b1-123">La instrucción defi define una constante de sombreador de enteros cuyo valor se carga cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-123">The defi instruction defines an integer shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="5b6b1-124">Se denominan constantes inmediatas.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-124">These are called immediate constants.</span></span> <span data-ttu-id="5b6b1-125">Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetVertexShaderConstantI.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-125">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantI.</span></span>

<span data-ttu-id="5b6b1-126">Hay dos maneras de establecer una constante de tipo entero en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-126">There are two ways to set an integer constant in a shader.</span></span>

1.  <span data-ttu-id="5b6b1-127">Use defi para definir el vector de constante entero directamente dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-127">Use defi to define the integer constant vector directly inside a shader.</span></span>
2.  <span data-ttu-id="5b6b1-128">Use los métodos de la API para establecer una constante.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-128">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="5b6b1-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) para establecer una constante de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="5b6b1-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b6b1-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b6b1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b6b1-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5b6b1-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="5b6b1-132">DEF-vs</span><span class="sxs-lookup"><span data-stu-id="5b6b1-132">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="5b6b1-133">defb-vs</span><span class="sxs-lookup"><span data-stu-id="5b6b1-133">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 