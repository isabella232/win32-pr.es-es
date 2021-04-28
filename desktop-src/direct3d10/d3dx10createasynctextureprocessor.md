---
description: 'Función D3DX10CreateAsyncTextureProcessor: cree un procesador de datos que se usará con una bomba de subprocesos.'
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Función D3DX10CreateAsyncTextureProcessor (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e75ab6b796f23399b453a6c7eebfe0d40e3b7b49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102793"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="ddc91-103">Función D3DX10CreateAsyncTextureProcessor</span><span class="sxs-lookup"><span data-stu-id="ddc91-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="ddc91-104">Cree un procesador de datos que se usará con una bomba [**de subprocesos**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="ddc91-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc91-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddc91-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="ddc91-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddc91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc91-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ddc91-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc91-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="ddc91-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="ddc91-109">Puntero a la interfaz devive [**(vea ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="ddc91-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="ddc91-110">*pLoadInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ddc91-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc91-111">Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddc91-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="ddc91-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ddc91-112">Optional.</span></span> <span data-ttu-id="ddc91-113">Identifica las características de una textura (vea [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; esta opción se establece en **NULL** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="ddc91-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ddc91-114">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ddc91-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc91-115">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ddc91-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="ddc91-116">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="ddc91-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc91-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddc91-117">Return value</span></span>

<span data-ttu-id="ddc91-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddc91-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddc91-119">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="ddc91-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ddc91-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddc91-120">Remarks</span></span>

<span data-ttu-id="ddc91-121">Esta API crea una interfaz de procesador de datos y carga la textura; [**D3DX10CreateAsyncTextureInfoProcessor crea**](d3dx10createasynctextureinfoprocessor.md) la interfaz del procesador de datos.</span><span class="sxs-lookup"><span data-stu-id="ddc91-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc91-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddc91-122">Requirements</span></span>



| <span data-ttu-id="ddc91-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc91-123">Requirement</span></span> | <span data-ttu-id="ddc91-124">Value</span><span class="sxs-lookup"><span data-stu-id="ddc91-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc91-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddc91-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ddc91-126"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="ddc91-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ddc91-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddc91-127">Library</span></span><br/> | <dl> <span data-ttu-id="ddc91-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddc91-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ddc91-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ddc91-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc91-130">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="ddc91-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




