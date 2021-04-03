---
description: Habilita o deshabilita una pista en el controlador de animación.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'ID3DXAnimationController:: SetTrackEnable (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083778"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a><span data-ttu-id="58c03-103">ID3DXAnimationController:: SetTrackEnable (método)</span><span class="sxs-lookup"><span data-stu-id="58c03-103">ID3DXAnimationController::SetTrackEnable method</span></span>

<span data-ttu-id="58c03-104">Habilita o deshabilita una pista en el controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="58c03-104">Enables or disables a track in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58c03-105">Syntax</span></span>


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="58c03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c03-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="58c03-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c03-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58c03-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58c03-109">Identificador de la pista que se va a mezclar.</span><span class="sxs-lookup"><span data-stu-id="58c03-109">Identifier of the track to be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="58c03-110">*Habilitar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58c03-110">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c03-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58c03-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58c03-112">Habilitar valor.</span><span class="sxs-lookup"><span data-stu-id="58c03-112">Enable value.</span></span> <span data-ttu-id="58c03-113">Establézcalo en **true** para habilitar esta pista en el controlador o en **false** para evitar que se mezcle.</span><span class="sxs-lookup"><span data-stu-id="58c03-113">Set to **TRUE** to enable this track in the controller, or to **FALSE** to prevent it from being mixed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c03-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58c03-114">Return value</span></span>

<span data-ttu-id="58c03-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58c03-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58c03-116">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58c03-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="58c03-117">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="58c03-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="58c03-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58c03-118">Remarks</span></span>

<span data-ttu-id="58c03-119">Para mezclar una pista con otras pistas, la marca enable debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="58c03-119">To mix a track with other tracks, the Enable flag must be set to **TRUE**.</span></span> <span data-ttu-id="58c03-120">Por el contrario, si se establece la marca en **false** , impedirá que la pista se mezcle con otras pistas.</span><span class="sxs-lookup"><span data-stu-id="58c03-120">Conversely, setting the flag to **FALSE** will prevent the track from being mixed with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="58c03-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58c03-121">Requirements</span></span>



| <span data-ttu-id="58c03-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="58c03-122">Requirement</span></span> | <span data-ttu-id="58c03-123">Value</span><span class="sxs-lookup"><span data-stu-id="58c03-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58c03-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58c03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="58c03-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="58c03-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="58c03-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58c03-126">Library</span></span><br/> | <dl> <span data-ttu-id="58c03-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58c03-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58c03-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="58c03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c03-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="58c03-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
