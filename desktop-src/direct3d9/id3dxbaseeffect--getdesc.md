---
description: Obtiene la descripción del efecto.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'ID3DXBaseEffect:: GetDesc (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698415"
---
# <a name="id3dxbaseeffectgetdesc-method"></a><span data-ttu-id="af686-103">ID3DXBaseEffect:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="af686-103">ID3DXBaseEffect::GetDesc method</span></span>

<span data-ttu-id="af686-104">Obtiene la descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="af686-104">Gets the effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="af686-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af686-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="af686-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af686-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af686-107">*pDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="af686-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af686-108">Tipo: **[ **D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="af686-108">Type: **[**D3DXEFFECT\_DESC**](d3dxeffect-desc.md)\***</span></span>

<span data-ttu-id="af686-109">Devuelve una descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="af686-109">Returns a description of the effect.</span></span> <span data-ttu-id="af686-110">Vea [**D3DXEFFECT \_ DESC**](d3dxeffect-desc.md).</span><span class="sxs-lookup"><span data-stu-id="af686-110">See [**D3DXEFFECT\_DESC**](d3dxeffect-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af686-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af686-111">Return value</span></span>

<span data-ttu-id="af686-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af686-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af686-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af686-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="af686-114">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="af686-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="af686-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af686-115">Requirements</span></span>



| <span data-ttu-id="af686-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af686-116">Requirement</span></span> | <span data-ttu-id="af686-117">Value</span><span class="sxs-lookup"><span data-stu-id="af686-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af686-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af686-118">Header</span></span><br/>  | <dl> <span data-ttu-id="af686-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="af686-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="af686-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af686-120">Library</span></span><br/> | <dl> <span data-ttu-id="af686-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af686-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="af686-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="af686-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af686-123">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="af686-123">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




