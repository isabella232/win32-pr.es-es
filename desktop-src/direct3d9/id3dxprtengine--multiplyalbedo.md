---
description: Multiplica cada vector de transferencia Radiance (PRT) precalculado por el albedo por vértice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine:: MultiplyAlbedo (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708049"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a><span data-ttu-id="208b3-103">ID3DXPRTEngine:: MultiplyAlbedo (método)</span><span class="sxs-lookup"><span data-stu-id="208b3-103">ID3DXPRTEngine::MultiplyAlbedo method</span></span>

<span data-ttu-id="208b3-104">Multiplica cada vector de transferencia Radiance (PRT) precalculado por el albedo por vértice.</span><span class="sxs-lookup"><span data-stu-id="208b3-104">Multiplies each precomputed radiance transfer (PRT) vector by the per-vertex albedo.</span></span>

## <a name="syntax"></a><span data-ttu-id="208b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="208b3-105">Syntax</span></span>


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="208b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="208b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="208b3-107">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="208b3-107">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="208b3-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="208b3-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="208b3-109">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que contendrá vectores PRT multiplicado por el albedo por vértice.</span><span class="sxs-lookup"><span data-stu-id="208b3-109">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will contain PRT vectors multiplied by the per-vertex albedo.</span></span> <span data-ttu-id="208b3-110">Si este búfer de salida es un objeto de textura, se debe tener cuidado para almacenar el albedo de la textura con la misma resolución que el búfer de simulación.</span><span class="sxs-lookup"><span data-stu-id="208b3-110">If this output buffer is a texture object, then care must be taken to store the albedo of the texture at the same resolution as the simulation buffer.</span></span> <span data-ttu-id="208b3-111">Puede establecer la resolución adecuada en Albedo con [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)y aplicar regiones de medianil de texturas si es necesario.</span><span class="sxs-lookup"><span data-stu-id="208b3-111">You can set the proper resolution on the albedo with [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applying texture gutter regions if appropriate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="208b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="208b3-112">Return value</span></span>

<span data-ttu-id="208b3-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="208b3-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="208b3-114">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="208b3-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="208b3-115">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="208b3-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="208b3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="208b3-116">Remarks</span></span>

<span data-ttu-id="208b3-117">Los métodos ID3DXPRTEngine:: Computexxx calculan los búferes de salida en los que la señal luminosa no se ha multiplicado por Albedo.</span><span class="sxs-lookup"><span data-stu-id="208b3-117">The ID3DXPRTEngine::Computexxx methods compute output buffers in which the light signal has not been multiplied by albedo.</span></span> <span data-ttu-id="208b3-118">Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.</span><span class="sxs-lookup"><span data-stu-id="208b3-118">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="208b3-119">Para incluir Albedo en el modelo representado-Light, llame a este método después de uno de los métodos Computexxx.</span><span class="sxs-lookup"><span data-stu-id="208b3-119">To include albedo in the rendered-light model, call this method after one of the Computexxx methods.</span></span>

<span data-ttu-id="208b3-120">Se debe llamar a [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="208b3-120">[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) should be called before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="208b3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="208b3-121">Requirements</span></span>



| <span data-ttu-id="208b3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="208b3-122">Requirement</span></span> | <span data-ttu-id="208b3-123">Value</span><span class="sxs-lookup"><span data-stu-id="208b3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="208b3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="208b3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="208b3-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="208b3-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="208b3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="208b3-126">Library</span></span><br/> | <dl> <span data-ttu-id="208b3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="208b3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="208b3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="208b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208b3-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="208b3-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="208b3-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="208b3-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




