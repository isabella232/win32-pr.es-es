---
description: Cree un grupo de efectos. Un grupo se utiliza para compartir parámetros entre efectos.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Función D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280474"
---
# <a name="d3dxcreateeffectpool-function"></a><span data-ttu-id="6e738-104">D3DXCreateEffectPool función)</span><span class="sxs-lookup"><span data-stu-id="6e738-104">D3DXCreateEffectPool function</span></span>

<span data-ttu-id="6e738-105">Cree un grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="6e738-105">Create an effect pool.</span></span> <span data-ttu-id="6e738-106">Un grupo se utiliza para compartir parámetros entre efectos.</span><span class="sxs-lookup"><span data-stu-id="6e738-106">A pool is used to share parameters between effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e738-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e738-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="6e738-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e738-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e738-109">*ppPool* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e738-109">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e738-110">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e738-110">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="6e738-111">Devuelve un puntero al grupo creado.</span><span class="sxs-lookup"><span data-stu-id="6e738-111">Returns a pointer to the created pool.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e738-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e738-112">Return value</span></span>

<span data-ttu-id="6e738-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e738-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e738-114">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e738-114">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="6e738-115">Si los argumentos no son válidos, el método devolverá D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6e738-115">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="6e738-116">Si se produce un error en el método, el valor devuelto será E \_ producirá un error.</span><span class="sxs-lookup"><span data-stu-id="6e738-116">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e738-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e738-117">Remarks</span></span>

<span data-ttu-id="6e738-118">En el caso de los efectos de un grupo, los parámetros compartidos con el mismo nombre comparten los mismos valores.</span><span class="sxs-lookup"><span data-stu-id="6e738-118">For effects within a pool, shared parameters with the same name share values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e738-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e738-119">Requirements</span></span>



| <span data-ttu-id="6e738-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e738-120">Requirement</span></span> | <span data-ttu-id="6e738-121">Value</span><span class="sxs-lookup"><span data-stu-id="6e738-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e738-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e738-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6e738-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e738-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6e738-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e738-124">Library</span></span><br/> | <dl> <span data-ttu-id="6e738-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e738-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6e738-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e738-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e738-127">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="6e738-127">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




