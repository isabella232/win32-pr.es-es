---
title: Función D3DX11GetImageInfoFromResource (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar funciones de recursos y, a continuación, usar la biblioteca DirectXTex (herramientas), LoadFromXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Recupera información acerca de una imagen determinada en un recurso.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Función D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987001"
---
# <a name="d3dx11getimageinfofromresource-function"></a><span data-ttu-id="c071f-106">D3DX11GetImageInfoFromResource función)</span><span class="sxs-lookup"><span data-stu-id="c071f-106">D3DX11GetImageInfoFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="c071f-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="c071f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="c071f-108">En lugar de usar esta función, se recomienda usar funciones de [recursos](/windows/desktop/menurc/resources-functions)y, a continuación, usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LOADFROMXXXMEMORY** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.</span><span class="sxs-lookup"><span data-stu-id="c071f-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="c071f-109">Recupera información acerca de una imagen determinada en un recurso.</span><span class="sxs-lookup"><span data-stu-id="c071f-109">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c071f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c071f-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c071f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c071f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c071f-112">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c071f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c071f-113">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c071f-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c071f-114">Módulo en el que se carga el recurso.</span><span class="sxs-lookup"><span data-stu-id="c071f-114">Module where the resource is loaded.</span></span> <span data-ttu-id="c071f-115">Establezca este parámetro en **null** para especificar el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="c071f-115">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="c071f-116">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c071f-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c071f-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c071f-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c071f-118">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c071f-118">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="c071f-119">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c071f-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c071f-120">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c071f-120">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="c071f-121">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="c071f-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c071f-122">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c071f-122">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c071f-123">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c071f-123">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="c071f-124">Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c071f-124">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="c071f-125">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c071f-125">Can be **NULL**.</span></span> <span data-ttu-id="c071f-126">Consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="c071f-126">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="c071f-127">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c071f-127">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c071f-128">Tipo: **[ **\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c071f-128">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="c071f-129">Puntero a una \_ estructura de \_ información de imagen D3DX11 que se va a rellenar con la descripción de los datos del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="c071f-129">Pointer to a D3DX11\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="c071f-130">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c071f-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c071f-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c071f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c071f-132">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c071f-132">A pointer to the return value.</span></span> <span data-ttu-id="c071f-133">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c071f-133">May be **NULL**.</span></span> <span data-ttu-id="c071f-134">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c071f-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c071f-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c071f-135">Return value</span></span>

<span data-ttu-id="c071f-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c071f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c071f-137">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c071f-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c071f-138">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="c071f-138">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c071f-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c071f-139">Remarks</span></span>

<span data-ttu-id="c071f-140">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="c071f-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c071f-141">Si se define Unicode, la llamada de función se resuelve como **D3DX11GetImageInfoFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="c071f-141">If Unicode is defined, the function call resolves to **D3DX11GetImageInfoFromResourceW**.</span></span> <span data-ttu-id="c071f-142">De lo contrario, la llamada de función se resuelve como **D3DX11GetImageInfoFromResourceA** porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="c071f-142">Otherwise, the function call resolves to **D3DX11GetImageInfoFromResourceA** because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c071f-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c071f-143">Requirements</span></span>



| <span data-ttu-id="c071f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c071f-144">Requirement</span></span> | <span data-ttu-id="c071f-145">Value</span><span class="sxs-lookup"><span data-stu-id="c071f-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c071f-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c071f-146">Header</span></span><br/>  | <dl> <span data-ttu-id="c071f-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-147"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c071f-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c071f-148">Library</span></span><br/> | <dl> <span data-ttu-id="c071f-149"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-149"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c071f-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="c071f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c071f-151">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="c071f-151">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

