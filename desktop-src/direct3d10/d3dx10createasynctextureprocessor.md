---
description: Cree un procesador de datos para usarlo con un bombeo de subprocesos.
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Función D3DX10CreateAsyncTextureProcessor (D3DX10Tex. h)
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
ms.openlocfilehash: d1d9c61729e72cc4ae5432361e9c1d968551b9c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083780"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="5d4e5-103">D3DX10CreateAsyncTextureProcessor función)</span><span class="sxs-lookup"><span data-stu-id="5d4e5-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="5d4e5-104">Cree un procesador de datos para usarlo con un [**bombeo de subprocesos**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="5d4e5-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d4e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d4e5-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="5d4e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d4e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d4e5-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d4e5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4e5-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="5d4e5-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="5d4e5-109">Un puntero a devive (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="5d4e5-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="5d4e5-110">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d4e5-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4e5-111">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d4e5-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="5d4e5-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5d4e5-112">Optional.</span></span> <span data-ttu-id="5d4e5-113">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="5d4e5-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5d4e5-114">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d4e5-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4e5-115">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d4e5-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="5d4e5-116">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="5d4e5-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d4e5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d4e5-117">Return value</span></span>

<span data-ttu-id="5d4e5-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d4e5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d4e5-119">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5d4e5-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d4e5-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d4e5-120">Remarks</span></span>

<span data-ttu-id="5d4e5-121">Esta API crea una interfaz de procesador de datos y carga la textura; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) crea la interfaz del procesador de datos.</span><span class="sxs-lookup"><span data-stu-id="5d4e5-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4e5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d4e5-122">Requirements</span></span>



| <span data-ttu-id="5d4e5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d4e5-123">Requirement</span></span> | <span data-ttu-id="5d4e5-124">Value</span><span class="sxs-lookup"><span data-stu-id="5d4e5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4e5-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d4e5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5d4e5-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d4e5-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5d4e5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d4e5-127">Library</span></span><br/> | <dl> <span data-ttu-id="5d4e5-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d4e5-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5d4e5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d4e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d4e5-130">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="5d4e5-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




