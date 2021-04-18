---
description: Crea un efecto a partir de una descripción de efectos ASCII o binarios. Esta función es una versión extendida de D3DXCreateEffect que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: Función D3DXCreateEffectEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 979b09f852e692b4c25414607f79cd8792342755
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721471"
---
# <a name="d3dxcreateeffectex-function"></a><span data-ttu-id="789e6-104">D3DXCreateEffectEx función)</span><span class="sxs-lookup"><span data-stu-id="789e6-104">D3DXCreateEffectEx function</span></span>

<span data-ttu-id="789e6-105">Crea un efecto a partir de una descripción de efectos ASCII o binarios.</span><span class="sxs-lookup"><span data-stu-id="789e6-105">Creates an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="789e6-106">Esta función es una versión extendida de [**D3DXCreateEffect**](d3dxcreateeffect.md) que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.</span><span class="sxs-lookup"><span data-stu-id="789e6-106">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="789e6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="789e6-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="789e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="789e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789e6-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="789e6-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="789e6-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="789e6-111">Puntero al dispositivo que va a crear el efecto.</span><span class="sxs-lookup"><span data-stu-id="789e6-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="789e6-112">Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="789e6-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="789e6-113">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="789e6-113">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-114">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="789e6-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="789e6-115">Puntero a un búfer que contiene una descripción de efecto.</span><span class="sxs-lookup"><span data-stu-id="789e6-115">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-116">*SrcDataLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="789e6-116">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="789e6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="789e6-118">Longitud de los datos del efecto, en bytes.</span><span class="sxs-lookup"><span data-stu-id="789e6-118">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-119">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="789e6-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-120">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="789e6-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="789e6-121">Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="789e6-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="789e6-122">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="789e6-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-123">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="789e6-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-124">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="789e6-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="789e6-125">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="789e6-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="789e6-126">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="789e6-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-127">*pSkipConstants* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="789e6-127">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-128">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="789e6-128">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="789e6-129">Una cadena de parámetros de efecto que el sistema de efectos omitirá.</span><span class="sxs-lookup"><span data-stu-id="789e6-129">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="789e6-130">La cadena debe terminar en **null** y debe contener el nombre de cada constante administrada por la aplicación separada por un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="789e6-130">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-131">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="789e6-131">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="789e6-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="789e6-133">Si *pSrcData* contiene un efecto de texto, las marcas pueden ser una combinación de marcas de [D3DXSHADER](d3dxshader-flags.md) y marcas de [D3DXFX](d3dxfx.md) ; de lo contrario, *pSrcData* contiene un efecto binario y las únicas marcas respetadas son marcas D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="789e6-133">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="789e6-134">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="789e6-134">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="789e6-135">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="789e6-135">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-136">*pPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="789e6-136">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-137">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="789e6-137">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="789e6-138">Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) que se va a usar para los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="789e6-138">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="789e6-139">Si este valor es **null**, no se compartirá ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="789e6-139">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-140">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="789e6-140">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-141">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="789e6-141">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="789e6-142">Devuelve un puntero a una interfaz [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="789e6-142">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="789e6-143">*ppCompilationErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="789e6-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="789e6-144">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="789e6-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="789e6-145">Devuelve un búfer que contiene una lista de errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="789e6-145">Returns a buffer containing a list of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="789e6-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="789e6-146">Return value</span></span>

<span data-ttu-id="789e6-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="789e6-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="789e6-148">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="789e6-148">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="789e6-149">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="789e6-149">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="789e6-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="789e6-150">Remarks</span></span>

<span data-ttu-id="789e6-151">Esta función es una versión extendida de [**D3DXCreateEffect**](d3dxcreateeffect.md) que permite a una aplicación especificar qué constantes de efecto administrará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="789e6-151">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="789e6-152">El sistema de efectos omite una constante administrada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="789e6-152">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="789e6-153">Es decir, la aplicación es responsable de inicializar la constante, así como de guardar y restaurar su estado siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="789e6-153">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="789e6-154">Esta función comprueba cada constante de pSkipConstants para ver lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="789e6-154">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="789e6-155">Está enlazado a un registro constante.</span><span class="sxs-lookup"><span data-stu-id="789e6-155">It is bound to a constant register.</span></span>
-   <span data-ttu-id="789e6-156">Solo se usa en el código del sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="789e6-156">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="789e6-157">Si se asigna un nombre a una constante en la cadena que no está presente en el efecto, se omite.</span><span class="sxs-lookup"><span data-stu-id="789e6-157">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="789e6-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="789e6-158">Requirements</span></span>



| <span data-ttu-id="789e6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="789e6-159">Requirement</span></span> | <span data-ttu-id="789e6-160">Value</span><span class="sxs-lookup"><span data-stu-id="789e6-160">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="789e6-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="789e6-161">Header</span></span><br/>  | <dl> <span data-ttu-id="789e6-162"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="789e6-162"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="789e6-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="789e6-163">Library</span></span><br/> | <dl> <span data-ttu-id="789e6-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="789e6-164"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="789e6-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="789e6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789e6-166">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="789e6-166">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="789e6-167">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="789e6-167">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[<span data-ttu-id="789e6-168">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="789e6-168">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
