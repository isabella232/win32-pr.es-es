---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de tipo entero de sombreador de vértices.
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'ID3DXEffectStateManager:: SetPixelShaderConstantI (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2e84d883370038435dc59bb948ef94fcd82223db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718304"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="381be-103">ID3DXEffectStateManager:: SetPixelShaderConstantI (método)</span><span class="sxs-lookup"><span data-stu-id="381be-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="381be-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de tipo entero de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="381be-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="381be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="381be-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="381be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="381be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381be-107">*StartRegister* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="381be-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="381be-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="381be-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="381be-109">Índice de base cero del primer registro constante.</span><span class="sxs-lookup"><span data-stu-id="381be-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="381be-110">*pConstantData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="381be-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="381be-111">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="381be-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="381be-112">Matriz de constantes de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="381be-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="381be-113">*RegisterCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="381be-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="381be-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="381be-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="381be-115">El número de registros en pConstantData.</span><span class="sxs-lookup"><span data-stu-id="381be-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="381be-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="381be-116">Return value</span></span>

<span data-ttu-id="381be-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="381be-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="381be-118">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="381be-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="381be-119">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="381be-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="381be-120">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="381be-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="381be-121">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)).</span><span class="sxs-lookup"><span data-stu-id="381be-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="381be-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="381be-122">Requirements</span></span>



| <span data-ttu-id="381be-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="381be-123">Requirement</span></span> | <span data-ttu-id="381be-124">Value</span><span class="sxs-lookup"><span data-stu-id="381be-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="381be-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="381be-125">Header</span></span><br/>  | <dl> <span data-ttu-id="381be-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="381be-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="381be-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="381be-127">Library</span></span><br/> | <dl> <span data-ttu-id="381be-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="381be-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="381be-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="381be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381be-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="381be-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
