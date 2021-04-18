---
description: Devuelve un identificador de evento al evento que se está ejecutando actualmente en la pista de animación especificada.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController:: GetCurrentTrackEvent (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718375"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a><span data-ttu-id="c91fb-103">ID3DXAnimationController:: GetCurrentTrackEvent (método)</span><span class="sxs-lookup"><span data-stu-id="c91fb-103">ID3DXAnimationController::GetCurrentTrackEvent method</span></span>

<span data-ttu-id="c91fb-104">Devuelve un identificador de evento al evento que se está ejecutando actualmente en la pista de animación especificada.</span><span class="sxs-lookup"><span data-stu-id="c91fb-104">Returns an event handle to the event currently running on the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="c91fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c91fb-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a><span data-ttu-id="c91fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c91fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c91fb-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c91fb-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c91fb-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c91fb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c91fb-109">Identificador de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="c91fb-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c91fb-110">*EventType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c91fb-110">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c91fb-111">Tipo: **[ **D3DXEVENT \_ Type**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="c91fb-111">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

<span data-ttu-id="c91fb-112">Tipo de evento que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="c91fb-112">Type of event to query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c91fb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c91fb-113">Return value</span></span>

<span data-ttu-id="c91fb-114">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="c91fb-114">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="c91fb-115">Identificador de evento para el evento que se ejecuta actualmente en la pista especificada. Se devuelve **null** si no se está ejecutando ningún evento en la pista especificada.</span><span class="sxs-lookup"><span data-stu-id="c91fb-115">Event handle to the event currently running on the specified track. **NULL** is returned if no event is running on the specified track.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91fb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c91fb-116">Requirements</span></span>



| <span data-ttu-id="c91fb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c91fb-117">Requirement</span></span> | <span data-ttu-id="c91fb-118">Value</span><span class="sxs-lookup"><span data-stu-id="c91fb-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c91fb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c91fb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c91fb-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c91fb-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c91fb-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c91fb-121">Library</span></span><br/> | <dl> <span data-ttu-id="c91fb-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c91fb-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c91fb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c91fb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c91fb-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c91fb-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
