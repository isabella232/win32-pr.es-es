---
description: Función de devolución de llamada que debe ser implementada por un usuario para habilitar o deshabilitar una luz.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'ID3DXEffectStateManager:: LightEnable (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280404"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a><span data-ttu-id="c212a-103">ID3DXEffectStateManager:: LightEnable (método)</span><span class="sxs-lookup"><span data-stu-id="c212a-103">ID3DXEffectStateManager::LightEnable method</span></span>

<span data-ttu-id="c212a-104">Función de devolución de llamada que debe ser implementada por un usuario para habilitar o deshabilitar una luz.</span><span class="sxs-lookup"><span data-stu-id="c212a-104">A callback function that must be implemented by a user to enable/disable a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="c212a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c212a-105">Syntax</span></span>


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a><span data-ttu-id="c212a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c212a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c212a-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c212a-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c212a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c212a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c212a-109">Índice de base cero de la luz.</span><span class="sxs-lookup"><span data-stu-id="c212a-109">The zero-based index of the light.</span></span> <span data-ttu-id="c212a-110">Este es el mismo índice en [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="c212a-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="c212a-111">*Habilitar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c212a-111">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c212a-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c212a-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c212a-113">True para habilitar la luz; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="c212a-113">True to enable the light, false otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c212a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c212a-114">Return value</span></span>

<span data-ttu-id="c212a-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c212a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c212a-116">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c212a-116">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c212a-117">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="c212a-117">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="c212a-118">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="c212a-118">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="c212a-119">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)).</span><span class="sxs-lookup"><span data-stu-id="c212a-119">The dynamic effect state call (such as [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c212a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c212a-120">Requirements</span></span>



| <span data-ttu-id="c212a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c212a-121">Requirement</span></span> | <span data-ttu-id="c212a-122">Value</span><span class="sxs-lookup"><span data-stu-id="c212a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c212a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c212a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c212a-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c212a-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c212a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c212a-125">Library</span></span><br/> | <dl> <span data-ttu-id="c212a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c212a-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c212a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c212a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c212a-128">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="c212a-128">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
