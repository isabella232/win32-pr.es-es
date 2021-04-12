---
description: Recupera información acerca de una imagen determinada en un recurso.
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Función D3DX10GetImageInfoFromResource (D3DX10Tex. h)
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
ms.openlocfilehash: e77efb973e20a5db708d28b49f0cee27bee7d4e5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280273"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="ee4e3-103">D3DX10GetImageInfoFromResource función)</span><span class="sxs-lookup"><span data-stu-id="ee4e3-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="ee4e3-104">Recupera información acerca de una imagen determinada en un recurso.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee4e3-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ee4e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee4e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee4e3-107">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4e3-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4e3-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4e3-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee4e3-109">Módulo en el que se carga el recurso.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-109">Module where the resource is loaded.</span></span> <span data-ttu-id="ee4e3-110">Establezca este parámetro en **null** para especificar el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="ee4e3-111">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4e3-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4e3-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4e3-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee4e3-113">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ee4e3-114">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ee4e3-115">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="ee4e3-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ee4e3-117">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4e3-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4e3-118">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee4e3-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="ee4e3-119">Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="ee4e3-120">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-120">Can be **NULL**.</span></span> <span data-ttu-id="ee4e3-121">Vea [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="ee4e3-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee4e3-122">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4e3-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4e3-123">Tipo: **[ **\_ \_ información de imagen de D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee4e3-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="ee4e3-124">Puntero a una \_ estructura de \_ información de imagen D3DX10 que se va a rellenar con la descripción de los datos del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="ee4e3-125">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ee4e3-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4e3-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ee4e3-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ee4e3-127">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-127">A pointer to the return value.</span></span> <span data-ttu-id="ee4e3-128">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-128">May be **NULL**.</span></span> <span data-ttu-id="ee4e3-129">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee4e3-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee4e3-130">Return value</span></span>

<span data-ttu-id="ee4e3-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee4e3-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee4e3-132">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee4e3-133">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="ee4e3-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="ee4e3-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee4e3-134">Remarks</span></span>

<span data-ttu-id="ee4e3-135">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ee4e3-136">Si se define Unicode, la llamada de función se resuelve como D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="ee4e3-137">De lo contrario, la llamada de función se resuelve como D3DX10GetImageInfoFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee4e3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4e3-138">Requirements</span></span>



| <span data-ttu-id="ee4e3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4e3-139">Requirement</span></span> | <span data-ttu-id="ee4e3-140">Value</span><span class="sxs-lookup"><span data-stu-id="ee4e3-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4e3-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee4e3-141">Header</span></span><br/>  | <dl> <span data-ttu-id="ee4e3-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e3-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ee4e3-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee4e3-143">Library</span></span><br/> | <dl> <span data-ttu-id="ee4e3-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e3-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ee4e3-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee4e3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4e3-146">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="ee4e3-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
