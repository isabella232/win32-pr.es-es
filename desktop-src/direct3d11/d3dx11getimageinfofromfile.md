---
title: Función D3DX11GetImageInfoFromFile (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, GetMetadataFromXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Recupera información sobre un archivo de imagen determinado.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- Función D3DX11GetImageInfoFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083768"
---
# <a name="d3dx11getimageinfofromfile-function"></a><span data-ttu-id="18266-106">D3DX11GetImageInfoFromFile función)</span><span class="sxs-lookup"><span data-stu-id="18266-106">D3DX11GetImageInfoFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="18266-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="18266-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="18266-108">En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXFILE** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.</span><span class="sxs-lookup"><span data-stu-id="18266-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="18266-109">Recupera información sobre un archivo de imagen determinado.</span><span class="sxs-lookup"><span data-stu-id="18266-109">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="18266-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18266-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="18266-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18266-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18266-112">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18266-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18266-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="18266-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="18266-114">Nombre de archivo de la imagen sobre la que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="18266-114">File name of image to retrieve information about.</span></span> <span data-ttu-id="18266-115">Si se definen Unicode o \_ Unicode, este tipo de parámetro es LPCWSTR; de lo contrario, el tipo es LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="18266-115">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="18266-116">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18266-116">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18266-117">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="18266-117">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="18266-118">Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="18266-118">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="18266-119">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="18266-119">Can be **NULL**.</span></span> <span data-ttu-id="18266-120">Consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="18266-120">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="18266-121">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18266-121">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18266-122">Tipo: **[ **\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="18266-122">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="18266-123">Puntero a la [**\_ \_ información de la imagen D3DX11**](d3dx11-image-info.md) que se va a rellenar con la descripción de los datos del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="18266-123">Pointer to a [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md) to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="18266-124">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="18266-124">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18266-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="18266-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="18266-126">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="18266-126">A pointer to the return value.</span></span> <span data-ttu-id="18266-127">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="18266-127">May be **NULL**.</span></span> <span data-ttu-id="18266-128">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="18266-128">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18266-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18266-129">Return value</span></span>

<span data-ttu-id="18266-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18266-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18266-131">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="18266-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="18266-132">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="18266-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="18266-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18266-133">Remarks</span></span>

<span data-ttu-id="18266-134">Esta función admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="18266-134">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="18266-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18266-135">Requirements</span></span>



| <span data-ttu-id="18266-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="18266-136">Requirement</span></span> | <span data-ttu-id="18266-137">Value</span><span class="sxs-lookup"><span data-stu-id="18266-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18266-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18266-138">Header</span></span><br/>  | <dl> <span data-ttu-id="18266-139"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="18266-139"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="18266-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18266-140">Library</span></span><br/> | <dl> <span data-ttu-id="18266-141"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18266-141"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="18266-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="18266-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18266-143">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="18266-143">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

