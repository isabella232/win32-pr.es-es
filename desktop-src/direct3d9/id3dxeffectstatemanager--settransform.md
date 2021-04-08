---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer una transformación.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'ID3DXEffectStateManager:: SetTransform (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003878"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a><span data-ttu-id="1fc59-103">ID3DXEffectStateManager:: SetTransform (método)</span><span class="sxs-lookup"><span data-stu-id="1fc59-103">ID3DXEffectStateManager::SetTransform method</span></span>

<span data-ttu-id="1fc59-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una transformación.</span><span class="sxs-lookup"><span data-stu-id="1fc59-104">A callback function that must be implemented by a user to set a transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc59-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fc59-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="1fc59-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fc59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc59-107">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1fc59-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc59-108">Tipo: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc59-108">Type: **[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span></span>

<span data-ttu-id="1fc59-109">Tipo de transformación a la que se va a aplicar la matriz.</span><span class="sxs-lookup"><span data-stu-id="1fc59-109">The type of transform to apply the matrix to.</span></span> <span data-ttu-id="1fc59-110">Vea [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="1fc59-110">See [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc59-111">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1fc59-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc59-112">Tipo: **const [**D3DMATRIX**](d3dmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1fc59-112">Type: **const [**D3DMATRIX**](d3dmatrix.md)\***</span></span>

<span data-ttu-id="1fc59-113">Matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="1fc59-113">A transformation matrix.</span></span> <span data-ttu-id="1fc59-114">Vea [**D3DMATRIX**](d3dmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="1fc59-114">See [**D3DMATRIX**](d3dmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc59-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fc59-115">Return value</span></span>

<span data-ttu-id="1fc59-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fc59-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fc59-117">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="1fc59-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="1fc59-118">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="1fc59-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="1fc59-119">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="1fc59-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="1fc59-120">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)).</span><span class="sxs-lookup"><span data-stu-id="1fc59-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc59-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc59-121">Requirements</span></span>



| <span data-ttu-id="1fc59-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc59-122">Requirement</span></span> | <span data-ttu-id="1fc59-123">Value</span><span class="sxs-lookup"><span data-stu-id="1fc59-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc59-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fc59-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1fc59-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc59-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1fc59-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fc59-126">Library</span></span><br/> | <dl> <span data-ttu-id="1fc59-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fc59-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1fc59-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fc59-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc59-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="1fc59-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
