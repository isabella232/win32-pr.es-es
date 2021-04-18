---
description: Obtiene una descripción de un evento de animación especificado.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'ID3DXAnimationController:: GetEventDesc (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718475"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a><span data-ttu-id="f7ee3-103">ID3DXAnimationController:: GetEventDesc (método)</span><span class="sxs-lookup"><span data-stu-id="f7ee3-103">ID3DXAnimationController::GetEventDesc method</span></span>

<span data-ttu-id="f7ee3-104">Obtiene una descripción de un evento de animación especificado.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-104">Gets a description of a specified animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ee3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7ee3-105">Syntax</span></span>


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="f7ee3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7ee3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7ee3-107">*hEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7ee3-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7ee3-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="f7ee3-109">Identificador de evento de un evento de animación que se va a describir.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-109">Event handle to an animation event to describe.</span></span>

</dd> <dt>

<span data-ttu-id="f7ee3-110">*pDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f7ee3-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7ee3-111">Tipo: **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-111">Type: **[**LPD3DXEVENT\_DESC**](d3dxevent-desc.md)**</span></span>

<span data-ttu-id="f7ee3-112">Puntero a una [**estructura \_ DESC de D3DXEVENT**](d3dxevent-desc.md) que contiene una descripción del evento de animación.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-112">Pointer to a [**D3DXEVENT\_DESC**](d3dxevent-desc.md) structure that contains a description of the animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7ee3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7ee3-113">Return value</span></span>

<span data-ttu-id="f7ee3-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7ee3-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f7ee3-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ee3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7ee3-117">Requirements</span></span>



| <span data-ttu-id="f7ee3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7ee3-118">Requirement</span></span> | <span data-ttu-id="f7ee3-119">Value</span><span class="sxs-lookup"><span data-stu-id="f7ee3-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ee3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7ee3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f7ee3-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7ee3-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f7ee3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7ee3-122">Library</span></span><br/> | <dl> <span data-ttu-id="f7ee3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7ee3-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7ee3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7ee3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ee3-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f7ee3-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




