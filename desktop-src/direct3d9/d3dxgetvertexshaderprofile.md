---
description: Devuelve el nombre del perfil de lenguaje de sombreado de alto nivel (HLSL) más alto compatible con un dispositivo determinado.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Función D3DXGetVertexShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717755"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="aaa7e-103">D3DXGetVertexShaderProfile función)</span><span class="sxs-lookup"><span data-stu-id="aaa7e-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="aaa7e-104">Devuelve el nombre del perfil de lenguaje de sombreado de alto nivel (HLSL) más alto compatible con un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aaa7e-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="aaa7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aaa7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa7e-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaa7e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa7e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="aaa7e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="aaa7e-109">Puntero al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-109">Pointer to the device.</span></span> <span data-ttu-id="aaa7e-110">Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="aaa7e-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa7e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aaa7e-111">Return value</span></span>

<span data-ttu-id="aaa7e-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaa7e-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aaa7e-113">Nombre del perfil de HLSL.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-113">The HLSL profile name.</span></span>

<span data-ttu-id="aaa7e-114">Si el dispositivo no admite sombreadores de vértices, la función devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa7e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aaa7e-115">Remarks</span></span>

<span data-ttu-id="aaa7e-116">Un perfil de sombreador especifica la versión del sombreador de ensamblado que se va a usar y las capacidades disponibles para el compilador de HLSL al compilar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="aaa7e-117">En la tabla siguiente se enumeran los perfiles del sombreador de vértices que se admiten.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aaa7e-118">Perfil de sombreador</span><span class="sxs-lookup"><span data-stu-id="aaa7e-118">Shader Profile</span></span></th>
<th><span data-ttu-id="aaa7e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaa7e-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aaa7e-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="aaa7e-120">vs_1_1</span></span></td>
<td><span data-ttu-id="aaa7e-121">Compilar para vs_1_1 versión.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaa7e-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="aaa7e-122">vs_2_0</span></span></td>
<td><span data-ttu-id="aaa7e-123">Compilar para vs_2_0 versión.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaa7e-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="aaa7e-124">vs_2_a</span></span></td>
<td><span data-ttu-id="aaa7e-125">Igual que el perfil de vs_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador tenga como destino:</span><span class="sxs-lookup"><span data-stu-id="aaa7e-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="aaa7e-126">El número de registros temporales (r #) es mayor o igual a 13.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="aaa7e-127">Instrucción de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="aaa7e-128">Predication.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaa7e-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="aaa7e-129">vs_3_0</span></span></td>
<td><span data-ttu-id="aaa7e-130">Compilar para vs_3_0 versión.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="aaa7e-131">Para obtener más información sobre las diferencias entre las versiones del sombreador, vea [diferencias del sombreador de vértices](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span><span class="sxs-lookup"><span data-stu-id="aaa7e-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa7e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaa7e-132">Requirements</span></span>



| <span data-ttu-id="aaa7e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaa7e-133">Requirement</span></span> | <span data-ttu-id="aaa7e-134">Value</span><span class="sxs-lookup"><span data-stu-id="aaa7e-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa7e-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aaa7e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="aaa7e-136"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaa7e-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="aaa7e-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aaa7e-137">Library</span></span><br/> | <dl> <span data-ttu-id="aaa7e-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaa7e-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="aaa7e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="aaa7e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa7e-140">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="aaa7e-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
