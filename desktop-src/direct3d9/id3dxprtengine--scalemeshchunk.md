---
description: Escala todos los ejemplos asociados a una submalla determinada. El método es útil para calcular la dispersión de subsuperficies.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'ID3DXPRTEngine:: ScaleMeshChunk (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708047"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a><span data-ttu-id="c43ad-104">ID3DXPRTEngine:: ScaleMeshChunk (método)</span><span class="sxs-lookup"><span data-stu-id="c43ad-104">ID3DXPRTEngine::ScaleMeshChunk method</span></span>

<span data-ttu-id="c43ad-105">Escala todos los ejemplos asociados a una submalla determinada.</span><span class="sxs-lookup"><span data-stu-id="c43ad-105">Scales all the samples associated with a given submesh.</span></span> <span data-ttu-id="c43ad-106">El método es útil para calcular la dispersión de subsuperficies.</span><span class="sxs-lookup"><span data-stu-id="c43ad-106">The method is useful for computing subsurface scattering.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43ad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c43ad-107">Syntax</span></span>


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="c43ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c43ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c43ad-109">*uMeshChunk* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c43ad-109">*uMeshChunk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43ad-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c43ad-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c43ad-111">Ubicación de la malla en la que se inician los ejemplos de escalado.</span><span class="sxs-lookup"><span data-stu-id="c43ad-111">Location in the mesh at which to start scaling samples.</span></span>

</dd> <dt>

<span data-ttu-id="c43ad-112">*fScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c43ad-112">*fScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43ad-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c43ad-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c43ad-114">Valor por el que se multiplica cada vector de la submalla.</span><span class="sxs-lookup"><span data-stu-id="c43ad-114">Value by which to multiply each vector in the submesh.</span></span>

</dd> <dt>

<span data-ttu-id="c43ad-115">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c43ad-115">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c43ad-116">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c43ad-116">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c43ad-117">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) para recibir ejemplos de escalado en la submalla.</span><span class="sxs-lookup"><span data-stu-id="c43ad-117">Pointer to a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object to receive rescaled samples in the submesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c43ad-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c43ad-118">Return value</span></span>

<span data-ttu-id="c43ad-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c43ad-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c43ad-120">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c43ad-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c43ad-121">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c43ad-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c43ad-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c43ad-122">Requirements</span></span>



| <span data-ttu-id="c43ad-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c43ad-123">Requirement</span></span> | <span data-ttu-id="c43ad-124">Value</span><span class="sxs-lookup"><span data-stu-id="c43ad-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c43ad-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c43ad-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c43ad-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c43ad-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c43ad-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c43ad-127">Library</span></span><br/> | <dl> <span data-ttu-id="c43ad-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c43ad-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c43ad-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c43ad-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43ad-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c43ad-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
