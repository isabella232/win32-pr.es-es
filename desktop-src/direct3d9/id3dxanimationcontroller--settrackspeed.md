---
description: Establece la velocidad de la pista. La velocidad de la pista es similar a un multiplicador que se usa para acelerar o ralentizar la reproducción de la pista.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'ID3DXAnimationController:: SetTrackSpeed (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362790"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a><span data-ttu-id="2395e-104">ID3DXAnimationController:: SetTrackSpeed (método)</span><span class="sxs-lookup"><span data-stu-id="2395e-104">ID3DXAnimationController::SetTrackSpeed method</span></span>

<span data-ttu-id="2395e-105">Establece la velocidad de la pista.</span><span class="sxs-lookup"><span data-stu-id="2395e-105">Sets the track speed.</span></span> <span data-ttu-id="2395e-106">La velocidad de la pista es similar a un multiplicador que se usa para acelerar o ralentizar la reproducción de la pista.</span><span class="sxs-lookup"><span data-stu-id="2395e-106">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="2395e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2395e-107">Syntax</span></span>


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a><span data-ttu-id="2395e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2395e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2395e-109">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2395e-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2395e-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2395e-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2395e-111">Identificador de la pista en la que se va a establecer la velocidad.</span><span class="sxs-lookup"><span data-stu-id="2395e-111">Identifier of the track to set the speed on.</span></span>

</dd> <dt>

<span data-ttu-id="2395e-112">*Velocidad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2395e-112">*Speed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2395e-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2395e-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2395e-114">Nueva velocidad.</span><span class="sxs-lookup"><span data-stu-id="2395e-114">New speed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2395e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2395e-115">Return value</span></span>

<span data-ttu-id="2395e-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2395e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2395e-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2395e-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2395e-118">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2395e-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2395e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2395e-119">Requirements</span></span>



| <span data-ttu-id="2395e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2395e-120">Requirement</span></span> | <span data-ttu-id="2395e-121">Value</span><span class="sxs-lookup"><span data-stu-id="2395e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2395e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2395e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2395e-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2395e-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2395e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2395e-124">Library</span></span><br/> | <dl> <span data-ttu-id="2395e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2395e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2395e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2395e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2395e-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2395e-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
