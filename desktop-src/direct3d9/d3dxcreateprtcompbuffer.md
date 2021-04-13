---
description: Crea un búfer de transferencia de Radiance (PRT) comprimido previamente a partir de un objeto ID3DXPRTBuffer no comprimido. Esta función debe usarse con búferes de volumen o por vértices.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Función D3DXCreatePRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362583"
---
# <a name="d3dxcreateprtcompbuffer-function"></a><span data-ttu-id="43f5f-104">D3DXCreatePRTCompBuffer función)</span><span class="sxs-lookup"><span data-stu-id="43f5f-104">D3DXCreatePRTCompBuffer function</span></span>

<span data-ttu-id="43f5f-105">Crea un búfer de transferencia de Radiance (PRT) comprimido previamente a partir de un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) no comprimido.</span><span class="sxs-lookup"><span data-stu-id="43f5f-105">Creates a compressed precomputed radiance transfer (PRT) buffer from an uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="43f5f-106">Esta función debe usarse con búferes de volumen o por vértices.</span><span class="sxs-lookup"><span data-stu-id="43f5f-106">This function should be used with per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f5f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43f5f-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="43f5f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43f5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f5f-109">*Calidad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="43f5f-109">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5f-110">Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span><span class="sxs-lookup"><span data-stu-id="43f5f-110">Type: **[**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span></span>

<span data-ttu-id="43f5f-111">Calidad de la compresión armónica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="43f5f-111">Quality of spherical harmonic (SH) compression.</span></span> <span data-ttu-id="43f5f-112">Vea [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span><span class="sxs-lookup"><span data-stu-id="43f5f-112">See [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span></span>

</dd> <dt>

<span data-ttu-id="43f5f-113">*NumClusters* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43f5f-113">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5f-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43f5f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43f5f-115">Número de clústeres que se usarán para la compresión.</span><span class="sxs-lookup"><span data-stu-id="43f5f-115">Number of clusters to use for compression.</span></span>

</dd> <dt>

<span data-ttu-id="43f5f-116">*NumPCA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43f5f-116">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5f-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43f5f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43f5f-118">Número de vectores de base del análisis de componentes principales (PCA) que se van a usar en cada clúster.</span><span class="sxs-lookup"><span data-stu-id="43f5f-118">Number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span>

</dd> <dt>

<span data-ttu-id="43f5f-119">*pCB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43f5f-119">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5f-120">Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="43f5f-120">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="43f5f-121">Puntero opcional a la función de devolución de llamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que se usa para calcular el porcentaje de los cálculos de compresión de PRT completados.</span><span class="sxs-lookup"><span data-stu-id="43f5f-121">Optional pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that is used to compute the percentage of PRT compression computations completed.</span></span> <span data-ttu-id="43f5f-122">La función de devolución de llamada debe implementarse para devolver \_ los valores correctos para seguir ejecutando la rutina de compresión.</span><span class="sxs-lookup"><span data-stu-id="43f5f-122">The callback function must be implemented to return S\_OK to keep running the compression routine.</span></span> <span data-ttu-id="43f5f-123">Cualquier otro valor detendrá la compresión.</span><span class="sxs-lookup"><span data-stu-id="43f5f-123">Any other value will halt compression.</span></span> <span data-ttu-id="43f5f-124">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="43f5f-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43f5f-125">*lpUserContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43f5f-125">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5f-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43f5f-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43f5f-127">Puntero opcional a un valor definido por el usuario que se pasa a la función de devolución de llamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) .</span><span class="sxs-lookup"><span data-stu-id="43f5f-127">Optional pointer to a user-defined value passed to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function.</span></span> <span data-ttu-id="43f5f-128">Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="43f5f-128">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span> <span data-ttu-id="43f5f-129">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="43f5f-129">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43f5f-130">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43f5f-130">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5f-131">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="43f5f-131">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="43f5f-132">Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) sin comprimir que se comprimirá.</span><span class="sxs-lookup"><span data-stu-id="43f5f-132">Address of a pointer to the uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="43f5f-133">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="43f5f-133">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5f-134">Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="43f5f-134">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="43f5f-135">Dirección de un puntero al objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="43f5f-135">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f5f-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43f5f-136">Return value</span></span>

<span data-ttu-id="43f5f-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43f5f-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43f5f-138">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43f5f-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="43f5f-139">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="43f5f-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f5f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43f5f-140">Requirements</span></span>



| <span data-ttu-id="43f5f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f5f-141">Requirement</span></span> | <span data-ttu-id="43f5f-142">Value</span><span class="sxs-lookup"><span data-stu-id="43f5f-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43f5f-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43f5f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="43f5f-144"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f5f-144"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="43f5f-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43f5f-145">Library</span></span><br/> | <dl> <span data-ttu-id="43f5f-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43f5f-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43f5f-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="43f5f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f5f-148">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="43f5f-148">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="43f5f-149">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="43f5f-149">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="43f5f-150">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="43f5f-150">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
