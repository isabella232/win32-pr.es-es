---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer el número de segmentos de subdivisión para N-patches.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'ID3DXEffectStateManager:: SetNPatchMode (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003966"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a><span data-ttu-id="2c795-103">ID3DXEffectStateManager:: SetNPatchMode (método)</span><span class="sxs-lookup"><span data-stu-id="2c795-103">ID3DXEffectStateManager::SetNPatchMode method</span></span>

<span data-ttu-id="2c795-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer el número de segmentos de subdivisión para N-patches.</span><span class="sxs-lookup"><span data-stu-id="2c795-104">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c795-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c795-105">Syntax</span></span>


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a><span data-ttu-id="2c795-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c795-107">*nSegments* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c795-107">*nSegments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c795-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c795-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c795-109">Divida la superficie en este número de subdivisiones.</span><span class="sxs-lookup"><span data-stu-id="2c795-109">Break the surface into this number of subdivisions.</span></span> <span data-ttu-id="2c795-110">Es lo mismo que el número usado por [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="2c795-110">This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c795-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c795-111">Return value</span></span>

<span data-ttu-id="2c795-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c795-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c795-113">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="2c795-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="2c795-114">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="2c795-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="2c795-115">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="2c795-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="2c795-116">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)).</span><span class="sxs-lookup"><span data-stu-id="2c795-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c795-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c795-117">Requirements</span></span>



| <span data-ttu-id="2c795-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c795-118">Requirement</span></span> | <span data-ttu-id="2c795-119">Value</span><span class="sxs-lookup"><span data-stu-id="2c795-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c795-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c795-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2c795-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c795-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2c795-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c795-122">Library</span></span><br/> | <dl> <span data-ttu-id="2c795-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c795-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2c795-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c795-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c795-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="2c795-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
