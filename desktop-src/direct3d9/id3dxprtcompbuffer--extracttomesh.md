---
description: Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos ID3DXPRTCompBuffer y agrega los datos a un objeto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer:: ExtractToMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707783"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a><span data-ttu-id="6c647-103">ID3DXPRTCompBuffer:: ExtractToMesh (método)</span><span class="sxs-lookup"><span data-stu-id="6c647-103">ID3DXPRTCompBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="6c647-104">Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) y agrega los datos a un objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="6c647-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c647-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c647-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="6c647-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c647-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c647-107">*NumPCA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c647-107">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c647-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c647-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c647-109">Número de coeficientes de PCA que se van a extraer del búfer.</span><span class="sxs-lookup"><span data-stu-id="6c647-109">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6c647-110">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6c647-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c647-111">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="6c647-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="6c647-112">Descripciones del uso de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="6c647-112">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="6c647-113">Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="6c647-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c647-114">*UsageIndexStart* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c647-114">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c647-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c647-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c647-116">Índice inicial de los coeficientes de PCA que se va a almacenar en la malla.</span><span class="sxs-lookup"><span data-stu-id="6c647-116">Starting index for PCA coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6c647-117">*pScene* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c647-117">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c647-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6c647-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="6c647-119">Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) que almacenará los coeficientes del PCA.</span><span class="sxs-lookup"><span data-stu-id="6c647-119">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c647-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c647-120">Return value</span></span>

<span data-ttu-id="6c647-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c647-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c647-122">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c647-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6c647-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6c647-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c647-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c647-124">Requirements</span></span>



| <span data-ttu-id="6c647-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c647-125">Requirement</span></span> | <span data-ttu-id="6c647-126">Value</span><span class="sxs-lookup"><span data-stu-id="6c647-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c647-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c647-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6c647-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c647-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6c647-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c647-129">Library</span></span><br/> | <dl> <span data-ttu-id="6c647-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c647-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c647-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c647-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c647-132">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="6c647-132">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
