---
description: Obtiene información acerca de una imagen ya cargada en la memoria.
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: Función D3DX10GetImageInfoFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718233"
---
# <a name="d3dx10getimageinfofrommemory-function"></a><span data-ttu-id="3e1f1-103">D3DX10GetImageInfoFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="3e1f1-103">D3DX10GetImageInfoFromMemory function</span></span>

<span data-ttu-id="3e1f1-104">Obtiene información acerca de una imagen ya cargada en la memoria.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-104">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1f1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e1f1-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="3e1f1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e1f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e1f1-107">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e1f1-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f1-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e1f1-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e1f1-109">Puntero a la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-109">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f1-110">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e1f1-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f1-111">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e1f1-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e1f1-112">Tamaño de la imagen en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-112">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f1-113">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e1f1-113">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f1-114">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e1f1-114">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="3e1f1-115">Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-115">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="3e1f1-116">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-116">Can be **NULL**.</span></span> <span data-ttu-id="3e1f1-117">Vea [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="3e1f1-117">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e1f1-118">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e1f1-118">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f1-119">Tipo: **[ **\_ \_ información de imagen de D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e1f1-119">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="3e1f1-120">Información sobre la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-120">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f1-121">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3e1f1-121">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f1-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="3e1f1-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="3e1f1-123">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-123">A pointer to the return value.</span></span> <span data-ttu-id="3e1f1-124">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-124">May be **NULL**.</span></span> <span data-ttu-id="3e1f1-125">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3e1f1-125">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e1f1-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e1f1-126">Return value</span></span>

<span data-ttu-id="3e1f1-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e1f1-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e1f1-128">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3e1f1-128">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e1f1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e1f1-129">Requirements</span></span>



| <span data-ttu-id="3e1f1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e1f1-130">Requirement</span></span> | <span data-ttu-id="3e1f1-131">Value</span><span class="sxs-lookup"><span data-stu-id="3e1f1-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1f1-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e1f1-132">Header</span></span><br/>  | <dl> <span data-ttu-id="3e1f1-133"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e1f1-133"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3e1f1-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e1f1-134">Library</span></span><br/> | <dl> <span data-ttu-id="3e1f1-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e1f1-135"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3e1f1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e1f1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e1f1-137">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="3e1f1-137">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
