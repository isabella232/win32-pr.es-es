---
description: Restablece el tiempo de la animación global en cero. Los eventos pendientes conservarán las programaciones originales, pero en el nuevo período de tiempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'ID3DXAnimationController:: ResetTime (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821303"
---
# <a name="id3dxanimationcontrollerresettime-method"></a><span data-ttu-id="fb367-104">ID3DXAnimationController:: ResetTime (método)</span><span class="sxs-lookup"><span data-stu-id="fb367-104">ID3DXAnimationController::ResetTime method</span></span>

<span data-ttu-id="fb367-105">Restablece el tiempo de la animación global en cero.</span><span class="sxs-lookup"><span data-stu-id="fb367-105">Resets the global animation time to zero.</span></span> <span data-ttu-id="fb367-106">Los eventos pendientes conservarán las programaciones originales, pero en el nuevo período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb367-106">Any pending events will retain their original schedules, but in the new timeframe.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb367-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb367-107">Syntax</span></span>


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a><span data-ttu-id="fb367-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb367-108">Parameters</span></span>

<span data-ttu-id="fb367-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb367-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb367-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb367-110">Return value</span></span>

<span data-ttu-id="fb367-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb367-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb367-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb367-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fb367-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fb367-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb367-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb367-114">Remarks</span></span>

<span data-ttu-id="fb367-115">Este método se utiliza normalmente cuando el valor de tiempo de animación global está cerca de la precisión máxima del almacenamiento doble o 2 ⁶ ⁴-1.</span><span class="sxs-lookup"><span data-stu-id="fb367-115">This method is typically used when the global animation time value is nearing the maximum precision of DOUBLE storage, or 2⁶⁴ - 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb367-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb367-116">Requirements</span></span>



| <span data-ttu-id="fb367-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb367-117">Requirement</span></span> | <span data-ttu-id="fb367-118">Value</span><span class="sxs-lookup"><span data-stu-id="fb367-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb367-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb367-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fb367-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb367-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fb367-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb367-121">Library</span></span><br/> | <dl> <span data-ttu-id="fb367-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb367-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb367-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb367-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb367-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="fb367-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




