---
description: Cree un efecto a partir de una descripción de efectos ASCII o binarios. Esta función es una versión extendida de D3DXCreateEffectFromFile que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: Función D3DXCreateEffectFromFileEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721501"
---
# <a name="d3dxcreateeffectfromfileex-function"></a><span data-ttu-id="aae27-104">D3DXCreateEffectFromFileEx función)</span><span class="sxs-lookup"><span data-stu-id="aae27-104">D3DXCreateEffectFromFileEx function</span></span>

<span data-ttu-id="aae27-105">Cree un efecto a partir de una descripción de efectos ASCII o binarios.</span><span class="sxs-lookup"><span data-stu-id="aae27-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="aae27-106">Esta función es una versión extendida de [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.</span><span class="sxs-lookup"><span data-stu-id="aae27-106">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aae27-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="aae27-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aae27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae27-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aae27-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="aae27-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="aae27-111">Puntero al dispositivo que va a crear el efecto.</span><span class="sxs-lookup"><span data-stu-id="aae27-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="aae27-112">Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="aae27-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="aae27-113">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aae27-113">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae27-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aae27-115">Puntero al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="aae27-115">Pointer to the filename.</span></span> <span data-ttu-id="aae27-116">Este parámetro admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="aae27-116">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="aae27-117">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="aae27-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="aae27-118">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aae27-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-119">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="aae27-119">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="aae27-120">Matriz opcional terminada en NULL de definiciones de macro de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="aae27-120">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="aae27-121">Vea [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="aae27-121">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="aae27-122">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aae27-122">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-123">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="aae27-123">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="aae27-124">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="aae27-124">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="aae27-125">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="aae27-125">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="aae27-126">*pSkipConstants* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aae27-126">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-127">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae27-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aae27-128">Una cadena de parámetros de efecto que el sistema de efectos omitirá.</span><span class="sxs-lookup"><span data-stu-id="aae27-128">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="aae27-129">La cadena debe terminar en **null** y debe contener el nombre de cada constante administrada por la aplicación separada por un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="aae27-129">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="aae27-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="aae27-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae27-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aae27-132">Si *pSrcFile* contiene un efecto de texto, las marcas pueden ser una combinación de marcas de [D3DXSHADER](d3dxshader-flags.md) y marcas de [D3DXFX](d3dxfx.md) ; de lo contrario, *pSrcFile* contiene un efecto binario y las únicas marcas respetadas son marcas D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="aae27-132">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="aae27-133">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aae27-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="aae27-134">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="aae27-134">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="aae27-135">*pPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aae27-135">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-136">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="aae27-136">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="aae27-137">Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) que se va a usar para los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="aae27-137">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="aae27-138">Si este valor es **null**, no se compartirá ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="aae27-138">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="aae27-139">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aae27-139">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-140">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="aae27-140">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="aae27-141">Devuelve un puntero a un búfer que contiene el efecto compilado.</span><span class="sxs-lookup"><span data-stu-id="aae27-141">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="aae27-142">Vea [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="aae27-142">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="aae27-143">*ppCompilationErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aae27-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae27-144">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="aae27-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="aae27-145">Devuelve un puntero a un búfer que contiene una lista de errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="aae27-145">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="aae27-146">Vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="aae27-146">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae27-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aae27-147">Return value</span></span>

<span data-ttu-id="aae27-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aae27-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aae27-149">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aae27-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aae27-150">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="aae27-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="aae27-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aae27-151">Remarks</span></span>

<span data-ttu-id="aae27-152">Esta función es una versión extendida de [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite a una aplicación especificar qué constantes de efecto administrará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aae27-152">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="aae27-153">El sistema de efectos omite una constante administrada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aae27-153">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="aae27-154">Es decir, la aplicación es responsable de inicializar la constante, así como de guardar y restaurar su estado siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="aae27-154">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="aae27-155">Esta función comprueba cada constante de pSkipConstants para ver lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="aae27-155">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="aae27-156">Está enlazado a un registro constante.</span><span class="sxs-lookup"><span data-stu-id="aae27-156">It is bound to a constant register.</span></span>
-   <span data-ttu-id="aae27-157">Solo se usa en el código del sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="aae27-157">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="aae27-158">Si se asigna un nombre a una constante en la cadena que no está presente en el efecto, se omite.</span><span class="sxs-lookup"><span data-stu-id="aae27-158">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="aae27-159">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="aae27-159">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="aae27-160">De lo contrario, el tipo de datos LPCTSTR se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="aae27-160">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="aae27-161">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="aae27-161">The compiler setting also determines the function version.</span></span> <span data-ttu-id="aae27-162">Si se define Unicode, la llamada de función se resuelve como D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="aae27-162">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="aae27-163">De lo contrario, la llamada de función se resuelve como D3DXCreateEffectFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="aae27-163">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae27-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aae27-164">Requirements</span></span>



| <span data-ttu-id="aae27-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae27-165">Requirement</span></span> | <span data-ttu-id="aae27-166">Value</span><span class="sxs-lookup"><span data-stu-id="aae27-166">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae27-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aae27-167">Header</span></span><br/>  | <dl> <span data-ttu-id="aae27-168"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae27-168"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="aae27-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aae27-169">Library</span></span><br/> | <dl> <span data-ttu-id="aae27-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aae27-170"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="aae27-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="aae27-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae27-172">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="aae27-172">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="aae27-173">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="aae27-173">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="aae27-174">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="aae27-174">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
