---
description: Obtiene un puntero al grupo de parámetros compartidos.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'ID3DXEffect:: GetPool (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003778"
---
# <a name="id3dxeffectgetpool-method"></a><span data-ttu-id="01b7a-103">ID3DXEffect:: GetPool (método)</span><span class="sxs-lookup"><span data-stu-id="01b7a-103">ID3DXEffect::GetPool method</span></span>

<span data-ttu-id="01b7a-104">Obtiene un puntero al grupo de parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="01b7a-104">Gets a pointer to the pool of shared parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01b7a-105">Syntax</span></span>


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="01b7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01b7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b7a-107">*ppPool* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="01b7a-107">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01b7a-108">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="01b7a-108">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="01b7a-109">Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="01b7a-109">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b7a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01b7a-110">Return value</span></span>

<span data-ttu-id="01b7a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01b7a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01b7a-112">Este método siempre devuelve el valor S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="01b7a-112">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b7a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01b7a-113">Remarks</span></span>

<span data-ttu-id="01b7a-114">Los grupos contienen parámetros compartidos entre efectos.</span><span class="sxs-lookup"><span data-stu-id="01b7a-114">Pools contain shared parameters between effects.</span></span> <span data-ttu-id="01b7a-115">Vea [clonación y uso compartido (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="01b7a-115">See [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01b7a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01b7a-116">Requirements</span></span>



| <span data-ttu-id="01b7a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b7a-117">Requirement</span></span> | <span data-ttu-id="01b7a-118">Value</span><span class="sxs-lookup"><span data-stu-id="01b7a-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b7a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01b7a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="01b7a-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b7a-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="01b7a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01b7a-121">Library</span></span><br/> | <dl> <span data-ttu-id="01b7a-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01b7a-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="01b7a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="01b7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b7a-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="01b7a-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




