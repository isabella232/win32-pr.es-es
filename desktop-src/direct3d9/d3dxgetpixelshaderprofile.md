---
description: 'Función D3DXGetPixelShaderProfile: devuelve el nombre del perfil hlsl (lenguaje de sombreador de alto nivel) más alto admitido por un dispositivo determinado.'
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Función D3DXGetPixelShaderProfile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114443"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="bf116-103">Función D3DXGetPixelShaderProfile</span><span class="sxs-lookup"><span data-stu-id="bf116-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="bf116-104">Devuelve el nombre del perfil de lenguaje de sombreador de alto nivel (HLSL) más alto admitido por un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="bf116-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf116-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf116-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="bf116-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf116-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf116-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bf116-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf116-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bf116-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bf116-109">Puntero al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf116-109">Pointer to the device.</span></span> <span data-ttu-id="bf116-110">Vea [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)</span><span class="sxs-lookup"><span data-stu-id="bf116-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf116-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf116-111">Return value</span></span>

<span data-ttu-id="bf116-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf116-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf116-113">Nombre del perfil HLSL.</span><span class="sxs-lookup"><span data-stu-id="bf116-113">The HLSL profile name.</span></span>

<span data-ttu-id="bf116-114">Si el dispositivo no admite sombreadores de píxeles, la función devuelve **NULL.**</span><span class="sxs-lookup"><span data-stu-id="bf116-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf116-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf116-115">Remarks</span></span>

<span data-ttu-id="bf116-116">Un perfil de sombreador especifica la versión del sombreador de ensamblados que se usará y las funcionalidades disponibles para el compilador HLSL al compilar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf116-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="bf116-117">En la tabla siguiente se enumeran los perfiles de sombreador de píxeles que se admiten.</span><span class="sxs-lookup"><span data-stu-id="bf116-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf116-118">Perfil de sombreador</span><span class="sxs-lookup"><span data-stu-id="bf116-118">Shader Profile</span></span></th>
<th><span data-ttu-id="bf116-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf116-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf116-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="bf116-120">ps_1_1</span></span></td>
<td><span data-ttu-id="bf116-121">Compile para ps_1_1 versión.</span><span class="sxs-lookup"><span data-stu-id="bf116-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf116-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="bf116-122">ps_1_2</span></span></td>
<td><span data-ttu-id="bf116-123">Compile para ps_1_2 versión.</span><span class="sxs-lookup"><span data-stu-id="bf116-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf116-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="bf116-124">ps_1_3</span></span></td>
<td><span data-ttu-id="bf116-125">Compile para ps_1_3 versión.</span><span class="sxs-lookup"><span data-stu-id="bf116-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf116-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="bf116-126">ps_1_4</span></span></td>
<td><span data-ttu-id="bf116-127">Compile para ps_1_4 versión.</span><span class="sxs-lookup"><span data-stu-id="bf116-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf116-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="bf116-128">ps_2_0</span></span></td>
<td><span data-ttu-id="bf116-129">Compile para ps_2_0 versión.</span><span class="sxs-lookup"><span data-stu-id="bf116-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf116-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="bf116-130">ps_2_a</span></span></td>
<td><span data-ttu-id="bf116-131">Igual que el perfil ps_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador sea el destino:</span><span class="sxs-lookup"><span data-stu-id="bf116-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="bf116-132">El número de registros temporales (r#) es mayor o igual que 22.</span><span class="sxs-lookup"><span data-stu-id="bf116-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="bf116-133">Swzzle de origen arbitrario.</span><span class="sxs-lookup"><span data-stu-id="bf116-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="bf116-134">Instrucciones de degradado: dsx, dsy.</span><span class="sxs-lookup"><span data-stu-id="bf116-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="bf116-135">Predicación.</span><span class="sxs-lookup"><span data-stu-id="bf116-135">Predication.</span></span></li>
<li><span data-ttu-id="bf116-136">No hay límite de lectura de textura dependiente.</span><span class="sxs-lookup"><span data-stu-id="bf116-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="bf116-137">No hay límite para el número de instrucciones de textura.</span><span class="sxs-lookup"><span data-stu-id="bf116-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf116-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="bf116-138">ps_2_b</span></span></td>
<td><span data-ttu-id="bf116-139">Igual que el perfil ps_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador sea el destino:</span><span class="sxs-lookup"><span data-stu-id="bf116-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="bf116-140">El número de registros temporales (r#) es mayor o igual que 32.</span><span class="sxs-lookup"><span data-stu-id="bf116-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="bf116-141">No hay límite para el número de instrucciones de textura.</span><span class="sxs-lookup"><span data-stu-id="bf116-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf116-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="bf116-142">ps_3_0</span></span></td>
<td><span data-ttu-id="bf116-143">Compile para ps_3_0 versión.</span><span class="sxs-lookup"><span data-stu-id="bf116-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bf116-144">Para obtener más información sobre las diferencias entre las versiones del sombreador, vea [Diferencias del sombreador de píxeles.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)</span><span class="sxs-lookup"><span data-stu-id="bf116-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf116-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf116-145">Requirements</span></span>



| <span data-ttu-id="bf116-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf116-146">Requirement</span></span> | <span data-ttu-id="bf116-147">Value</span><span class="sxs-lookup"><span data-stu-id="bf116-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf116-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf116-148">Header</span></span><br/>  | <dl> <span data-ttu-id="bf116-149"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="bf116-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bf116-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf116-150">Library</span></span><br/> | <dl> <span data-ttu-id="bf116-151"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf116-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bf116-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf116-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf116-153">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="bf116-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
