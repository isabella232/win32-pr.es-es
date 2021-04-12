---
description: Quita un evento especificado de una pista de animación, lo que impide la ejecución del evento.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'ID3DXAnimationController:: UnkeyEvent (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362788"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a><span data-ttu-id="950e2-103">ID3DXAnimationController:: UnkeyEvent (método)</span><span class="sxs-lookup"><span data-stu-id="950e2-103">ID3DXAnimationController::UnkeyEvent method</span></span>

<span data-ttu-id="950e2-104">Quita un evento especificado de una pista de animación, lo que impide la ejecución del evento.</span><span class="sxs-lookup"><span data-stu-id="950e2-104">Removes a specified event from an animation track, preventing the execution of the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="950e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="950e2-105">Syntax</span></span>


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="950e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="950e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950e2-107">*hEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="950e2-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950e2-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="950e2-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="950e2-109">Identificador del evento que se va a quitar de la pista de animación.</span><span class="sxs-lookup"><span data-stu-id="950e2-109">Event handle to the event to be removed from the animation track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="950e2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="950e2-110">Return value</span></span>

<span data-ttu-id="950e2-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="950e2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="950e2-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="950e2-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="950e2-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="950e2-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="950e2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="950e2-114">Requirements</span></span>



| <span data-ttu-id="950e2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="950e2-115">Requirement</span></span> | <span data-ttu-id="950e2-116">Value</span><span class="sxs-lookup"><span data-stu-id="950e2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="950e2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="950e2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="950e2-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="950e2-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="950e2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="950e2-119">Library</span></span><br/> | <dl> <span data-ttu-id="950e2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="950e2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="950e2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="950e2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950e2-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="950e2-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




