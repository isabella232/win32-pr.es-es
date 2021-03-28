---
title: defi-PS
description: Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149492"
---
# <a name="defi---ps"></a><span data-ttu-id="2a1ee-103">defi-PS</span><span class="sxs-lookup"><span data-stu-id="2a1ee-103">defi - ps</span></span>

<span data-ttu-id="2a1ee-104">Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-104">Defines an integer constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1ee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a1ee-105">Syntax</span></span>



| <span data-ttu-id="2a1ee-106">defi DST, integerValue</span><span class="sxs-lookup"><span data-stu-id="2a1ee-106">defi dst, integerValue</span></span> |
|------------------------|



 

-   <span data-ttu-id="2a1ee-107">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-107">dst is the destination register.</span></span>
-   <span data-ttu-id="2a1ee-108">integerValue es un valor entero constante.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-108">integerValue is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a1ee-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a1ee-109">Remarks</span></span>



| <span data-ttu-id="2a1ee-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2a1ee-110">Pixel shader versions</span></span> | <span data-ttu-id="2a1ee-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="2a1ee-111">1\_1</span></span> | <span data-ttu-id="2a1ee-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="2a1ee-112">1\_2</span></span> | <span data-ttu-id="2a1ee-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2a1ee-113">1\_3</span></span> | <span data-ttu-id="2a1ee-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="2a1ee-114">1\_4</span></span> | <span data-ttu-id="2a1ee-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a1ee-115">2\_0</span></span> | <span data-ttu-id="2a1ee-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2a1ee-116">2\_x</span></span> | <span data-ttu-id="2a1ee-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2a1ee-117">2\_sw</span></span> | <span data-ttu-id="2a1ee-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a1ee-118">3\_0</span></span> | <span data-ttu-id="2a1ee-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2a1ee-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2a1ee-120">defi</span><span class="sxs-lookup"><span data-stu-id="2a1ee-120">defi</span></span>                  |      |      |      |      |      | <span data-ttu-id="2a1ee-121">x</span><span class="sxs-lookup"><span data-stu-id="2a1ee-121">x</span></span>    | <span data-ttu-id="2a1ee-122">x</span><span class="sxs-lookup"><span data-stu-id="2a1ee-122">x</span></span>     | <span data-ttu-id="2a1ee-123">x</span><span class="sxs-lookup"><span data-stu-id="2a1ee-123">x</span></span>    | <span data-ttu-id="2a1ee-124">x</span><span class="sxs-lookup"><span data-stu-id="2a1ee-124">x</span></span>     |



 

<span data-ttu-id="2a1ee-125">La instrucción defi define una constante de sombreador cuyo valor se carga cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-125">The defi instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="2a1ee-126">Se denominan constantes inmediatas.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-126">These are called immediate constants.</span></span> <span data-ttu-id="2a1ee-127">Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-127">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="2a1ee-128">Hay dos maneras de establecer una constante en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="2a1ee-129">Use defi para definir la constante directamente dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-129">Use defi to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="2a1ee-130">Use los métodos de la API para establecer una constante.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-130">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="2a1ee-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para establecer una constante booleana.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>
    -   <span data-ttu-id="2a1ee-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) para establecer una constante de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) to set a floating-point constant.</span></span>
    -   <span data-ttu-id="2a1ee-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) para establecer una constante de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="2a1ee-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a1ee-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a1ee-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a1ee-135">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2a1ee-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 