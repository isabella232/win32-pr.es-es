---
description: Cree una vista de recursos del sombreador desde un recurso.
ms.assetid: 207cda5f-5b7e-420a-988f-135cd2a04eb0
title: Función D3DX10CreateShaderResourceViewFromResource (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 12de92153b6f812b4f014f53e918e7a97000eda6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707941"
---
# <a name="d3dx10createshaderresourceviewfromresource-function"></a><span data-ttu-id="46e8f-103">D3DX10CreateShaderResourceViewFromResource función)</span><span class="sxs-lookup"><span data-stu-id="46e8f-103">D3DX10CreateShaderResourceViewFromResource function</span></span>

<span data-ttu-id="46e8f-104">Cree una vista de recursos del sombreador desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="46e8f-104">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46e8f-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromResource(
  _In_  ID3D10Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="46e8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46e8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e8f-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46e8f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e8f-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="46e8f-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="46e8f-109">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="46e8f-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="46e8f-110">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46e8f-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e8f-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46e8f-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46e8f-112">Identificador del módulo de recursos que contiene la vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="46e8f-112">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="46e8f-113">HMODULE se puede obtener con la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="46e8f-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="46e8f-114">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46e8f-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e8f-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46e8f-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46e8f-116">Nombre de la vista de recursos del sombreador en hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="46e8f-116">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="46e8f-117">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="46e8f-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="46e8f-118">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="46e8f-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="46e8f-119">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46e8f-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e8f-120">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="46e8f-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="46e8f-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="46e8f-121">Optional.</span></span> <span data-ttu-id="46e8f-122">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="46e8f-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="46e8f-123">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46e8f-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e8f-124">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="46e8f-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="46e8f-125">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="46e8f-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="46e8f-126">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="46e8f-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="46e8f-127">*ppShaderResourceView* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46e8f-127">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e8f-128">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="46e8f-128">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="46e8f-129">Dirección de un puntero a la vista de recursos del sombreador (vea la [**interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="46e8f-129">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="46e8f-130">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46e8f-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e8f-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="46e8f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="46e8f-132">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="46e8f-132">A pointer to the return value.</span></span> <span data-ttu-id="46e8f-133">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="46e8f-133">May be **NULL**.</span></span> <span data-ttu-id="46e8f-134">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="46e8f-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e8f-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46e8f-135">Return value</span></span>

<span data-ttu-id="46e8f-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46e8f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46e8f-137">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="46e8f-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46e8f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e8f-138">Requirements</span></span>



| <span data-ttu-id="46e8f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e8f-139">Requirement</span></span> | <span data-ttu-id="46e8f-140">Value</span><span class="sxs-lookup"><span data-stu-id="46e8f-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e8f-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46e8f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="46e8f-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="46e8f-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="46e8f-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46e8f-143">Library</span></span><br/> | <dl> <span data-ttu-id="46e8f-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46e8f-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="46e8f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="46e8f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e8f-146">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="46e8f-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="46e8f-147">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="46e8f-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
