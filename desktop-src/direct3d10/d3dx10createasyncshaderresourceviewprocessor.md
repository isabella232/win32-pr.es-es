---
description: Cree un procesador de datos que cargue un recurso y, a continuación, cree una vista de recursos del sombreador para él. Los procesadores de datos son un componente de la característica de carga asincrónica de datos de D3DX10 que usa los bombeos de subprocesos.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: Función D3DX10CreateAsyncShaderResourceViewProcessor (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718429"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="2f206-104">D3DX10CreateAsyncShaderResourceViewProcessor función)</span><span class="sxs-lookup"><span data-stu-id="2f206-104">D3DX10CreateAsyncShaderResourceViewProcessor function</span></span>

<span data-ttu-id="2f206-105">Cree un procesador de datos que cargue un recurso y, a continuación, cree una vista de recursos del sombreador para él.</span><span class="sxs-lookup"><span data-stu-id="2f206-105">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="2f206-106">Los procesadores de datos son un componente de la característica de carga asincrónica de datos de D3DX10 que usa los [**bombeos de subprocesos**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="2f206-106">Data processors are a component of the asynchronous data loading feature in D3DX10 that uses [**thread pumps**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f206-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f206-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="2f206-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f206-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f206-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f206-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f206-110">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="2f206-110">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="2f206-111">Puntero al dispositivo Direct3D (consulte la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que se usará para crear un recurso y una vista de recursos del sombreador para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="2f206-111">Pointer to the Direct3D device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="2f206-112">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f206-112">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f206-113">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f206-113">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="2f206-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2f206-114">Optional.</span></span> <span data-ttu-id="2f206-115">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="2f206-115">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="2f206-116">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2f206-116">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f206-117">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2f206-117">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="2f206-118">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="2f206-118">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f206-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f206-119">Return value</span></span>

<span data-ttu-id="2f206-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f206-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f206-121">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2f206-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f206-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f206-122">Requirements</span></span>



| <span data-ttu-id="2f206-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f206-123">Requirement</span></span> | <span data-ttu-id="2f206-124">Value</span><span class="sxs-lookup"><span data-stu-id="2f206-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f206-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f206-125">Header</span></span><br/> | <dl> <span data-ttu-id="2f206-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f206-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f206-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f206-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f206-128">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="2f206-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




