---
title: Constantes de D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Estas constantes dirigen el modo en que el compilador compila un archivo de efectos o el modo en que el tiempo de ejecución procesa el archivo de efecto.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986796"
---
# <a name="d3dcompile_effect-constants"></a><span data-ttu-id="20470-103">Constantes de efecto de D3DCOMPILE \_</span><span class="sxs-lookup"><span data-stu-id="20470-103">D3DCOMPILE\_EFFECT Constants</span></span>

<span data-ttu-id="20470-104">Estas constantes dirigen el modo en que el compilador compila un archivo de efectos o el modo en que el tiempo de ejecución procesa el archivo de efecto.</span><span class="sxs-lookup"><span data-stu-id="20470-104">These constants direct how the compiler compiles an effect file or how the runtime processes the effect file.</span></span>

<dl> <dt>

<span data-ttu-id="20470-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_ \_ Efecto secundario del efecto de D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="20470-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE\_EFFECT\_CHILD\_EFFECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20470-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="20470-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="20470-107">Compilar el archivo de efectos (. FX) en un efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="20470-107">Compile the effects (.fx) file to a child effect.</span></span> <span data-ttu-id="20470-108">Los efectos secundarios no tienen inicializadores para los valores compartidos porque estos efectos secundarios se inicializan en el efecto maestro (el grupo de efectos).</span><span class="sxs-lookup"><span data-stu-id="20470-108">Child effects have no initializers for any shared values because these child effects are initialized in the master effect (the effect pool).</span></span>

> [!Note]  
> <span data-ttu-id="20470-109">Los grupos de efectos son compatibles con los efectos 10 (FX10), pero no con los efectos 11 (FX11).</span><span class="sxs-lookup"><span data-stu-id="20470-109">Effect pools are supported by Effects 10 (FX10) but not by Effects 11 (FX11).</span></span> <span data-ttu-id="20470-110">Para obtener más información sobre las diferencias entre los grupos de efectos de Direct3D 10 y los grupos de efectos en Direct3D 11, consulte grupos de [efectos y grupos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span><span class="sxs-lookup"><span data-stu-id="20470-110">For more info about differences between effect pools in Direct3D 10 and effect groups in Direct3D 11, see [Effect Pools and Groups](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="20470-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ efecto \_ permitir \_ operaciones lentas \_**</span><span class="sxs-lookup"><span data-stu-id="20470-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE\_EFFECT\_ALLOW\_SLOW\_OPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20470-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="20470-112">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="20470-113">Deshabilita el modo de rendimiento y permite objetos de estado mutables.</span><span class="sxs-lookup"><span data-stu-id="20470-113">Disables performance mode and allows for mutable state objects.</span></span>

<span data-ttu-id="20470-114">De forma predeterminada, el modo de rendimiento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="20470-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="20470-115">El modo de rendimiento no permite objetos de estado mutable impidiendo que las expresiones no literales aparezcan en las definiciones de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="20470-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20470-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20470-116">Requirements</span></span>



| <span data-ttu-id="20470-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="20470-117">Requirement</span></span> | <span data-ttu-id="20470-118">Value</span><span class="sxs-lookup"><span data-stu-id="20470-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20470-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20470-119">Header</span></span><br/> | <dl> <span data-ttu-id="20470-120"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="20470-120"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20470-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="20470-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20470-122">Constantes de D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="20470-122">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

