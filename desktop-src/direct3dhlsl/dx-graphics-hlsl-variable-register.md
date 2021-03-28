---
title: registro
description: registro
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- registro de HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420744"
---
# <a name="register"></a><span data-ttu-id="3e412-104">registro</span><span class="sxs-lookup"><span data-stu-id="3e412-104">register</span></span>

<span data-ttu-id="3e412-105">Palabra clave opcional para asignar una variable de sombreador a un registro determinado, que usa la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e412-105">Optional keyword for assigning a shader variable to a particular register, which uses the following syntax:</span></span>



| <span data-ttu-id="3e412-106">: Register ( *\[ \_ perfil \] de sombreador*, \* \# \[ subcomponente \] de tipo\* )</span><span class="sxs-lookup"><span data-stu-id="3e412-106">: register ( *\[shader\_profile\]*, *Type\#\[subcomponent\]* )</span></span> |
|----------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3e412-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e412-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e412-108"><span id="register"></span><span id="REGISTER"></span>el</span><span class="sxs-lookup"><span data-stu-id="3e412-108"><span id="register"></span><span id="REGISTER"></span>register</span></span>
</dt> <dd>

<span data-ttu-id="3e412-109">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="3e412-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="3e412-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Perfil de sombreador \_\]*</span><span class="sxs-lookup"><span data-stu-id="3e412-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[shader\_profile\]*</span></span>
</dt> <dd>

<span data-ttu-id="3e412-111">[Perfil de sombreador](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)opcional, que puede ser un destino de sombreador o simplemente **PS** o **vs**.</span><span class="sxs-lookup"><span data-stu-id="3e412-111">Optional [shader profile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), which can be a shader target or simply **ps** or **vs**.</span></span>

</dd> <dt>

<span data-ttu-id="3e412-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Subcomponente de tipo \# \[\]*</span><span class="sxs-lookup"><span data-stu-id="3e412-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Type\#\[subcomponent\]*</span></span>
</dt> <dd>

<span data-ttu-id="3e412-113">Registra el tipo, el número y la declaración del subcomponente.</span><span class="sxs-lookup"><span data-stu-id="3e412-113">Register type, number, and subcomponent declaration.</span></span>

-   <span data-ttu-id="3e412-114">El tipo es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3e412-114">Type is one of the following:</span></span>

    

    | <span data-ttu-id="3e412-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e412-115">Type</span></span> | <span data-ttu-id="3e412-116">Descripción del registro</span><span class="sxs-lookup"><span data-stu-id="3e412-116">Register Description</span></span>       |
    |------|----------------------------|
    | <span data-ttu-id="3e412-117">b</span><span class="sxs-lookup"><span data-stu-id="3e412-117">b</span></span>    | <span data-ttu-id="3e412-118">Búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="3e412-118">Constant buffer</span></span>            |
    | <span data-ttu-id="3e412-119">t</span><span class="sxs-lookup"><span data-stu-id="3e412-119">t</span></span>    | <span data-ttu-id="3e412-120">Búfer de textura y textura</span><span class="sxs-lookup"><span data-stu-id="3e412-120">Texture and texture buffer</span></span> |
    | <span data-ttu-id="3e412-121">c</span><span class="sxs-lookup"><span data-stu-id="3e412-121">c</span></span>    | <span data-ttu-id="3e412-122">Desplazamiento de búfer</span><span class="sxs-lookup"><span data-stu-id="3e412-122">Buffer offset</span></span>              |
    | <span data-ttu-id="3e412-123">s</span><span class="sxs-lookup"><span data-stu-id="3e412-123">s</span></span>    | <span data-ttu-id="3e412-124">Muestra</span><span class="sxs-lookup"><span data-stu-id="3e412-124">Sampler</span></span>                    |
    | <span data-ttu-id="3e412-125">u</span><span class="sxs-lookup"><span data-stu-id="3e412-125">u</span></span>    | <span data-ttu-id="3e412-126">Vista de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="3e412-126">Unordered Access View</span></span>      |

    

     

-   <span data-ttu-id="3e412-127">*\#* es el número de registro, que es un número entero.</span><span class="sxs-lookup"><span data-stu-id="3e412-127">*\#* is the register number, which is an integer number.</span></span>
-   <span data-ttu-id="3e412-128">El *subcomponente* es un número entero opcional.</span><span class="sxs-lookup"><span data-stu-id="3e412-128">The *subcomponent* is an optional integer number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e412-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e412-129">Remarks</span></span>

<span data-ttu-id="3e412-130">Puede Agregar una o varias asignaciones de registro a la misma declaración de variable, separadas por espacios.</span><span class="sxs-lookup"><span data-stu-id="3e412-130">You may add one or more register assignments to the same variable declaration, separated by spaces.</span></span>

<span data-ttu-id="3e412-131">En el caso de las variables de Direct3D 10 en el ámbito global, la palabra clave **Register** actúa igual que la palabra clave [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="3e412-131">For Direct3D 10 variables in global scope, the **register** keyword acts the same as the [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="3e412-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3e412-132">Examples</span></span>

<span data-ttu-id="3e412-133">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="3e412-133">Here are some examples:</span></span>


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a><span data-ttu-id="3e412-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e412-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e412-135">Sintaxis de variables</span><span class="sxs-lookup"><span data-stu-id="3e412-135">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="3e412-136">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e412-136">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 