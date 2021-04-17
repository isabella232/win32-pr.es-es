---
description: Calcula la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica.
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'ID3DXPRTEngine:: ComputeDirectLightingSH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708113"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a><span data-ttu-id="839d8-103">ID3DXPRTEngine:: ComputeDirectLightingSH (método)</span><span class="sxs-lookup"><span data-stu-id="839d8-103">ID3DXPRTEngine::ComputeDirectLightingSH method</span></span>

<span data-ttu-id="839d8-104">Calcula la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica.</span><span class="sxs-lookup"><span data-stu-id="839d8-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span>

## <a name="syntax"></a><span data-ttu-id="839d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="839d8-105">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="839d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="839d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="839d8-107">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="839d8-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="839d8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="839d8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="839d8-109">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="839d8-109">Order of the SH evaluation.</span></span> <span data-ttu-id="839d8-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="839d8-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="839d8-111">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="839d8-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="839d8-112">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="839d8-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="839d8-113">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="839d8-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="839d8-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="839d8-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="839d8-115">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela la contribución de iluminación directa con la aproximación SH.</span><span class="sxs-lookup"><span data-stu-id="839d8-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution with the SH approximation.</span></span> <span data-ttu-id="839d8-116">Este búfer debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="839d8-116">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="839d8-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="839d8-117">Return value</span></span>

<span data-ttu-id="839d8-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="839d8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="839d8-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="839d8-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="839d8-120">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="839d8-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="839d8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="839d8-121">Remarks</span></span>

<span data-ttu-id="839d8-122">La salida no incluye albedo y solo la luz entrante está integrada en el simulador.</span><span class="sxs-lookup"><span data-stu-id="839d8-122">The output does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="839d8-123">Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.</span><span class="sxs-lookup"><span data-stu-id="839d8-123">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="839d8-124">Llame a [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de transferencia de Radiance previamente calculado (PRT) por Albedo.</span><span class="sxs-lookup"><span data-stu-id="839d8-124">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="839d8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="839d8-125">Requirements</span></span>



| <span data-ttu-id="839d8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="839d8-126">Requirement</span></span> | <span data-ttu-id="839d8-127">Value</span><span class="sxs-lookup"><span data-stu-id="839d8-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="839d8-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="839d8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="839d8-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="839d8-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="839d8-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="839d8-130">Library</span></span><br/> | <dl> <span data-ttu-id="839d8-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="839d8-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="839d8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="839d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839d8-133">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="839d8-133">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
