---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer una muestra.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'ID3DXEffectStateManager:: SetSamplerState (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362635"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a><span data-ttu-id="6bf5a-103">ID3DXEffectStateManager:: SetSamplerState (método)</span><span class="sxs-lookup"><span data-stu-id="6bf5a-103">ID3DXEffectStateManager::SetSamplerState method</span></span>

<span data-ttu-id="6bf5a-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una muestra.</span><span class="sxs-lookup"><span data-stu-id="6bf5a-104">A callback function that must be implemented by a user to set a sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf5a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bf5a-105">Syntax</span></span>


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a><span data-ttu-id="6bf5a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bf5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bf5a-107">*Muestra* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6bf5a-107">*Sampler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf5a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bf5a-109">Número de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="6bf5a-109">The zero-based sampler number.</span></span>

</dd> <dt>

<span data-ttu-id="6bf5a-110">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6bf5a-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf5a-111">Tipo: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-111">Type: **[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span></span>

<span data-ttu-id="6bf5a-112">Identifica el estado del muestrario, que puede especificar el filtrado, el direccionamiento o el color del borde.</span><span class="sxs-lookup"><span data-stu-id="6bf5a-112">Identifies sampler state, which can specify the filtering, addressing, or the border color.</span></span> <span data-ttu-id="6bf5a-113">Vea [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="6bf5a-113">See [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bf5a-114">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6bf5a-114">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf5a-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bf5a-116">Un valor de uno de los tipos de estado de muestra en el tipo.</span><span class="sxs-lookup"><span data-stu-id="6bf5a-116">A value from one of the sampler state types in Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bf5a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bf5a-117">Return value</span></span>

<span data-ttu-id="6bf5a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6bf5a-119">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="6bf5a-119">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="6bf5a-120">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="6bf5a-120">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="6bf5a-121">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="6bf5a-121">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="6bf5a-122">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)).</span><span class="sxs-lookup"><span data-stu-id="6bf5a-122">The dynamic effect state call (such as [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bf5a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bf5a-123">Requirements</span></span>



| <span data-ttu-id="6bf5a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bf5a-124">Requirement</span></span> | <span data-ttu-id="6bf5a-125">Value</span><span class="sxs-lookup"><span data-stu-id="6bf5a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf5a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bf5a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6bf5a-127"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bf5a-127"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6bf5a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bf5a-128">Library</span></span><br/> | <dl> <span data-ttu-id="6bf5a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bf5a-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6bf5a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bf5a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bf5a-131">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="6bf5a-131">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
