---
description: 'Función D3DX10GetImageInfoFromResource: recupera información sobre una imagen determinada en un recurso.'
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Función D3DX10GetImageInfoFromResource (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 650d05f379be634bfdd9dfb0908153260f795b00
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098373"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="938b5-103">Función D3DX10GetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="938b5-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="938b5-104">Recupera información sobre una imagen determinada en un recurso.</span><span class="sxs-lookup"><span data-stu-id="938b5-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="938b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="938b5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="938b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="938b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="938b5-107">*hSrcModule* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="938b5-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938b5-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="938b5-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="938b5-109">Módulo donde se carga el recurso.</span><span class="sxs-lookup"><span data-stu-id="938b5-109">Module where the resource is loaded.</span></span> <span data-ttu-id="938b5-110">Establezca este parámetro en **NULL** para especificar el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="938b5-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="938b5-111">*pSrcResource* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="938b5-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938b5-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="938b5-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="938b5-113">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="938b5-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="938b5-114">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="938b5-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="938b5-115">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="938b5-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="938b5-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="938b5-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="938b5-117">*pPump* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="938b5-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938b5-118">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="938b5-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="938b5-119">Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="938b5-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="938b5-120">Puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="938b5-120">Can be **NULL**.</span></span> <span data-ttu-id="938b5-121">Vea [**ID3DX10ThreadPump.**](id3dx10threadpump.md)</span><span class="sxs-lookup"><span data-stu-id="938b5-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="938b5-122">*pSrcInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="938b5-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938b5-123">Tipo: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="938b5-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="938b5-124">Puntero a una estructura DE INFORMACIÓN DE IMAGEN D3DX10 que se va a rellenar con la descripción de \_ los datos del archivo de \_ origen.</span><span class="sxs-lookup"><span data-stu-id="938b5-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="938b5-125">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="938b5-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="938b5-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="938b5-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="938b5-127">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="938b5-127">A pointer to the return value.</span></span> <span data-ttu-id="938b5-128">Puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="938b5-128">May be **NULL**.</span></span> <span data-ttu-id="938b5-129">Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="938b5-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="938b5-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="938b5-130">Return value</span></span>

<span data-ttu-id="938b5-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="938b5-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="938b5-132">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="938b5-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="938b5-133">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="938b5-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="938b5-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="938b5-134">Remarks</span></span>

<span data-ttu-id="938b5-135">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="938b5-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="938b5-136">Si se define Unicode, la llamada de función se resuelve en D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="938b5-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="938b5-137">De lo contrario, la llamada de función se resuelve en D3DX10GetImageInfoFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="938b5-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="938b5-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="938b5-138">Requirements</span></span>



| <span data-ttu-id="938b5-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="938b5-139">Requirement</span></span> | <span data-ttu-id="938b5-140">Value</span><span class="sxs-lookup"><span data-stu-id="938b5-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="938b5-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="938b5-141">Header</span></span><br/>  | <dl> <span data-ttu-id="938b5-142"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="938b5-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="938b5-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="938b5-143">Library</span></span><br/> | <dl> <span data-ttu-id="938b5-144"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="938b5-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="938b5-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="938b5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="938b5-146">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="938b5-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
