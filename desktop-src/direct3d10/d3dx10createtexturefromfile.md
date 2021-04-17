---
description: Cree un recurso de textura a partir de un archivo.
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: Función D3DX10CreateTextureFromFile (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698298"
---
# <a name="d3dx10createtexturefromfile-function"></a><span data-ttu-id="1df56-103">D3DX10CreateTextureFromFile función)</span><span class="sxs-lookup"><span data-stu-id="1df56-103">D3DX10CreateTextureFromFile function</span></span>

<span data-ttu-id="1df56-104">Cree un recurso de textura a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="1df56-104">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df56-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1df56-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="1df56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1df56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1df56-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1df56-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df56-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1df56-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1df56-109">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="1df56-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1df56-110">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1df56-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df56-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1df56-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1df56-112">Nombre del archivo que contiene el recurso.</span><span class="sxs-lookup"><span data-stu-id="1df56-112">The name of the file containing the resource.</span></span> <span data-ttu-id="1df56-113">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1df56-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1df56-114">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1df56-114">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="1df56-115">Consulte enumeración de [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md) para obtener una lista de los formatos de archivo de imagen compatibles.</span><span class="sxs-lookup"><span data-stu-id="1df56-115">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md) enumeration for a list of the supported image file formats.</span></span>

</dd> <dt>

<span data-ttu-id="1df56-116">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1df56-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df56-117">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1df56-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="1df56-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1df56-118">Optional.</span></span> <span data-ttu-id="1df56-119">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="1df56-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="1df56-120">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1df56-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df56-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1df56-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="1df56-122">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1df56-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="1df56-123">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="1df56-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="1df56-124">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1df56-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1df56-125">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="1df56-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="1df56-126">La dirección de un puntero al recurso de textura (vea la [**interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="1df56-126">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="1df56-127">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1df56-127">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1df56-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1df56-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1df56-129">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1df56-129">A pointer to the return value.</span></span> <span data-ttu-id="1df56-130">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1df56-130">May be **NULL**.</span></span> <span data-ttu-id="1df56-131">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1df56-131">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1df56-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1df56-132">Return value</span></span>

<span data-ttu-id="1df56-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1df56-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1df56-134">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1df56-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1df56-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1df56-135">Remarks</span></span>

<span data-ttu-id="1df56-136">Para obtener una lista de formatos de imagen admitidos, consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="1df56-136">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1df56-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1df56-137">Requirements</span></span>



| <span data-ttu-id="1df56-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1df56-138">Requirement</span></span> | <span data-ttu-id="1df56-139">Value</span><span class="sxs-lookup"><span data-stu-id="1df56-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1df56-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1df56-140">Header</span></span><br/>  | <dl> <span data-ttu-id="1df56-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1df56-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1df56-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1df56-142">Library</span></span><br/> | <dl> <span data-ttu-id="1df56-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1df56-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df56-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1df56-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df56-145">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="1df56-145">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="1df56-146">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="1df56-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
