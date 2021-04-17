---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer el estado del material.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'ID3DXEffectStateManager:: SetMaterial (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698302"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a><span data-ttu-id="d43e3-103">ID3DXEffectStateManager:: SetMaterial (método)</span><span class="sxs-lookup"><span data-stu-id="d43e3-103">ID3DXEffectStateManager::SetMaterial method</span></span>

<span data-ttu-id="d43e3-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer el estado del material.</span><span class="sxs-lookup"><span data-stu-id="d43e3-104">A callback function that must be implemented by a user to set material state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d43e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d43e3-105">Syntax</span></span>


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a><span data-ttu-id="d43e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d43e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d43e3-107">*pMaterial* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d43e3-107">*pMaterial* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d43e3-108">Tipo: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***</span><span class="sxs-lookup"><span data-stu-id="d43e3-108">Type: **const [**D3DMATERIAL9**](d3dmaterial9.md)\***</span></span>

<span data-ttu-id="d43e3-109">Puntero al estado del material.</span><span class="sxs-lookup"><span data-stu-id="d43e3-109">A pointer to the material state.</span></span> <span data-ttu-id="d43e3-110">Vea [**D3DMATERIAL9**](d3dmaterial9.md).</span><span class="sxs-lookup"><span data-stu-id="d43e3-110">See [**D3DMATERIAL9**](d3dmaterial9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d43e3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d43e3-111">Return value</span></span>

<span data-ttu-id="d43e3-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d43e3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d43e3-113">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="d43e3-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="d43e3-114">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="d43e3-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="d43e3-115">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="d43e3-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="d43e3-116">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)).</span><span class="sxs-lookup"><span data-stu-id="d43e3-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d43e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d43e3-117">Requirements</span></span>



| <span data-ttu-id="d43e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d43e3-118">Requirement</span></span> | <span data-ttu-id="d43e3-119">Value</span><span class="sxs-lookup"><span data-stu-id="d43e3-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d43e3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d43e3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d43e3-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d43e3-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d43e3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d43e3-122">Library</span></span><br/> | <dl> <span data-ttu-id="d43e3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d43e3-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d43e3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d43e3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d43e3-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="d43e3-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
