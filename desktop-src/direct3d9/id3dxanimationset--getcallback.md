---
description: Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet:: GetCallback (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280505"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="06ae6-103">ID3DXAnimationSet:: GetCallback (método)</span><span class="sxs-lookup"><span data-stu-id="06ae6-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="06ae6-104">Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="06ae6-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ae6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06ae6-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="06ae6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06ae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ae6-107">*Posición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="06ae6-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06ae6-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06ae6-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06ae6-109">Posición desde la que se van a buscar devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="06ae6-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="06ae6-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="06ae6-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06ae6-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06ae6-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06ae6-112">Marcas de búsqueda de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="06ae6-112">Callback search flags.</span></span> <span data-ttu-id="06ae6-113">Este parámetro se puede establecer en una combinación de una o varias marcas de [**las \_ \_ marcas de búsqueda de D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="06ae6-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="06ae6-114">*pCallbackPosition* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06ae6-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06ae6-115">Tipo: **[ **Double**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06ae6-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06ae6-116">Puntero a la posición de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="06ae6-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="06ae6-117">*ppCallbackData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06ae6-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06ae6-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06ae6-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06ae6-119">Dirección del puntero de datos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="06ae6-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06ae6-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06ae6-120">Return value</span></span>

<span data-ttu-id="06ae6-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06ae6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06ae6-122">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="06ae6-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="06ae6-123">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06ae6-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="06ae6-124">En caso contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="06ae6-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06ae6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06ae6-125">Requirements</span></span>



| <span data-ttu-id="06ae6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="06ae6-126">Requirement</span></span> | <span data-ttu-id="06ae6-127">Value</span><span class="sxs-lookup"><span data-stu-id="06ae6-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06ae6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06ae6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="06ae6-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="06ae6-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="06ae6-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06ae6-130">Library</span></span><br/> | <dl> <span data-ttu-id="06ae6-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06ae6-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06ae6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="06ae6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ae6-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="06ae6-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
