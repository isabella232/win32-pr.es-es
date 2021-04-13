---
description: Finaliza un paso activo.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect:: EndPass (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362601"
---
# <a name="id3dxeffectendpass-method"></a><span data-ttu-id="96537-103">ID3DXEffect:: EndPass (método)</span><span class="sxs-lookup"><span data-stu-id="96537-103">ID3DXEffect::EndPass method</span></span>

<span data-ttu-id="96537-104">Finaliza un paso activo.</span><span class="sxs-lookup"><span data-stu-id="96537-104">End an active pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="96537-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96537-105">Syntax</span></span>


```C++
HRESULT EndPass();
```



## <a name="parameters"></a><span data-ttu-id="96537-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96537-106">Parameters</span></span>

<span data-ttu-id="96537-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="96537-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96537-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96537-108">Return value</span></span>

<span data-ttu-id="96537-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96537-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96537-110">Este método siempre devuelve el valor S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="96537-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="96537-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96537-111">Remarks</span></span>

<span data-ttu-id="96537-112">Una aplicación señala el final de la representación de un paso activo mediante una llamada a **ID3DXEffect:: EndPass**.</span><span class="sxs-lookup"><span data-stu-id="96537-112">An application signals the end of rendering an active pass by calling **ID3DXEffect::EndPass**.</span></span> <span data-ttu-id="96537-113">Cada **ID3DXEffect:: EndPass** debe formar parte de un par coincidente de las llamadas a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) y **ID3DXEffect:: EndPass** .</span><span class="sxs-lookup"><span data-stu-id="96537-113">Each **ID3DXEffect::EndPass** must be part of a matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls.</span></span>

<span data-ttu-id="96537-114">Cada par coincidente de las llamadas a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) y **ID3DXEffect:: EndPass** debe encontrarse dentro de un par coincidente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) y [**ID3DXEffect:: end**](id3dxeffect--end.md) calls.</span><span class="sxs-lookup"><span data-stu-id="96537-114">Each matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls must be located within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="96537-115">Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**Effect:: setx**](id3dxeffect.md) dentro de un par de coincidencia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: EndPass** , la aplicación debe llamar a [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) antes de cualquier llamada a DrawxPrimitive para propagar los cambios de estado en el dispositivo antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="96537-115">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/**ID3DXEffect::EndPass** matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="96537-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96537-116">Requirements</span></span>



| <span data-ttu-id="96537-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="96537-117">Requirement</span></span> | <span data-ttu-id="96537-118">Value</span><span class="sxs-lookup"><span data-stu-id="96537-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96537-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96537-119">Header</span></span><br/>  | <dl> <span data-ttu-id="96537-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="96537-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="96537-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96537-121">Library</span></span><br/> | <dl> <span data-ttu-id="96537-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96537-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="96537-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="96537-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96537-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="96537-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




