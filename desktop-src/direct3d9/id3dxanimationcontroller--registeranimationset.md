---
description: Agrega un conjunto de animaciones al controlador de animación.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'ID3DXAnimationController:: RegisterAnimationSet (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718412"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a><span data-ttu-id="0f00f-103">ID3DXAnimationController:: RegisterAnimationSet (método)</span><span class="sxs-lookup"><span data-stu-id="0f00f-103">ID3DXAnimationController::RegisterAnimationSet method</span></span>

<span data-ttu-id="0f00f-104">Agrega un conjunto de animaciones al controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="0f00f-104">Adds an animation set to the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f00f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f00f-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="0f00f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f00f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f00f-107">*pAnimSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f00f-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f00f-108">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="0f00f-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="0f00f-109">Puntero a la animación [**ID3DXAnimationSet**](id3dxanimationset.md) establecida en Add.</span><span class="sxs-lookup"><span data-stu-id="0f00f-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f00f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f00f-110">Return value</span></span>

<span data-ttu-id="0f00f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f00f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f00f-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f00f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0f00f-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0f00f-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f00f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f00f-114">Requirements</span></span>



| <span data-ttu-id="0f00f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f00f-115">Requirement</span></span> | <span data-ttu-id="0f00f-116">Value</span><span class="sxs-lookup"><span data-stu-id="0f00f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f00f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f00f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0f00f-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f00f-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0f00f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f00f-119">Library</span></span><br/> | <dl> <span data-ttu-id="0f00f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f00f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f00f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f00f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f00f-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0f00f-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




