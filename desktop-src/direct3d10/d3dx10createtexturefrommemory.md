---
description: Cree un recurso de textura a partir de un archivo que reside en la memoria del sistema.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: Función D3DX10CreateTextureFromMemory (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 885f734cd9caeaccbab27b2fcdb258c032c5d7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003792"
---
# <a name="d3dx10createtexturefrommemory-function"></a><span data-ttu-id="e2134-103">D3DX10CreateTextureFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="e2134-103">D3DX10CreateTextureFromMemory function</span></span>

<span data-ttu-id="e2134-104">Cree un recurso de textura a partir de un archivo que reside en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2134-104">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2134-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2134-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e2134-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2134-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2134-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2134-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2134-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="e2134-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="e2134-109">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="e2134-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e2134-110">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2134-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2134-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2134-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2134-112">Puntero al recurso en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2134-112">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="e2134-113">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2134-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2134-114">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2134-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2134-115">Tamaño del recurso en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2134-115">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="e2134-116">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2134-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2134-117">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2134-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="e2134-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e2134-118">Optional.</span></span> <span data-ttu-id="e2134-119">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="e2134-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e2134-120">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2134-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2134-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2134-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="e2134-122">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="e2134-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="e2134-123">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="e2134-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="e2134-124">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e2134-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2134-125">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="e2134-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="e2134-126">Dirección de un puntero al recurso creado.</span><span class="sxs-lookup"><span data-stu-id="e2134-126">Address of a pointer to the created resource.</span></span> <span data-ttu-id="e2134-127">Consulte la [**interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="e2134-127">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="e2134-128">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e2134-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2134-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e2134-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e2134-130">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e2134-130">A pointer to the return value.</span></span> <span data-ttu-id="e2134-131">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="e2134-131">May be **NULL**.</span></span> <span data-ttu-id="e2134-132">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e2134-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2134-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2134-133">Return value</span></span>

<span data-ttu-id="e2134-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2134-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2134-135">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e2134-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2134-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2134-136">Remarks</span></span>

<span data-ttu-id="e2134-137">Para obtener una lista de formatos de imagen admitidos, consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e2134-137">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2134-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2134-138">Requirements</span></span>



| <span data-ttu-id="e2134-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2134-139">Requirement</span></span> | <span data-ttu-id="e2134-140">Value</span><span class="sxs-lookup"><span data-stu-id="e2134-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2134-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2134-141">Header</span></span><br/>  | <dl> <span data-ttu-id="e2134-142"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2134-142"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2134-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2134-143">Library</span></span><br/> | <dl> <span data-ttu-id="e2134-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2134-144"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2134-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2134-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2134-146">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="e2134-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="e2134-147">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="e2134-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
