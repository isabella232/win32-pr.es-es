---
description: Crea una interfaz de conjunto de animaciones con fotogramas clave ID3DXCompressedAnimationSet que almacena los datos de fotogramas clave en un formato comprimido.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Función D3DXCreateCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003844"
---
# <a name="d3dxcreatecompressedanimationset-function"></a><span data-ttu-id="0cf69-103">D3DXCreateCompressedAnimationSet función)</span><span class="sxs-lookup"><span data-stu-id="0cf69-103">D3DXCreateCompressedAnimationSet function</span></span>

<span data-ttu-id="0cf69-104">Crea una interfaz de conjunto de animaciones con fotogramas clave [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que almacena los datos de fotogramas clave en un formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="0cf69-104">Creates a [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) key framed animation set interface that stores key frame data in a compressed format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf69-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cf69-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="0cf69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cf69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf69-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cf69-109">Puntero al nombre del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="0cf69-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="0cf69-110">*TicksPerSecond* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cf69-112">Número de TICs de fotogramas clave que transcurren por segundo.</span><span class="sxs-lookup"><span data-stu-id="0cf69-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="0cf69-113">*Reproducción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-114">Tipo: **[ **D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="0cf69-115">Tipo del bucle de reproducción establecido de la animación.</span><span class="sxs-lookup"><span data-stu-id="0cf69-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="0cf69-116">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="0cf69-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cf69-117">*pCompressedData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-117">*pCompressedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-118">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-118">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="0cf69-119">Puntero al búfer de [**ID3DXBuffer**](id3dxbuffer.md) que almacena el conjunto de animación como datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="0cf69-119">Pointer to the [**ID3DXBuffer**](id3dxbuffer.md) buffer that stores the animation set as compressed data.</span></span>

</dd> <dt>

<span data-ttu-id="0cf69-120">*NumCallbackKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cf69-122">Número de claves de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0cf69-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="0cf69-123">*pCallKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-124">Tipo: **[**LPD3DXKEY de \_ devolución de llamada**](d3dxkey-callback.md) const \***</span><span class="sxs-lookup"><span data-stu-id="0cf69-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="0cf69-125">Puntero a una estructura de [**\_ devolución de llamada D3DXKEY**](d3dxkey-callback.md) que almacena los datos de devolución de llamada del usuario.</span><span class="sxs-lookup"><span data-stu-id="0cf69-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="0cf69-126">*ppAnimationSet* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-127">Tipo: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cf69-127">Type: **[**LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span></span>

<span data-ttu-id="0cf69-128">Dirección de un puntero a la interfaz [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que almacena los datos de conjuntos de animación fotogramas clave en un formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="0cf69-128">Address of a pointer to the [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) interface that stores key framed animation set data in a compressed format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf69-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cf69-129">Return value</span></span>

<span data-ttu-id="0cf69-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cf69-131">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cf69-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0cf69-132">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0cf69-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf69-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cf69-133">Requirements</span></span>



| <span data-ttu-id="0cf69-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cf69-134">Requirement</span></span> | <span data-ttu-id="0cf69-135">Value</span><span class="sxs-lookup"><span data-stu-id="0cf69-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf69-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cf69-136">Header</span></span><br/>  | <dl> <span data-ttu-id="0cf69-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cf69-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0cf69-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cf69-138">Library</span></span><br/> | <dl> <span data-ttu-id="0cf69-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cf69-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cf69-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cf69-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf69-141">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="0cf69-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
