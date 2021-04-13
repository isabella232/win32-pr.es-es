---
description: Finaliza una técnica activa.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect:: end (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362602"
---
# <a name="id3dxeffectend-method"></a><span data-ttu-id="a2256-103">ID3DXEffect:: end (método)</span><span class="sxs-lookup"><span data-stu-id="a2256-103">ID3DXEffect::End method</span></span>

<span data-ttu-id="a2256-104">Finaliza una técnica activa.</span><span class="sxs-lookup"><span data-stu-id="a2256-104">Ends an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2256-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2256-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="a2256-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2256-106">Parameters</span></span>

<span data-ttu-id="a2256-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2256-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2256-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2256-108">Return value</span></span>

<span data-ttu-id="a2256-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2256-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2256-110">Este método siempre devuelve el valor S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a2256-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2256-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2256-111">Remarks</span></span>

<span data-ttu-id="a2256-112">Toda la representación en un efecto se realiza dentro de un par coincidente de llamadas a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) y **ID3DXEffect:: end** .</span><span class="sxs-lookup"><span data-stu-id="a2256-112">All rendering in an effect is done within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and **ID3DXEffect::End** calls.</span></span> <span data-ttu-id="a2256-113">Una vez que se representan todas las pasadas, se debe llamar a **ID3DXEffect:: end** para finalizar la técnica activa.</span><span class="sxs-lookup"><span data-stu-id="a2256-113">After all passes are rendered, **ID3DXEffect::End** must be called to end the active technique.</span></span> <span data-ttu-id="a2256-114">El sistema de efecto responde mediante el uso del bloque de estado creado cuando se llamó a **ID3DXEffect:: Begin** para restaurar automáticamente el estado de la canalización antes de **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="a2256-114">The effect system responds by using the state block created when **ID3DXEffect::Begin** was called, to automatically restore the pipeline state before **ID3DXEffect::Begin**.</span></span>

<span data-ttu-id="a2256-115">De forma predeterminada, el sistema de efectos se encarga de guardar el estado antes de una técnica y restaurar el estado después de una técnica.</span><span class="sxs-lookup"><span data-stu-id="a2256-115">By default, the effect system takes care of saving state prior to a technique, and restoring state after a technique.</span></span> <span data-ttu-id="a2256-116">Si decide deshabilitar esta funcionalidad de guardar y restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a2256-116">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2256-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2256-117">Requirements</span></span>



| <span data-ttu-id="a2256-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2256-118">Requirement</span></span> | <span data-ttu-id="a2256-119">Value</span><span class="sxs-lookup"><span data-stu-id="a2256-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2256-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2256-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a2256-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2256-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a2256-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2256-122">Library</span></span><br/> | <dl> <span data-ttu-id="a2256-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2256-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a2256-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2256-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2256-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="a2256-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




