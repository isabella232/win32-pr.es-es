---
description: Obtiene el número máximo de influencias para cualquier vértice de la malla.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'ID3DXSkinInfo:: GetMaxVertexInfluences (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acae5cc119df25989e6bf22692ec1609ffa9408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003758"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a><span data-ttu-id="82441-103">ID3DXSkinInfo:: GetMaxVertexInfluences (método)</span><span class="sxs-lookup"><span data-stu-id="82441-103">ID3DXSkinInfo::GetMaxVertexInfluences method</span></span>

<span data-ttu-id="82441-104">Obtiene el número máximo de influencias para cualquier vértice de la malla.</span><span class="sxs-lookup"><span data-stu-id="82441-104">Gets the maximum number of influences for any vertex in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="82441-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82441-105">Syntax</span></span>


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="82441-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82441-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82441-107">*maxVertexInfluences* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82441-107">*maxVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82441-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="82441-108">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="82441-109">Puntero a la influencia máxima del vértice.</span><span class="sxs-lookup"><span data-stu-id="82441-109">Pointer to the maximum vertex influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82441-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82441-110">Return value</span></span>

<span data-ttu-id="82441-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82441-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82441-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82441-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82441-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="82441-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="82441-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82441-114">Requirements</span></span>



| <span data-ttu-id="82441-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="82441-115">Requirement</span></span> | <span data-ttu-id="82441-116">Value</span><span class="sxs-lookup"><span data-stu-id="82441-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82441-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82441-117">Header</span></span><br/>  | <dl> <span data-ttu-id="82441-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="82441-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="82441-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82441-119">Library</span></span><br/> | <dl> <span data-ttu-id="82441-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82441-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82441-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="82441-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82441-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="82441-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
