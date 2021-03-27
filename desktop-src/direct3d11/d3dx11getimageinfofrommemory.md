---
title: Función D3DX11GetImageInfoFromMemory (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, GetMetadataFromXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Obtiene información acerca de una imagen ya cargada en la memoria.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- Función D3DX11GetImageInfoFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987000"
---
# <a name="d3dx11getimageinfofrommemory-function"></a><span data-ttu-id="abc39-106">D3DX11GetImageInfoFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="abc39-106">D3DX11GetImageInfoFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="abc39-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="abc39-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="abc39-108">En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXMEMORY** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.</span><span class="sxs-lookup"><span data-stu-id="abc39-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="abc39-109">Obtiene información acerca de una imagen ya cargada en la memoria.</span><span class="sxs-lookup"><span data-stu-id="abc39-109">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc39-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abc39-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="abc39-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abc39-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc39-112">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abc39-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abc39-113">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="abc39-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="abc39-114">Puntero a la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="abc39-114">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="abc39-115">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abc39-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abc39-116">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="abc39-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="abc39-117">Tamaño de la imagen en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="abc39-117">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="abc39-118">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abc39-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abc39-119">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="abc39-119">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="abc39-120">Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="abc39-120">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="abc39-121">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="abc39-121">Can be **NULL**.</span></span> <span data-ttu-id="abc39-122">Consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="abc39-122">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="abc39-123">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abc39-123">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abc39-124">Tipo: **[ **\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="abc39-124">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="abc39-125">Información sobre la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="abc39-125">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="abc39-126">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="abc39-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abc39-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="abc39-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="abc39-128">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="abc39-128">A pointer to the return value.</span></span> <span data-ttu-id="abc39-129">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="abc39-129">May be **NULL**.</span></span> <span data-ttu-id="abc39-130">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="abc39-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc39-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abc39-131">Return value</span></span>

<span data-ttu-id="abc39-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abc39-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abc39-133">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="abc39-133">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abc39-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abc39-134">Requirements</span></span>



| <span data-ttu-id="abc39-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="abc39-135">Requirement</span></span> | <span data-ttu-id="abc39-136">Value</span><span class="sxs-lookup"><span data-stu-id="abc39-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abc39-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abc39-137">Header</span></span><br/>  | <dl> <span data-ttu-id="abc39-138"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="abc39-138"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="abc39-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="abc39-139">Library</span></span><br/> | <dl> <span data-ttu-id="abc39-140"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abc39-140"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="abc39-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="abc39-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc39-142">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="abc39-142">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

