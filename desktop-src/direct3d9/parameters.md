---
description: Los parámetros son variables de efecto.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parámetros (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152690"
---
# <a name="parameters-direct3d-9"></a><span data-ttu-id="396c5-103">Parámetros (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="396c5-103">Parameters (Direct3D 9)</span></span>

<span data-ttu-id="396c5-104">Los parámetros son variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="396c5-104">Parameters are effect variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="396c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="396c5-105">Syntax</span></span>

<span data-ttu-id="396c5-106">*ID. de tipo de uso* \[ : expresión *semántica* \] \[ < *(s)* > \] \[ =   \] ;</span><span class="sxs-lookup"><span data-stu-id="396c5-106">*usage type ID* \[: *semantic*\] \[<*annotation(s)*>\] \[= *expression*\];</span></span>

<span data-ttu-id="396c5-107">Los parámetros se pueden leer y escribir en la aplicación con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="396c5-107">Parameters can be read from and written to by the application with [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>

<span data-ttu-id="396c5-108">Se puede hacer referencia a los parámetros en funciones y en técnicas (concretamente, en el lado derecho de las asignaciones de estado).</span><span class="sxs-lookup"><span data-stu-id="396c5-108">Parameters can be referenced in functions and in techniques (specifically, in the right side of state assignments).</span></span>



| <span data-ttu-id="396c5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="396c5-109">Item</span></span>                                                                                 | <span data-ttu-id="396c5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="396c5-110">Description</span></span>                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="396c5-111"><span id="usage"></span><span id="USAGE"></span>*uso*</span><span class="sxs-lookup"><span data-stu-id="396c5-111"><span id="usage"></span><span id="USAGE"></span>*usage*</span></span><br/>                   | <span data-ttu-id="396c5-112">Ámbito del parámetro.</span><span class="sxs-lookup"><span data-stu-id="396c5-112">Scope of the parameter.</span></span> <span data-ttu-id="396c5-113">Vea [usos y literales (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="396c5-113">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span><br/>                                                             |
| <span data-ttu-id="396c5-114"><span id="type"></span><span id="TYPE"></span>*automáticamente*</span><span class="sxs-lookup"><span data-stu-id="396c5-114"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                      | <span data-ttu-id="396c5-115">Cualquier [referencia válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) el tipo HLSL.</span><span class="sxs-lookup"><span data-stu-id="396c5-115">Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span><br/>                                                                        |
| <span data-ttu-id="396c5-116"><span id="ID"></span><span id="id"></span>*SESIÓN*</span><span class="sxs-lookup"><span data-stu-id="396c5-116"><span id="ID"></span><span id="id"></span>*ID*</span></span><br/>                            | <span data-ttu-id="396c5-117">Un nombre único.</span><span class="sxs-lookup"><span data-stu-id="396c5-117">A unique name.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="396c5-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semántica*</span><span class="sxs-lookup"><span data-stu-id="396c5-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantic*</span></span><br/>          | <span data-ttu-id="396c5-119">Una etiqueta que sigue las reglas de identificador que normalmente indica el uso del parámetro.</span><span class="sxs-lookup"><span data-stu-id="396c5-119">A tag following identifier rules that typically indicates the usage of the parameter.</span></span> <span data-ttu-id="396c5-120">Debe ser un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="396c5-120">Must be a particular type.</span></span><br/>                                     |
| <span data-ttu-id="396c5-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*anotaciones*</span><span class="sxs-lookup"><span data-stu-id="396c5-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span></span><br/> | <span data-ttu-id="396c5-122">Cero o más partes de la información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="396c5-122">Zero or more pieces of user-specific information.</span></span> <span data-ttu-id="396c5-123">Puede ser cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="396c5-123">May be any type.</span></span> <span data-ttu-id="396c5-124">Consulte [Agregar información a los parámetros de efectos con anotaciones](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="396c5-124">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/> |
| <span data-ttu-id="396c5-125"><span id="expression"></span><span id="EXPRESSION"></span>*Expresiones*</span><span class="sxs-lookup"><span data-stu-id="396c5-125"><span id="expression"></span><span id="EXPRESSION"></span>*expression*</span></span><br/>    | <span data-ttu-id="396c5-126">Inicializa el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="396c5-126">Initializes the parameter's value.</span></span> <span data-ttu-id="396c5-127">Vea [expresiones (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="396c5-127">See [Expressions (Direct3D 9)](expressions.md).</span></span><br/>                                                                  |



 

<span data-ttu-id="396c5-128">Los parámetros se pueden inicializar en cualquier [referencia válida de](../direct3dhlsl/dx-graphics-hlsl-reference.md) la expresión HLSL que se reduzca a un valor literal.</span><span class="sxs-lookup"><span data-stu-id="396c5-128">Parameters can be initialized to any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) expression that reduces to a literal value.</span></span>

<span data-ttu-id="396c5-129">Los valores de parámetro no cambian en la ejecución de las llamadas de función o de asignación de estado.</span><span class="sxs-lookup"><span data-stu-id="396c5-129">Parameter values are not changed by the execution of state assignment or function calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="396c5-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="396c5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="396c5-131">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="396c5-131">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
