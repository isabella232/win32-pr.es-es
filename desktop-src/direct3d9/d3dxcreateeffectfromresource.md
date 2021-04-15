---
description: Cree un efecto a partir de una descripción de efectos ASCII o binarios.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Función D3DXCreateEffectFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36db2c82debc542301ba44d4baa74ecaaf01245e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708013"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="fdf3b-103">D3DXCreateEffectFromResource función)</span><span class="sxs-lookup"><span data-stu-id="fdf3b-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="fdf3b-104">Cree un efecto a partir de una descripción de efectos ASCII o binarios.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf3b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdf3b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="fdf3b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdf3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf3b-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fdf3b-109">Puntero al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-110">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdf3b-112">Identificador de un módulo que contiene la descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="fdf3b-113">Si este parámetro es **null**, se usará el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-114">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdf3b-116">Puntero al recurso.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-116">Pointer to the resource.</span></span> <span data-ttu-id="fdf3b-117">Este parámetro admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="fdf3b-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-119">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-120">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdf3b-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="fdf3b-121">Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="fdf3b-122">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-123">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-124">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="fdf3b-125">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="fdf3b-126">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-127">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdf3b-129">Si *hSrcModule* contiene un efecto de texto, las marcas pueden ser una combinación de marcas de [D3DXSHADER](d3dxshader-flags.md) y marcas de [D3DXFX](d3dxfx.md) ; de lo contrario, *hSrcModule* contiene un efecto binario y las únicas marcas respetadas son marcas D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="fdf3b-130">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="fdf3b-131">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-132">*pPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-133">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="fdf3b-134">Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) que se va a usar para los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="fdf3b-135">Si este valor es **null**, no se compartirá ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-136">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-137">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdf3b-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="fdf3b-138">Devuelve un búfer que contiene el efecto compilado.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="fdf3b-139">*ppCompilationErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fdf3b-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf3b-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdf3b-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fdf3b-141">Devuelve un búfer que contiene una lista de errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf3b-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdf3b-142">Return value</span></span>

<span data-ttu-id="fdf3b-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fdf3b-144">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fdf3b-145">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdf3b-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdf3b-146">Remarks</span></span>

<span data-ttu-id="fdf3b-147">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fdf3b-148">De lo contrario, el tipo de datos LPCTSTR se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="fdf3b-149">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fdf3b-150">Si se define Unicode, la llamada de función se resuelve como D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="fdf3b-151">De lo contrario, la llamada de función se resuelve como D3DXCreateEffectFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="fdf3b-152">D3DXCreateEffectFromResource carga los datos de un recurso de tipo RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="fdf3b-153">Consulte MSDN para obtener más información acerca de los recursos de Windows.</span><span class="sxs-lookup"><span data-stu-id="fdf3b-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf3b-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdf3b-154">Requirements</span></span>



| <span data-ttu-id="fdf3b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdf3b-155">Requirement</span></span> | <span data-ttu-id="fdf3b-156">Value</span><span class="sxs-lookup"><span data-stu-id="fdf3b-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf3b-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdf3b-157">Header</span></span><br/>  | <dl> <span data-ttu-id="fdf3b-158"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf3b-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="fdf3b-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdf3b-159">Library</span></span><br/> | <dl> <span data-ttu-id="fdf3b-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdf3b-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fdf3b-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdf3b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf3b-162">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="fdf3b-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="fdf3b-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="fdf3b-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="fdf3b-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
