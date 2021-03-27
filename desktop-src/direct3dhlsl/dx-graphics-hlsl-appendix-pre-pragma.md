---
title: " pragma (Directiva)"
description: Directiva de preprocesador que proporciona características específicas del equipo o del sistema operativo, a la vez que conserva la compatibilidad total con los lenguajes C y C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- Directiva pragma HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076746"
---
# <a name="pragma-directive"></a><span data-ttu-id="41d3e-104">\#pragma (Directiva)</span><span class="sxs-lookup"><span data-stu-id="41d3e-104">\#pragma Directive</span></span>

<span data-ttu-id="41d3e-105">Directiva de preprocesador que proporciona características específicas del equipo o del sistema operativo, a la vez que conserva la compatibilidad total con los lenguajes C y C++.</span><span class="sxs-lookup"><span data-stu-id="41d3e-105">Preprocessor directive that provides machine-specific or operating system-specific features while retaining overall compatibility with the C and C++ languages.</span></span>



| <span data-ttu-id="41d3e-106">\#*cadena de token de* pragma</span><span class="sxs-lookup"><span data-stu-id="41d3e-106">\#pragma *token-string*</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="41d3e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41d3e-107">Parameters</span></span>



| <span data-ttu-id="41d3e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="41d3e-108">Item</span></span>                                                                                    | <span data-ttu-id="41d3e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="41d3e-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41d3e-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-cadena*</span><span class="sxs-lookup"><span data-stu-id="41d3e-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="41d3e-111">Serie de caracteres que proporciona una instrucción de compilador y argumentos concretos.</span><span class="sxs-lookup"><span data-stu-id="41d3e-111">Series of characters that gives a specific compiler instruction and arguments.</span></span> <span data-ttu-id="41d3e-112">Este parámetro está sujeto a la expansión de macros.</span><span class="sxs-lookup"><span data-stu-id="41d3e-112">This parameter is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="41d3e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41d3e-113">Remarks</span></span>

<span data-ttu-id="41d3e-114">Si el compilador encuentra una directiva pragma que no reconoce, emite una advertencia, pero la compilación continúa.</span><span class="sxs-lookup"><span data-stu-id="41d3e-114">If the compiler finds a pragma it does not recognize, it issues a warning, but compilation continues.</span></span>

<span data-ttu-id="41d3e-115">El compilador de HLSL reconoce las siguientes pragmas:</span><span class="sxs-lookup"><span data-stu-id="41d3e-115">The HLSL compiler recognizes the following pragmas:</span></span>

-   [<span data-ttu-id="41d3e-116">Def</span><span class="sxs-lookup"><span data-stu-id="41d3e-116">def</span></span>](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [<span data-ttu-id="41d3e-117">message</span><span class="sxs-lookup"><span data-stu-id="41d3e-117">message</span></span>](message-pragma-directive--directx-hlsl-.md)
-   [<span data-ttu-id="41d3e-118">matriz de paquetes \_</span><span class="sxs-lookup"><span data-stu-id="41d3e-118">pack\_matrix</span></span>](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [<span data-ttu-id="41d3e-119">warning</span><span class="sxs-lookup"><span data-stu-id="41d3e-119">warning</span></span>](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a><span data-ttu-id="41d3e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="41d3e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d3e-121">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41d3e-121">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





