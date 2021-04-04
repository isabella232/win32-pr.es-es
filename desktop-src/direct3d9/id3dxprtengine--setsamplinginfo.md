---
description: Establece las propiedades de muestreo utilizadas por el simulador Radiance Transfer (PRT) precalculado.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine:: SetSamplingInfo (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821191"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a><span data-ttu-id="02f11-103">ID3DXPRTEngine:: SetSamplingInfo (método)</span><span class="sxs-lookup"><span data-stu-id="02f11-103">ID3DXPRTEngine::SetSamplingInfo method</span></span>

<span data-ttu-id="02f11-104">Establece las propiedades de muestreo utilizadas por el simulador Radiance Transfer (PRT) precalculado.</span><span class="sxs-lookup"><span data-stu-id="02f11-104">Sets sampling properties used by the precomputed radiance transfer (PRT) simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f11-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02f11-105">Syntax</span></span>


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a><span data-ttu-id="02f11-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02f11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f11-107">*NumRays* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02f11-107">*NumRays* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f11-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02f11-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02f11-109">Número de rayos de luz que se dirigen a cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="02f11-109">Number of light rays to direct at each sample.</span></span> <span data-ttu-id="02f11-110">Debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="02f11-110">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="02f11-111">*UseSphere* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02f11-111">*UseSphere* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f11-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02f11-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02f11-113">Si **es true**, los ejemplos se calcularán en una esfera completa.</span><span class="sxs-lookup"><span data-stu-id="02f11-113">If **TRUE**, samples will be computed over a full sphere.</span></span> <span data-ttu-id="02f11-114">Si **es false**, los ejemplos se calcularán sobre un hemisferio.</span><span class="sxs-lookup"><span data-stu-id="02f11-114">If **FALSE**, samples will be computed over a hemisphere.</span></span>

</dd> <dt>

<span data-ttu-id="02f11-115">*UseCosine* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02f11-115">*UseCosine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f11-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02f11-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02f11-117">Si **es true**, se usa una ponderación de muestras de coseno.</span><span class="sxs-lookup"><span data-stu-id="02f11-117">If **TRUE**, use a cosine weighting of samples.</span></span> <span data-ttu-id="02f11-118">Si tanto UseCosine como UseSphere son **true**, se producirá un error en el método y se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="02f11-118">If both UseCosine and UseSphere are **TRUE**, the method will fail and an error will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="02f11-119">*Adaptable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02f11-119">*Adaptive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f11-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02f11-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02f11-121">Debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="02f11-121">Must be **FALSE**.</span></span> <span data-ttu-id="02f11-122">El muestreo adaptable no está implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="02f11-122">Adaptive sampling is currently not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="02f11-123">*AdaptiveThresh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02f11-123">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f11-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02f11-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02f11-125">ignorado.</span><span class="sxs-lookup"><span data-stu-id="02f11-125">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02f11-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02f11-126">Return value</span></span>

<span data-ttu-id="02f11-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02f11-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02f11-128">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02f11-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="02f11-129">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, e \_ NOTIMPL e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="02f11-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f11-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02f11-130">Requirements</span></span>



| <span data-ttu-id="02f11-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="02f11-131">Requirement</span></span> | <span data-ttu-id="02f11-132">Value</span><span class="sxs-lookup"><span data-stu-id="02f11-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02f11-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02f11-133">Header</span></span><br/>  | <dl> <span data-ttu-id="02f11-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="02f11-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="02f11-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02f11-135">Library</span></span><br/> | <dl> <span data-ttu-id="02f11-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02f11-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02f11-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="02f11-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f11-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="02f11-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
