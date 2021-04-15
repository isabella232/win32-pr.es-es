---
description: Divide caras en una malla, lo que permite un muestreo adaptativo conservador que no eliminará características en la malla.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'ID3DXPRTEngine:: RobustMeshRefine (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708048"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a><span data-ttu-id="ec766-103">ID3DXPRTEngine:: RobustMeshRefine (método)</span><span class="sxs-lookup"><span data-stu-id="ec766-103">ID3DXPRTEngine::RobustMeshRefine method</span></span>

<span data-ttu-id="ec766-104">Divide caras en una malla, lo que permite un muestreo adaptativo conservador que no eliminará características en la malla.</span><span class="sxs-lookup"><span data-stu-id="ec766-104">Subdivides faces on a mesh, allowing for conservative adaptive sampling that will not eliminate features on the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec766-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec766-105">Syntax</span></span>


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a><span data-ttu-id="ec766-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec766-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec766-107">*MinEdgeLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ec766-107">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec766-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec766-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec766-109">Longitud mínima del borde de la superficie que se generará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="ec766-109">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="ec766-110">Si es cero, se sustituirá un valor predeterminado razonable.</span><span class="sxs-lookup"><span data-stu-id="ec766-110">If zero, a reasonable default value will be substituted.</span></span>

</dd> <dt>

<span data-ttu-id="ec766-111">*MaxSubdiv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ec766-111">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec766-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec766-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec766-113">Nivel máximo de subdivisión de una esfera que se usará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="ec766-113">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="ec766-114">Si es cero, se sustituirá un valor predeterminado de 5.</span><span class="sxs-lookup"><span data-stu-id="ec766-114">If zero, a default value of 5 will be substituted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec766-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec766-115">Return value</span></span>

<span data-ttu-id="ec766-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec766-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec766-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ec766-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ec766-118">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ec766-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec766-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec766-119">Requirements</span></span>



| <span data-ttu-id="ec766-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec766-120">Requirement</span></span> | <span data-ttu-id="ec766-121">Value</span><span class="sxs-lookup"><span data-stu-id="ec766-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec766-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec766-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ec766-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec766-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ec766-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec766-124">Library</span></span><br/> | <dl> <span data-ttu-id="ec766-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec766-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ec766-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec766-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec766-127">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="ec766-127">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="ec766-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span><span class="sxs-lookup"><span data-stu-id="ec766-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span></span>](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[<span data-ttu-id="ec766-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span><span class="sxs-lookup"><span data-stu-id="ec766-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span></span>](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
