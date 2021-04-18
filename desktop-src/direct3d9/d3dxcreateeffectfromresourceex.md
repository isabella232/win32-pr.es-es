---
description: Cree un efecto a partir de una descripción de efectos ASCII o binarios. Se trata de una versión extendida de D3DXCreateEffectFromResource que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: Función D3DXCreateEffectFromResourceEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718397"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a><span data-ttu-id="8c97f-104">D3DXCreateEffectFromResourceEx función)</span><span class="sxs-lookup"><span data-stu-id="8c97f-104">D3DXCreateEffectFromResourceEx function</span></span>

<span data-ttu-id="8c97f-105">Cree un efecto a partir de una descripción de efectos ASCII o binarios.</span><span class="sxs-lookup"><span data-stu-id="8c97f-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="8c97f-106">Se trata de una versión extendida de [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.</span><span class="sxs-lookup"><span data-stu-id="8c97f-106">This is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c97f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c97f-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="8c97f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c97f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c97f-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8c97f-111">Puntero al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c97f-111">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-112">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c97f-114">Identificador de un módulo que contiene la descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="8c97f-114">Handle to a module containing the effect description.</span></span> <span data-ttu-id="8c97f-115">Si este parámetro es **null**, se usará el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="8c97f-115">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-116">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-117">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c97f-118">Puntero al recurso.</span><span class="sxs-lookup"><span data-stu-id="8c97f-118">Pointer to the resource.</span></span> <span data-ttu-id="8c97f-119">Este parámetro admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="8c97f-119">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="8c97f-120">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8c97f-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-121">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-122">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c97f-122">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="8c97f-123">Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="8c97f-123">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="8c97f-124">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8c97f-124">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-125">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-125">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-126">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-126">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="8c97f-127">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="8c97f-127">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="8c97f-128">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="8c97f-128">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-129">*pSkipConstants* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-129">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c97f-131">Una cadena de parámetros de efecto que el sistema de efectos omitirá.</span><span class="sxs-lookup"><span data-stu-id="8c97f-131">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="8c97f-132">La cadena debe terminar en **null** y debe contener el nombre de cada constante administrada por la aplicación separada por un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="8c97f-132">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-133">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-133">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c97f-135">Si *pSrcResource* contiene un efecto de texto, las marcas pueden ser una combinación de marcas de [D3DXSHADER](d3dxshader-flags.md) y marcas de [D3DXFX](d3dxfx.md) ; de lo contrario, *pSrcResource* contiene un efecto binario y las únicas marcas respetadas son marcas D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="8c97f-135">If *pSrcResource* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcResource* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="8c97f-136">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8c97f-136">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="8c97f-137">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="8c97f-137">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-138">*pPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-138">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-139">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-139">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="8c97f-140">Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) que se va a usar para los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="8c97f-140">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="8c97f-141">Si este valor es **null**, no se compartirá ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="8c97f-141">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-142">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-143">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c97f-143">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="8c97f-144">Devuelve un búfer que contiene el efecto compilado.</span><span class="sxs-lookup"><span data-stu-id="8c97f-144">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="8c97f-145">*ppCompilationErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c97f-145">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c97f-146">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c97f-146">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8c97f-147">Devuelve un búfer que contiene una lista de errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="8c97f-147">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c97f-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c97f-148">Return value</span></span>

<span data-ttu-id="8c97f-149">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c97f-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c97f-150">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c97f-150">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8c97f-151">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8c97f-151">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c97f-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c97f-152">Remarks</span></span>

<span data-ttu-id="8c97f-153">Esta función es una versión extendida de [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite a una aplicación especificar qué constantes de efecto administrará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c97f-153">This function is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="8c97f-154">El sistema de efectos omite una constante administrada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c97f-154">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="8c97f-155">Es decir, la aplicación es responsable de inicializar la constante, así como de guardar y restaurar su estado siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8c97f-155">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="8c97f-156">Esta función comprueba cada constante de pSkipConstants para ver lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8c97f-156">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="8c97f-157">Está enlazado a un registro constante.</span><span class="sxs-lookup"><span data-stu-id="8c97f-157">It is bound to a constant register.</span></span>
-   <span data-ttu-id="8c97f-158">Solo se usa en el código del sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="8c97f-158">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="8c97f-159">Si se asigna un nombre a una constante en la cadena que no está presente en el efecto, se omite.</span><span class="sxs-lookup"><span data-stu-id="8c97f-159">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="8c97f-160">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="8c97f-160">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8c97f-161">De lo contrario, el tipo de datos LPCTSTR se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8c97f-161">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="8c97f-162">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="8c97f-162">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8c97f-163">Si se define Unicode, la llamada de función se resuelve como D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="8c97f-163">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="8c97f-164">De lo contrario, la llamada de función se resuelve como D3DXCreateEffectFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="8c97f-164">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="8c97f-165">D3DXCreateEffectFromResource carga los datos de un recurso de tipo RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="8c97f-165">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="8c97f-166">Consulte MSDN para obtener más información acerca de los recursos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8c97f-166">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c97f-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c97f-167">Requirements</span></span>



| <span data-ttu-id="8c97f-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c97f-168">Requirement</span></span> | <span data-ttu-id="8c97f-169">Value</span><span class="sxs-lookup"><span data-stu-id="8c97f-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c97f-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c97f-170">Header</span></span><br/>  | <dl> <span data-ttu-id="8c97f-171"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c97f-171"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8c97f-172">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c97f-172">Library</span></span><br/> | <dl> <span data-ttu-id="8c97f-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c97f-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8c97f-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c97f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c97f-175">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="8c97f-175">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="8c97f-176">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="8c97f-176">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="8c97f-177">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="8c97f-177">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
