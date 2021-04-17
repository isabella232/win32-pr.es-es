---
description: Anima la malla y avanza el tiempo de animación global en una cantidad especificada.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'ID3DXAnimationController:: AdvanceTime (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698388"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a><span data-ttu-id="6cfd5-103">ID3DXAnimationController:: AdvanceTime (método)</span><span class="sxs-lookup"><span data-stu-id="6cfd5-103">ID3DXAnimationController::AdvanceTime method</span></span>

<span data-ttu-id="6cfd5-104">Anima la malla y avanza el tiempo de animación global en una cantidad especificada.</span><span class="sxs-lookup"><span data-stu-id="6cfd5-104">Animates the mesh and advances the global animation time by a specified amount.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfd5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cfd5-105">Syntax</span></span>


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a><span data-ttu-id="6cfd5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cfd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cfd5-107">*TimeDelta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6cfd5-107">*TimeDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfd5-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cfd5-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6cfd5-109">Cantidad, en segundos, por la que se va a avanzar el tiempo de animación global.</span><span class="sxs-lookup"><span data-stu-id="6cfd5-109">Amount, in seconds, by which to advance the global animation time.</span></span> <span data-ttu-id="6cfd5-110">El valor de TimeDelta debe ser no negativo o cero.</span><span class="sxs-lookup"><span data-stu-id="6cfd5-110">TimeDelta value must be non-negative or zero.</span></span>

</dd> <dt>

<span data-ttu-id="6cfd5-111">*pCallbackHandler* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6cfd5-111">*pCallbackHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfd5-112">Tipo: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span><span class="sxs-lookup"><span data-stu-id="6cfd5-112">Type: **[**LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span></span>

<span data-ttu-id="6cfd5-113">Puntero a una interfaz de controlador de devolución de llamada de animación definida por el usuario, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span><span class="sxs-lookup"><span data-stu-id="6cfd5-113">Pointer to a user-defined animation callback handler interface, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cfd5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cfd5-114">Return value</span></span>

<span data-ttu-id="6cfd5-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6cfd5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6cfd5-116">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6cfd5-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6cfd5-117">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6cfd5-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cfd5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cfd5-118">Requirements</span></span>



| <span data-ttu-id="6cfd5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cfd5-119">Requirement</span></span> | <span data-ttu-id="6cfd5-120">Value</span><span class="sxs-lookup"><span data-stu-id="6cfd5-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfd5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cfd5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6cfd5-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd5-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6cfd5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cfd5-123">Library</span></span><br/> | <dl> <span data-ttu-id="6cfd5-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd5-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6cfd5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cfd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cfd5-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="6cfd5-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
