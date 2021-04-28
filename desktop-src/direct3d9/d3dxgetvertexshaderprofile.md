---
description: 'Función D3DXGetVertexShaderProfile: devuelve el nombre del perfil de lenguaje de sombreador de alto nivel (HLSL) más alto admitido por un dispositivo determinado.'
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Función D3DXGetVertexShaderProfile (D3DX9Shader.h)
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
ms.openlocfilehash: 70d6cdf79fdd91e819d54702682515aa3e4810b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114463"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="ad480-103">Función D3DXGetVertexShaderProfile</span><span class="sxs-lookup"><span data-stu-id="ad480-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="ad480-104">Devuelve el nombre del perfil de lenguaje de sombreador de alto nivel (HLSL) más alto admitido por un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="ad480-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad480-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad480-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ad480-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad480-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ad480-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad480-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ad480-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ad480-109">Puntero al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ad480-109">Pointer to the device.</span></span> <span data-ttu-id="ad480-110">Vea [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)</span><span class="sxs-lookup"><span data-stu-id="ad480-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad480-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad480-111">Return value</span></span>

<span data-ttu-id="ad480-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad480-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad480-113">Nombre del perfil HLSL.</span><span class="sxs-lookup"><span data-stu-id="ad480-113">The HLSL profile name.</span></span>

<span data-ttu-id="ad480-114">Si el dispositivo no admite sombreadores de vértices, la función devuelve **NULL.**</span><span class="sxs-lookup"><span data-stu-id="ad480-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad480-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad480-115">Remarks</span></span>

<span data-ttu-id="ad480-116">Un perfil de sombreador especifica la versión del sombreador de ensamblados que se usará y las funcionalidades disponibles para el compilador HLSL al compilar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="ad480-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="ad480-117">En la tabla siguiente se enumeran los perfiles de sombreador de vértices que se admiten.</span><span class="sxs-lookup"><span data-stu-id="ad480-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad480-118">Perfil de sombreador</span><span class="sxs-lookup"><span data-stu-id="ad480-118">Shader Profile</span></span></th>
<th><span data-ttu-id="ad480-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad480-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ad480-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="ad480-120">vs_1_1</span></span></td>
<td><span data-ttu-id="ad480-121">Compile para vs_1_1 versión.</span><span class="sxs-lookup"><span data-stu-id="ad480-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad480-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="ad480-122">vs_2_0</span></span></td>
<td><span data-ttu-id="ad480-123">Compile para vs_2_0 versión.</span><span class="sxs-lookup"><span data-stu-id="ad480-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad480-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="ad480-124">vs_2_a</span></span></td>
<td><span data-ttu-id="ad480-125">Igual que el perfil vs_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador lo deba tener como destino:</span><span class="sxs-lookup"><span data-stu-id="ad480-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="ad480-126">El número de registros temporales (r#) es mayor o igual que 13.</span><span class="sxs-lookup"><span data-stu-id="ad480-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="ad480-127">Instrucción de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="ad480-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="ad480-128">Predicación.</span><span class="sxs-lookup"><span data-stu-id="ad480-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad480-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="ad480-129">vs_3_0</span></span></td>
<td><span data-ttu-id="ad480-130">Compile para vs_3_0 versión.</span><span class="sxs-lookup"><span data-stu-id="ad480-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ad480-131">Para obtener más información sobre las diferencias entre las versiones del sombreador, vea [Diferencias de sombreador de vértices.](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md)</span><span class="sxs-lookup"><span data-stu-id="ad480-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad480-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad480-132">Requirements</span></span>



| <span data-ttu-id="ad480-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad480-133">Requirement</span></span> | <span data-ttu-id="ad480-134">Value</span><span class="sxs-lookup"><span data-stu-id="ad480-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad480-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad480-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ad480-136"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="ad480-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ad480-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad480-137">Library</span></span><br/> | <dl> <span data-ttu-id="ad480-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad480-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ad480-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad480-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad480-140">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="ad480-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
