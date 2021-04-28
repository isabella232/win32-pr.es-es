---
description: 'Función D3DX10CreateAsyncTextureInfoProcessor: cree un procesador de datos que se usará con una bomba de subprocesos.'
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: Función D3DX10CreateAsyncTextureInfoProcessor (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a23c2062c5f17e00d03161483d3ab1cf2ff225d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102803"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a><span data-ttu-id="e05c0-103">Función D3DX10CreateAsyncTextureInfoProcessor</span><span class="sxs-lookup"><span data-stu-id="e05c0-103">D3DX10CreateAsyncTextureInfoProcessor function</span></span>

<span data-ttu-id="e05c0-104">Cree un procesador de datos que se usará con una bomba [**de subprocesos**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="e05c0-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e05c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e05c0-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="e05c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e05c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05c0-107">*pLoadInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e05c0-107">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05c0-108">Tipo: **[ **INFORMACIÓN DE CARGA DE \_ IMÁGENES \_ \_ D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e05c0-108">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="e05c0-109">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e05c0-109">Optional.</span></span> <span data-ttu-id="e05c0-110">Identifica las características de una textura (vea [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; esta opción se establece en **NULL** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="e05c0-110">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e05c0-111">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e05c0-111">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e05c0-112">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e05c0-112">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="e05c0-113">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="e05c0-113">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e05c0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e05c0-114">Return value</span></span>

<span data-ttu-id="e05c0-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e05c0-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e05c0-116">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="e05c0-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e05c0-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e05c0-117">Remarks</span></span>

<span data-ttu-id="e05c0-118">Esta API crea una interfaz de procesador de datos; [**D3DX10CreateAsyncTextureProcessor crea**](d3dx10createasynctextureprocessor.md) la interfaz del procesador de datos y carga la textura.</span><span class="sxs-lookup"><span data-stu-id="e05c0-118">This API does creates a data-processor interface; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="e05c0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e05c0-119">Requirements</span></span>



| <span data-ttu-id="e05c0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e05c0-120">Requirement</span></span> | <span data-ttu-id="e05c0-121">Value</span><span class="sxs-lookup"><span data-stu-id="e05c0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e05c0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e05c0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e05c0-123"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="e05c0-123"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e05c0-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e05c0-124">Library</span></span><br/> | <dl> <span data-ttu-id="e05c0-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e05c0-125"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e05c0-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e05c0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05c0-127">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="e05c0-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




