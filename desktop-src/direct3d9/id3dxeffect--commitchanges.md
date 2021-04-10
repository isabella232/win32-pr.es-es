---
description: Propaga los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'ID3DXEffect:: CommitChanges (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280351"
---
# <a name="id3dxeffectcommitchanges-method"></a><span data-ttu-id="f566c-103">ID3DXEffect:: CommitChanges (método)</span><span class="sxs-lookup"><span data-stu-id="f566c-103">ID3DXEffect::CommitChanges method</span></span>

<span data-ttu-id="f566c-104">Propaga los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="f566c-104">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="f566c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f566c-105">Syntax</span></span>


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a><span data-ttu-id="f566c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f566c-106">Parameters</span></span>

<span data-ttu-id="f566c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f566c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f566c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f566c-108">Return value</span></span>

<span data-ttu-id="f566c-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f566c-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f566c-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f566c-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f566c-111">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f566c-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f566c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f566c-112">Remarks</span></span>

<span data-ttu-id="f566c-113">Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**ID3DXEffect:: setx**](id3dxeffect.md) dentro de un par de coincidencia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) , la aplicación debe llamar a **ID3DXEffect:: commitChanges** antes de cualquier llamada a DrawxPrimitive para propagar los cambios de estado en el dispositivo antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="f566c-113">If the application changes any effect state using any of the [**ID3DXEffect::Setx**](id3dxeffect.md) methods inside of an [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call **ID3DXEffect::CommitChanges** before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span> <span data-ttu-id="f566c-114">Si no se produce ningún cambio de estado dentro de un par de coincidencia **ID3DXEffect:: BeginPass** y **ID3DXEffect:: EndPass** , no es necesario llamar a **ID3DXEffect:: commitChanges**.</span><span class="sxs-lookup"><span data-stu-id="f566c-114">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

<span data-ttu-id="f566c-115">Esto es ligeramente diferente para los parámetros compartidos de un efecto clonado.</span><span class="sxs-lookup"><span data-stu-id="f566c-115">This is slightly different for any shared parameters in a cloned effect.</span></span> <span data-ttu-id="f566c-116">Cuando una técnica está activa en un efecto clonado (es decir, cuando se ha llamado a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) pero no se ha llamado a [**ID3DXEffect:: end**](id3dxeffect--end.md) ), **ID3DXEffect:: commitChanges** actualiza los parámetros que no se comparten según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="f566c-116">When a technique is active on a cloned effect (that is, when [**ID3DXEffect::Begin**](id3dxeffect--begin.md) has been called but and [**ID3DXEffect::End**](id3dxeffect--end.md) has not been called), **ID3DXEffect::CommitChanges** updates parameters that are not shared as expected.</span></span> <span data-ttu-id="f566c-117">Para actualizar un parámetro compartido (solo para un efecto clonado cuya técnica está activa), llame a **ID3DXEffect:: end** para desactivar la técnica y **ID3DXEffect:: Begin** para reactivar la técnica antes de llamar a **ID3DXEffect:: commitChanges**.</span><span class="sxs-lookup"><span data-stu-id="f566c-117">To update a shared parameter (only for a cloned effect whose technique is active), call **ID3DXEffect::End** to deactivate the technique and **ID3DXEffect::Begin** to reactivate the technique before calling **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f566c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f566c-118">Requirements</span></span>



| <span data-ttu-id="f566c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f566c-119">Requirement</span></span> | <span data-ttu-id="f566c-120">Value</span><span class="sxs-lookup"><span data-stu-id="f566c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f566c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f566c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f566c-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f566c-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f566c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f566c-123">Library</span></span><br/> | <dl> <span data-ttu-id="f566c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f566c-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f566c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f566c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f566c-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f566c-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




