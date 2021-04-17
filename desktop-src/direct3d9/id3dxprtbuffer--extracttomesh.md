---
description: Extrae los datos coeficientes de un búfer de un solo canal y agrega los datos a un objeto ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer:: ExtractToMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708117"
---
# <a name="id3dxprtbufferextracttomesh-method"></a><span data-ttu-id="be951-103">ID3DXPRTBuffer:: ExtractToMesh (método)</span><span class="sxs-lookup"><span data-stu-id="be951-103">ID3DXPRTBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="be951-104">Extrae los datos coeficientes de un búfer de un solo canal y agrega los datos a un objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="be951-104">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="be951-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be951-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="be951-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be951-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be951-107">*NumCoefficients* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be951-107">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be951-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be951-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be951-109">Número de coeficientes que se van a extraer del búfer.</span><span class="sxs-lookup"><span data-stu-id="be951-109">Number of coefficients to extract from the buffer.</span></span> <span data-ttu-id="be951-110">Cuando se usa la transferencia Radiance (PRT) precalculada de armónico (SH), el número de coeficientes debe ser Order ².</span><span class="sxs-lookup"><span data-stu-id="be951-110">When using spherical harmonic (SH) precomputed radiance transfer (PRT), the number of coefficients should be Order ².</span></span> <span data-ttu-id="be951-111">El orden debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="be951-111">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="be951-112">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="be951-112">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be951-113">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="be951-113">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="be951-114">Descripciones del uso de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="be951-114">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="be951-115">Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="be951-115">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="be951-116">*UsageIndexStart* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be951-116">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be951-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be951-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be951-118">Índice inicial de los coeficientes que se van a almacenar en la malla.</span><span class="sxs-lookup"><span data-stu-id="be951-118">Starting index for coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="be951-119">*pScene* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be951-119">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be951-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="be951-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="be951-121">Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) que almacenará los coeficientes.</span><span class="sxs-lookup"><span data-stu-id="be951-121">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be951-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be951-122">Return value</span></span>

<span data-ttu-id="be951-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be951-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be951-124">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be951-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="be951-125">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="be951-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="be951-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be951-126">Requirements</span></span>



| <span data-ttu-id="be951-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="be951-127">Requirement</span></span> | <span data-ttu-id="be951-128">Value</span><span class="sxs-lookup"><span data-stu-id="be951-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be951-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be951-129">Header</span></span><br/>  | <dl> <span data-ttu-id="be951-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="be951-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="be951-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be951-131">Library</span></span><br/> | <dl> <span data-ttu-id="be951-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be951-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be951-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="be951-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be951-134">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="be951-134">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
