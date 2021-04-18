---
description: Cree un procesador de datos para usarlo con un bombeo de subprocesos.
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: Función D3DX10CreateAsyncTextureInfoProcessor (D3DX10Tex. h)
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
ms.openlocfilehash: fe56fc217af6ebae9255b4f72d3c3af2f279fa29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718428"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a><span data-ttu-id="4b652-103">D3DX10CreateAsyncTextureInfoProcessor función)</span><span class="sxs-lookup"><span data-stu-id="4b652-103">D3DX10CreateAsyncTextureInfoProcessor function</span></span>

<span data-ttu-id="4b652-104">Cree un procesador de datos para usarlo con un [**bombeo de subprocesos**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="4b652-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b652-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b652-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="4b652-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b652-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b652-107">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b652-107">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b652-108">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b652-108">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="4b652-109">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4b652-109">Optional.</span></span> <span data-ttu-id="4b652-110">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="4b652-110">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="4b652-111">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b652-111">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b652-112">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4b652-112">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="4b652-113">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="4b652-113">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b652-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b652-114">Return value</span></span>

<span data-ttu-id="4b652-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b652-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b652-116">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4b652-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b652-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b652-117">Remarks</span></span>

<span data-ttu-id="4b652-118">Esta API crea una interfaz de procesador de datos; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) crea la interfaz del procesador de datos y carga la textura.</span><span class="sxs-lookup"><span data-stu-id="4b652-118">This API does creates a data-processor interface; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b652-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b652-119">Requirements</span></span>



| <span data-ttu-id="4b652-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b652-120">Requirement</span></span> | <span data-ttu-id="4b652-121">Value</span><span class="sxs-lookup"><span data-stu-id="4b652-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b652-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b652-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4b652-123"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b652-123"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4b652-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b652-124">Library</span></span><br/> | <dl> <span data-ttu-id="4b652-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b652-125"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4b652-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b652-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b652-127">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="4b652-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




