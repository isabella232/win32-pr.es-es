---
description: Función de devolución de llamada que debe ser implementada por un usuario para establecer una luz.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'ID3DXEffectStateManager:: SetLight (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698303"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a><span data-ttu-id="2e049-103">ID3DXEffectStateManager:: SetLight (método)</span><span class="sxs-lookup"><span data-stu-id="2e049-103">ID3DXEffectStateManager::SetLight method</span></span>

<span data-ttu-id="2e049-104">Función de devolución de llamada que debe ser implementada por un usuario para establecer una luz.</span><span class="sxs-lookup"><span data-stu-id="2e049-104">A callback function that must be implemented by a user to set a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e049-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e049-105">Syntax</span></span>


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a><span data-ttu-id="2e049-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e049-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2e049-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e049-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e049-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e049-109">Índice de base cero de la luz.</span><span class="sxs-lookup"><span data-stu-id="2e049-109">The zero-based index of the light.</span></span> <span data-ttu-id="2e049-110">Este es el mismo índice en [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="2e049-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="2e049-111">*pLight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e049-111">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e049-112">Tipo: **const [**D3DLight9**](d3dlight9.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e049-112">Type: **const [**D3DLight9**](d3dlight9.md)\***</span></span>

<span data-ttu-id="2e049-113">Objeto Light.</span><span class="sxs-lookup"><span data-stu-id="2e049-113">The light object.</span></span> <span data-ttu-id="2e049-114">Vea [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="2e049-114">See [**D3DLIGHT9**](d3dlight9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e049-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e049-115">Return value</span></span>

<span data-ttu-id="2e049-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e049-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e049-117">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="2e049-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="2e049-118">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="2e049-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="2e049-119">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="2e049-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="2e049-120">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)).</span><span class="sxs-lookup"><span data-stu-id="2e049-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e049-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e049-121">Requirements</span></span>



| <span data-ttu-id="2e049-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e049-122">Requirement</span></span> | <span data-ttu-id="2e049-123">Value</span><span class="sxs-lookup"><span data-stu-id="2e049-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e049-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e049-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2e049-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e049-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2e049-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e049-126">Library</span></span><br/> | <dl> <span data-ttu-id="2e049-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e049-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2e049-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e049-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e049-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="2e049-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
