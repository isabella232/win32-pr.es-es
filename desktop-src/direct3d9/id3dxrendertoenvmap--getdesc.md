---
description: Recupera la descripción de la superficie de representación.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'ID3DXRenderToEnvMap:: GetDesc (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821018"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a><span data-ttu-id="a437c-103">ID3DXRenderToEnvMap:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="a437c-103">ID3DXRenderToEnvMap::GetDesc method</span></span>

<span data-ttu-id="a437c-104">Recupera la descripción de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="a437c-104">Retrieves the description of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a437c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a437c-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a437c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a437c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a437c-107">*pDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a437c-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a437c-108">Tipo: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a437c-108">Type: **[**D3DXRTE\_DESC**](d3dxrte-desc.md)\***</span></span>

<span data-ttu-id="a437c-109">Puntero a una [**estructura \_ DESC de D3DXRTE**](d3dxrte-desc.md) que describe la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="a437c-109">Pointer to a [**D3DXRTE\_DESC**](d3dxrte-desc.md) structure that describes the rendering surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a437c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a437c-110">Return value</span></span>

<span data-ttu-id="a437c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a437c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a437c-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a437c-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a437c-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a437c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a437c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a437c-114">Requirements</span></span>



| <span data-ttu-id="a437c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a437c-115">Requirement</span></span> | <span data-ttu-id="a437c-116">Value</span><span class="sxs-lookup"><span data-stu-id="a437c-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a437c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a437c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a437c-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a437c-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a437c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a437c-119">Library</span></span><br/> | <dl> <span data-ttu-id="a437c-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a437c-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a437c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a437c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a437c-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a437c-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




