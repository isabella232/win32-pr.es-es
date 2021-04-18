---
description: Crea una interfaz de conjunto de animaciones con fotogramas clave ID3DXKeyframedAnimationSet.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Función D3DXCreateKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698347"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a><span data-ttu-id="3f0b7-103">D3DXCreateKeyframedAnimationSet función)</span><span class="sxs-lookup"><span data-stu-id="3f0b7-103">D3DXCreateKeyframedAnimationSet function</span></span>

<span data-ttu-id="3f0b7-104">Crea una interfaz de conjunto de animaciones con fotogramas clave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0b7-104">Creates a [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f0b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f0b7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="3f0b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f0b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f0b7-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f0b7-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0b7-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f0b7-109">Puntero al nombre del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="3f0b7-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="3f0b7-110">*TicksPerSecond* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f0b7-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0b7-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f0b7-112">Número de TICs de fotogramas clave que transcurren por segundo.</span><span class="sxs-lookup"><span data-stu-id="3f0b7-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="3f0b7-113">*Reproducción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3f0b7-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0b7-114">Tipo: **[ **D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="3f0b7-115">Tipo del bucle de reproducción establecido de la animación.</span><span class="sxs-lookup"><span data-stu-id="3f0b7-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="3f0b7-116">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="3f0b7-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f0b7-117">*NumAnimations* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f0b7-117">*NumAnimations* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0b7-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f0b7-119">Número de conjuntos de animaciones de escala, giro y traslación (SRT).</span><span class="sxs-lookup"><span data-stu-id="3f0b7-119">Number of scale, rotate, and translate (SRT) animation sets.</span></span>

</dd> <dt>

<span data-ttu-id="3f0b7-120">*NumCallbackKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f0b7-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0b7-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f0b7-122">Número de claves de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3f0b7-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="3f0b7-123">*pCallKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f0b7-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0b7-124">Tipo: **[**LPD3DXKEY de \_ devolución de llamada**](d3dxkey-callback.md) const \***</span><span class="sxs-lookup"><span data-stu-id="3f0b7-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="3f0b7-125">Puntero a una estructura de [**\_ devolución de llamada D3DXKEY**](d3dxkey-callback.md) que almacena los datos de devolución de llamada del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f0b7-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="3f0b7-126">*ppAnimationSet* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f0b7-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0b7-127">Tipo: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f0b7-127">Type: **[**LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span></span>

<span data-ttu-id="3f0b7-128">Dirección de un puntero a la interfaz de conjunto de animación con fotogramas clave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0b7-128">Address of a pointer to the [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f0b7-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f0b7-129">Return value</span></span>

<span data-ttu-id="3f0b7-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f0b7-131">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f0b7-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3f0b7-132">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3f0b7-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f0b7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f0b7-133">Requirements</span></span>



| <span data-ttu-id="3f0b7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f0b7-134">Requirement</span></span> | <span data-ttu-id="3f0b7-135">Value</span><span class="sxs-lookup"><span data-stu-id="3f0b7-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0b7-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f0b7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3f0b7-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f0b7-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3f0b7-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f0b7-138">Library</span></span><br/> | <dl> <span data-ttu-id="3f0b7-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f0b7-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f0b7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f0b7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0b7-141">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="3f0b7-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
