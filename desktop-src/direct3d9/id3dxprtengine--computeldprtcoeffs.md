---
description: Calcula los coeficientes de transferencia de Radiance precalculados (LDPRT) precalculados de forma local en relación con los vectores normales de cada muestra para minimizar el error de menos cuadrados con respecto a los datos de ID3DXPRTBuffer de entrada.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine:: ComputeLDPRTCoeffs (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718550"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a><span data-ttu-id="e30f7-103">ID3DXPRTEngine:: ComputeLDPRTCoeffs (método)</span><span class="sxs-lookup"><span data-stu-id="e30f7-103">ID3DXPRTEngine::ComputeLDPRTCoeffs method</span></span>

<span data-ttu-id="e30f7-104">Calcula los coeficientes de transferencia de Radiance precalculados (LDPRT) precalculados de forma local en relación con los vectores normales de cada muestra para minimizar el error de menos cuadrados con respecto a los datos de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="e30f7-104">Computes locally-deformable precomputed radiance transfer (LDPRT) coefficients relative to per-sample normal vectors to minimize the least-squares error with respect to input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) data.</span></span> <span data-ttu-id="e30f7-105">Estos coeficientes se pueden usar con vectores normales con o sin máscaras para modelar los efectos globales en los objetos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="e30f7-105">These coefficients can be used with skinned or transformed normal vectors to model global effects on dynamic objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="e30f7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e30f7-106">Syntax</span></span>


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="e30f7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e30f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e30f7-108">*pDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e30f7-108">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30f7-109">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e30f7-109">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e30f7-110">Puntero a un objeto de datos de Radiance (PRT) precalculado [**ID3DXPRTBuffer**](id3dxprtbuffer.md) esférico (SH) de entrada.</span><span class="sxs-lookup"><span data-stu-id="e30f7-110">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) spherical harmonic (SH) precomputed radiance transfer (PRT) data object.</span></span>

</dd> <dt>

<span data-ttu-id="e30f7-111">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e30f7-111">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30f7-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e30f7-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e30f7-113">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="e30f7-113">Order of the SH evaluation.</span></span> <span data-ttu-id="e30f7-114">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="e30f7-114">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e30f7-115">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="e30f7-115">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e30f7-116">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="e30f7-116">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e30f7-117">*pNormOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e30f7-117">*pNormOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e30f7-118">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e30f7-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e30f7-119">Matriz vector opcional que se va a rellenar con vectores normales de sombreador óptimo para los que se optimizan los coeficientes de LDPRT.</span><span class="sxs-lookup"><span data-stu-id="e30f7-119">Optional vector array to be filled with shader-optimal normal vectors for which LDPRT coefficients are optimized.</span></span> <span data-ttu-id="e30f7-120">Esta matriz debe tener el mismo tamaño que el número de muestras de pDataIn.</span><span class="sxs-lookup"><span data-stu-id="e30f7-120">This array must be the same size as the number of samples in pDataIn.</span></span> <span data-ttu-id="e30f7-121">Si **es null**, se usan vectores normales de superficie.</span><span class="sxs-lookup"><span data-stu-id="e30f7-121">If **NULL**, surface normal vectors are used.</span></span>

</dd> <dt>

<span data-ttu-id="e30f7-122">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e30f7-122">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e30f7-123">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e30f7-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e30f7-124">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que contiene los coeficientes armónicos de orden de pedido por canal de color por muestra.</span><span class="sxs-lookup"><span data-stu-id="e30f7-124">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that contains Order zonal harmonic coefficients per color channel per sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e30f7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e30f7-125">Return value</span></span>

<span data-ttu-id="e30f7-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e30f7-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e30f7-127">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e30f7-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e30f7-128">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e30f7-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e30f7-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e30f7-129">Remarks</span></span>

<span data-ttu-id="e30f7-130">Las soluciones para los vectores normales de sombreado se pueden obtener opcionalmente con este método.</span><span class="sxs-lookup"><span data-stu-id="e30f7-130">Solutions for shading normal vectors can optionally be obtained with this method.</span></span> <span data-ttu-id="e30f7-131">Estos vectores normales, junto con los coeficientes de LDPRT, pueden representar con mayor precisión la señal de PRT.</span><span class="sxs-lookup"><span data-stu-id="e30f7-131">These normal vectors, along with the LDPRT coefficients, can more accurately represent the PRT signal.</span></span> <span data-ttu-id="e30f7-132">En este caso, los coeficientes representan armónicos de zona orientados en la dirección normal.</span><span class="sxs-lookup"><span data-stu-id="e30f7-132">In this case, the coefficients represent zonal harmonics oriented in the normal direction.</span></span>

<span data-ttu-id="e30f7-133">Este método no se puede usar con los resultados de [**ID3DXPRTEngine:: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) o [**ID3DXPRTEngine:: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span><span class="sxs-lookup"><span data-stu-id="e30f7-133">This method cannot be used with results from [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) or [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e30f7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e30f7-134">Requirements</span></span>



| <span data-ttu-id="e30f7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e30f7-135">Requirement</span></span> | <span data-ttu-id="e30f7-136">Value</span><span class="sxs-lookup"><span data-stu-id="e30f7-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e30f7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e30f7-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e30f7-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e30f7-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e30f7-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e30f7-139">Library</span></span><br/> | <dl> <span data-ttu-id="e30f7-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e30f7-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e30f7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e30f7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e30f7-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e30f7-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
