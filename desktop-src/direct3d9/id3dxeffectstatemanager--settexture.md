---
description: Función de devolución de llamada que debe ser implementada por un usuario para establecer una textura.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'ID3DXEffectStateManager:: SetTexture (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547990"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a><span data-ttu-id="a3504-103">ID3DXEffectStateManager:: SetTexture (método)</span><span class="sxs-lookup"><span data-stu-id="a3504-103">ID3DXEffectStateManager::SetTexture method</span></span>

<span data-ttu-id="a3504-104">Función de devolución de llamada que debe ser implementada por un usuario para establecer una textura.</span><span class="sxs-lookup"><span data-stu-id="a3504-104">A callback function that must be implemented by a user to set a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3504-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3504-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="a3504-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3504-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3504-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a3504-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3504-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3504-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3504-109">Fase a la que se asigna la textura.</span><span class="sxs-lookup"><span data-stu-id="a3504-109">The stage to which the texture is assigned.</span></span> <span data-ttu-id="a3504-110">Este es el valor de índice en [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) o [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="a3504-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="a3504-111">*pTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3504-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3504-112">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="a3504-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="a3504-113">Puntero al objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="a3504-113">A pointer to the texture object.</span></span> <span data-ttu-id="a3504-114">Puede ser cualquiera de los tipos de texturas de Direct3D (cubo, volumen, etc.).</span><span class="sxs-lookup"><span data-stu-id="a3504-114">This can be any of the Direct3D texture types (cube, volume, etc.).</span></span> <span data-ttu-id="a3504-115">Vea [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="a3504-115">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3504-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3504-116">Return value</span></span>

<span data-ttu-id="a3504-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3504-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3504-118">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a3504-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="a3504-119">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a3504-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="a3504-120">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="a3504-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="a3504-121">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)).</span><span class="sxs-lookup"><span data-stu-id="a3504-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3504-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3504-122">Requirements</span></span>



| <span data-ttu-id="a3504-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3504-123">Requirement</span></span> | <span data-ttu-id="a3504-124">Value</span><span class="sxs-lookup"><span data-stu-id="a3504-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3504-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3504-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a3504-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3504-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a3504-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3504-127">Library</span></span><br/> | <dl> <span data-ttu-id="a3504-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3504-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a3504-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3504-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3504-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="a3504-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
