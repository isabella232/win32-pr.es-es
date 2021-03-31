---
description: Cree una vista de recursos del sombreador desde un archivo en la memoria.
ms.assetid: 8316987f-75b4-4cee-a1f2-10bee77a28e6
title: Función D3DX10CreateShaderResourceViewFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca3cf26d54d37ab3e3a2141ba7c3e4ea9fdd533f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820986"
---
# <a name="d3dx10createshaderresourceviewfrommemory-function"></a><span data-ttu-id="defdb-103">D3DX10CreateShaderResourceViewFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="defdb-103">D3DX10CreateShaderResourceViewFromMemory function</span></span>

<span data-ttu-id="defdb-104">Cree una vista de recursos del sombreador desde un archivo en la memoria.</span><span class="sxs-lookup"><span data-stu-id="defdb-104">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="defdb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="defdb-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromMemory(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="defdb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="defdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="defdb-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="defdb-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defdb-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="defdb-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="defdb-109">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="defdb-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="defdb-110">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="defdb-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defdb-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="defdb-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="defdb-112">Puntero al archivo en memoria que contiene la vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="defdb-112">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="defdb-113">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="defdb-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defdb-114">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="defdb-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="defdb-115">Tamaño del archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="defdb-115">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="defdb-116">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="defdb-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defdb-117">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="defdb-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="defdb-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="defdb-118">Optional.</span></span> <span data-ttu-id="defdb-119">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="defdb-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="defdb-120">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="defdb-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defdb-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="defdb-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="defdb-122">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="defdb-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="defdb-123">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="defdb-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="defdb-124">*ppShaderResourceView* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="defdb-124">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="defdb-125">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="defdb-125">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="defdb-126">Dirección de un puntero a la vista de recursos del sombreador recién creada.</span><span class="sxs-lookup"><span data-stu-id="defdb-126">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="defdb-127">Consulte la [**interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="defdb-127">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="defdb-128">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="defdb-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="defdb-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="defdb-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="defdb-130">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="defdb-130">A pointer to the return value.</span></span> <span data-ttu-id="defdb-131">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="defdb-131">May be **NULL**.</span></span> <span data-ttu-id="defdb-132">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="defdb-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="defdb-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="defdb-133">Return value</span></span>

<span data-ttu-id="defdb-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="defdb-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="defdb-135">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="defdb-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="defdb-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="defdb-136">Requirements</span></span>



| <span data-ttu-id="defdb-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="defdb-137">Requirement</span></span> | <span data-ttu-id="defdb-138">Value</span><span class="sxs-lookup"><span data-stu-id="defdb-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="defdb-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="defdb-139">Header</span></span><br/>  | <dl> <span data-ttu-id="defdb-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="defdb-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="defdb-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="defdb-141">Library</span></span><br/> | <dl> <span data-ttu-id="defdb-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="defdb-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="defdb-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="defdb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defdb-144">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="defdb-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="defdb-145">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="defdb-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
