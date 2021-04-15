---
description: Recupera los valores de albedo de los vértices de malla.
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: 'ID3DXPRTEngine:: GetVertexAlbedo (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7926f6393221552107667c9209ef2b4c51945ab8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708050"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a><span data-ttu-id="ee88b-103">ID3DXPRTEngine:: GetVertexAlbedo (método)</span><span class="sxs-lookup"><span data-stu-id="ee88b-103">ID3DXPRTEngine::GetVertexAlbedo method</span></span>

<span data-ttu-id="ee88b-104">Recupera los valores de albedo de los vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="ee88b-104">Retrieves albedo values of the mesh vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee88b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee88b-105">Syntax</span></span>


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a><span data-ttu-id="ee88b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee88b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee88b-107">*pVertColors* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ee88b-107">*pVertColors* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee88b-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee88b-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ee88b-109">Puntero a una matriz de destino de valores albedo de los vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="ee88b-109">Pointer to a destination array of albedo values of the mesh vertices.</span></span> <span data-ttu-id="ee88b-110">Vea [**D3DXCOLOR**](d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="ee88b-110">See [**D3DXCOLOR**](d3dxcolor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee88b-111">*NumVerts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee88b-111">*NumVerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee88b-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee88b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee88b-113">Número de vértices en la malla.</span><span class="sxs-lookup"><span data-stu-id="ee88b-113">Number of vertices in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee88b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee88b-114">Return value</span></span>

<span data-ttu-id="ee88b-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee88b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee88b-116">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee88b-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ee88b-117">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ee88b-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee88b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee88b-118">Requirements</span></span>



| <span data-ttu-id="ee88b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee88b-119">Requirement</span></span> | <span data-ttu-id="ee88b-120">Value</span><span class="sxs-lookup"><span data-stu-id="ee88b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee88b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee88b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ee88b-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee88b-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ee88b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee88b-123">Library</span></span><br/> | <dl> <span data-ttu-id="ee88b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee88b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee88b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee88b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee88b-126">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="ee88b-126">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
