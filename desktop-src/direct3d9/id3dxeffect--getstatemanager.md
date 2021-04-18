---
description: Obtiene el efecto administrador de estado.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect:: GetStateManager (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707798"
---
# <a name="id3dxeffectgetstatemanager-method"></a><span data-ttu-id="2083b-103">ID3DXEffect:: GetStateManager (método)</span><span class="sxs-lookup"><span data-stu-id="2083b-103">ID3DXEffect::GetStateManager method</span></span>

<span data-ttu-id="2083b-104">Obtiene el efecto administrador de estado.</span><span class="sxs-lookup"><span data-stu-id="2083b-104">Get the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="2083b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2083b-105">Syntax</span></span>


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="2083b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2083b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2083b-107">*ppManager* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2083b-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2083b-108">Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span><span class="sxs-lookup"><span data-stu-id="2083b-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span></span>

<span data-ttu-id="2083b-109">Devuelve un puntero al administrador de Estados.</span><span class="sxs-lookup"><span data-stu-id="2083b-109">Returns a pointer to the state manager.</span></span> <span data-ttu-id="2083b-110">Vea [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="2083b-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2083b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2083b-111">Return value</span></span>

<span data-ttu-id="2083b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2083b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2083b-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2083b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2083b-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2083b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2083b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2083b-115">Remarks</span></span>

<span data-ttu-id="2083b-116">[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) es una interfaz implementada por el usuario que facilita las devoluciones de llamada en una aplicación para establecer el estado del dispositivo de un efecto.</span><span class="sxs-lookup"><span data-stu-id="2083b-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="2083b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2083b-117">Requirements</span></span>



| <span data-ttu-id="2083b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2083b-118">Requirement</span></span> | <span data-ttu-id="2083b-119">Value</span><span class="sxs-lookup"><span data-stu-id="2083b-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2083b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2083b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2083b-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2083b-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2083b-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2083b-122">Library</span></span><br/> | <dl> <span data-ttu-id="2083b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2083b-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2083b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2083b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2083b-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2083b-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="2083b-126">**ID3DXEffect::SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="2083b-126">**ID3DXEffect::SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




