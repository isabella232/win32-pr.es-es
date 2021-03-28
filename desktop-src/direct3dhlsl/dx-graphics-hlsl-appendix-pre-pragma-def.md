---
title: Directiva pragma Def
description: Directiva pragma que asigna manualmente un registro de sombreador de punto flotante.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Directiva pragma Def
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996824"
---
# <a name="def-pragma-directive"></a><span data-ttu-id="f95cd-104">Directiva pragma Def</span><span class="sxs-lookup"><span data-stu-id="f95cd-104">def pragma Directive</span></span>

<span data-ttu-id="f95cd-105">Directiva pragma que asigna manualmente un registro de sombreador de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f95cd-105">Pragma directive that manually allocates a floating-point shader register.</span></span>



| <span data-ttu-id="f95cd-106">\#pragma DEF ( *destino*, *registro*, *val1*, *val2*,*val3*, *val4* )</span><span class="sxs-lookup"><span data-stu-id="f95cd-106">\#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* )</span></span> |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f95cd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f95cd-107">Parameters</span></span>



| <span data-ttu-id="f95cd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f95cd-108">Item</span></span>                                                                        | <span data-ttu-id="f95cd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f95cd-109">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f95cd-110"><span id="target"></span><span id="TARGET"></span>*dirigir*</span><span class="sxs-lookup"><span data-stu-id="f95cd-110"><span id="target"></span><span id="TARGET"></span>*target*</span></span><br/>       | <span data-ttu-id="f95cd-111">Destino que contiene el registro que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="f95cd-111">Target that contains the register to allocate.</span></span> <br/>                  |
| <span data-ttu-id="f95cd-112"><span id="register"></span><span id="REGISTER"></span>*el*</span><span class="sxs-lookup"><span data-stu-id="f95cd-112"><span id="register"></span><span id="REGISTER"></span>*register*</span></span><br/> | <span data-ttu-id="f95cd-113">Registro del sombreador de punto flotante que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="f95cd-113">Floating-point shader register to allocate.</span></span> <br/>                     |
| <span data-ttu-id="f95cd-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span><span class="sxs-lookup"><span data-stu-id="f95cd-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span></span><br/>             | <span data-ttu-id="f95cd-115">Primer byte del valor que se va a asignar al registro especificado.</span><span class="sxs-lookup"><span data-stu-id="f95cd-115">First byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="f95cd-116"><span id="val1"></span><span id="VAL1"></span>*valor1*</span><span class="sxs-lookup"><span data-stu-id="f95cd-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span></span><br/>             | <span data-ttu-id="f95cd-117">Segundo byte del valor que se va a asignar al registro especificado.</span><span class="sxs-lookup"><span data-stu-id="f95cd-117">Second byte of the value to allocate to the specified register.</span></span> <br/> |
| <span data-ttu-id="f95cd-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span><span class="sxs-lookup"><span data-stu-id="f95cd-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span></span><br/>             | <span data-ttu-id="f95cd-119">Tercer byte del valor que se va a asignar al registro especificado.</span><span class="sxs-lookup"><span data-stu-id="f95cd-119">Third byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="f95cd-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span><span class="sxs-lookup"><span data-stu-id="f95cd-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span></span><br/>             | <span data-ttu-id="f95cd-121">Cuarto byte del valor que se va a asignar al registro especificado.</span><span class="sxs-lookup"><span data-stu-id="f95cd-121">Fourth byte of the value to allocate to the specified register.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f95cd-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f95cd-122">Remarks</span></span>

<span data-ttu-id="f95cd-123">La pragma Def permite a un desarrollador rellenar previamente un registro de sombreador de punto flotante con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="f95cd-123">The def pragma allows a developer to prefill a floating-point shader register with the specified value.</span></span> <span data-ttu-id="f95cd-124">Esta pragma se usa con poca frecuencia.</span><span class="sxs-lookup"><span data-stu-id="f95cd-124">This pragma is infrequently used.</span></span>

## <a name="see-also"></a><span data-ttu-id="f95cd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f95cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95cd-126">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f95cd-126">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="f95cd-127">\#pragma (Directiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f95cd-127">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





