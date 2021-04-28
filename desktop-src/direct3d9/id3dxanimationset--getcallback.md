---
description: 'Método ID3DXAnimationSet::GetCallback: obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: Método ID3DXAnimationSet::GetCallback (D3dx9anim.h)
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
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097543"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="f735c-103">Método ID3DXAnimationSet::GetCallback</span><span class="sxs-lookup"><span data-stu-id="f735c-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="f735c-104">Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="f735c-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f735c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f735c-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="f735c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f735c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f735c-107">*Posición* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f735c-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f735c-108">Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f735c-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f735c-109">Posición desde la que se buscarán las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="f735c-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="f735c-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f735c-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f735c-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f735c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f735c-112">Marcas de búsqueda de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f735c-112">Callback search flags.</span></span> <span data-ttu-id="f735c-113">Este parámetro se puede establecer en una combinación de una o varias marcas de [**D3DXCALLBACK \_ SEARCH \_ FLAGS**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f735c-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f735c-114">*pCallbackPosition* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f735c-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f735c-115">Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f735c-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f735c-116">Puntero a la posición de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f735c-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="f735c-117">*ppCallbackData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f735c-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f735c-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f735c-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f735c-119">Dirección del puntero de datos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f735c-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f735c-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f735c-120">Return value</span></span>

<span data-ttu-id="f735c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f735c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f735c-122">Los valores devueltos de este método los implementa un programador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f735c-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="f735c-123">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f735c-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="f735c-124">De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR.**](./d3dxerr.md)</span><span class="sxs-lookup"><span data-stu-id="f735c-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f735c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f735c-125">Requirements</span></span>



| <span data-ttu-id="f735c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f735c-126">Requirement</span></span> | <span data-ttu-id="f735c-127">Value</span><span class="sxs-lookup"><span data-stu-id="f735c-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f735c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f735c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f735c-129"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="f735c-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f735c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f735c-130">Library</span></span><br/> | <dl> <span data-ttu-id="f735c-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f735c-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f735c-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f735c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f735c-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="f735c-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
