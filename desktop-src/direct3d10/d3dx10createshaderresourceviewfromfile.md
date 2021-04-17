---
description: Cree una vista de recursos del sombreador a partir de un archivo.
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: Función D3DX10CreateShaderResourceViewFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb787bed64d16f7593fba1f97c96ceeaa217b4e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424428"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a><span data-ttu-id="0cfa5-103">D3DX10CreateShaderResourceViewFromFile función)</span><span class="sxs-lookup"><span data-stu-id="0cfa5-103">D3DX10CreateShaderResourceViewFromFile function</span></span>

<span data-ttu-id="0cfa5-104">Cree una vista de recursos del sombreador a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-104">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfa5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cfa5-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0cfa5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cfa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfa5-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cfa5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa5-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="0cfa5-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="0cfa5-109">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa5-110">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cfa5-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa5-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cfa5-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cfa5-112">Nombre del archivo que contiene la vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-112">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="0cfa5-113">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0cfa5-114">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-114">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa5-115">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cfa5-115">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa5-116">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cfa5-116">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="0cfa5-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-117">Optional.</span></span> <span data-ttu-id="0cfa5-118">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-118">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa5-119">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cfa5-119">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa5-120">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cfa5-120">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0cfa5-121">Puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="0cfa5-121">Pointer to a thread-pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="0cfa5-122">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-122">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="0cfa5-123">*ppShaderResourceView* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0cfa5-123">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa5-124">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="0cfa5-124">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="0cfa5-125">Dirección de un puntero a la vista de recursos del sombreador (vea la [**interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="0cfa5-125">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="0cfa5-126">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0cfa5-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfa5-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0cfa5-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0cfa5-128">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-128">A pointer to the return value.</span></span> <span data-ttu-id="0cfa5-129">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-129">May be **NULL**.</span></span> <span data-ttu-id="0cfa5-130">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="0cfa5-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfa5-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cfa5-131">Return value</span></span>

<span data-ttu-id="0cfa5-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cfa5-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cfa5-133">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0cfa5-133">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0cfa5-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cfa5-134">Remarks</span></span>

<span data-ttu-id="0cfa5-135">Para obtener una lista de formatos de imagen compatibles, consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="0cfa5-135">For a list of supported image formats, see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfa5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cfa5-136">Requirements</span></span>



| <span data-ttu-id="0cfa5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cfa5-137">Requirement</span></span> | <span data-ttu-id="0cfa5-138">Value</span><span class="sxs-lookup"><span data-stu-id="0cfa5-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfa5-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cfa5-139">Header</span></span><br/>  | <dl> <span data-ttu-id="0cfa5-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfa5-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0cfa5-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cfa5-141">Library</span></span><br/> | <dl> <span data-ttu-id="0cfa5-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cfa5-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0cfa5-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cfa5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfa5-144">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="0cfa5-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="0cfa5-145">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="0cfa5-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
