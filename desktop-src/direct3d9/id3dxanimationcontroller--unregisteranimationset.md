---
description: Quita un conjunto de animaciones del controlador de animación.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'ID3DXAnimationController:: UnregisterAnimationSet (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698424"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a><span data-ttu-id="8cfba-103">ID3DXAnimationController:: UnregisterAnimationSet (método)</span><span class="sxs-lookup"><span data-stu-id="8cfba-103">ID3DXAnimationController::UnregisterAnimationSet method</span></span>

<span data-ttu-id="8cfba-104">Quita un conjunto de animaciones del controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="8cfba-104">Removes an animation set from the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cfba-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="8cfba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cfba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cfba-107">*pAnimSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cfba-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfba-108">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfba-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="8cfba-109">Puntero a la animación [**ID3DXAnimationSet**](id3dxanimationset.md) establecida en Remove.</span><span class="sxs-lookup"><span data-stu-id="8cfba-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cfba-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cfba-110">Return value</span></span>

<span data-ttu-id="8cfba-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cfba-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cfba-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8cfba-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8cfba-113">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="8cfba-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfba-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cfba-114">Requirements</span></span>



| <span data-ttu-id="8cfba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cfba-115">Requirement</span></span> | <span data-ttu-id="8cfba-116">Value</span><span class="sxs-lookup"><span data-stu-id="8cfba-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfba-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cfba-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8cfba-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cfba-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8cfba-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cfba-119">Library</span></span><br/> | <dl> <span data-ttu-id="8cfba-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cfba-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cfba-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cfba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfba-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="8cfba-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




