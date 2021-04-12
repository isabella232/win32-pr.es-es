---
description: Recupera los parámetros de la superficie de representación.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'ID3DXRenderToSurface:: GetDesc (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280494"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a><span data-ttu-id="7e50d-103">ID3DXRenderToSurface:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="7e50d-103">ID3DXRenderToSurface::GetDesc method</span></span>

<span data-ttu-id="7e50d-104">Recupera los parámetros de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="7e50d-104">Retrieves the parameters of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e50d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e50d-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="7e50d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e50d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e50d-107">*pParameters* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7e50d-107">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e50d-108">Tipo: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e50d-108">Type: **[**D3DXRTS\_DESC**](d3dxrts-desc.md)\***</span></span>

<span data-ttu-id="7e50d-109">Puntero a una [**estructura \_ DESC de D3DXRTS**](d3dxrts-desc.md) , que describe los parámetros de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="7e50d-109">Pointer to a [**D3DXRTS\_DESC**](d3dxrts-desc.md) structure, describing the parameters of the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e50d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e50d-110">Return value</span></span>

<span data-ttu-id="7e50d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e50d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e50d-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e50d-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e50d-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7e50d-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e50d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e50d-114">Requirements</span></span>



| <span data-ttu-id="7e50d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e50d-115">Requirement</span></span> | <span data-ttu-id="7e50d-116">Value</span><span class="sxs-lookup"><span data-stu-id="7e50d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e50d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e50d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7e50d-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e50d-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7e50d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e50d-119">Library</span></span><br/> | <dl> <span data-ttu-id="7e50d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e50d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e50d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e50d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e50d-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="7e50d-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 




