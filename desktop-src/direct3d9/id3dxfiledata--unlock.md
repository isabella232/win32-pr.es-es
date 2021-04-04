---
description: 'Finaliza la duración del puntero ppData devuelto por ID3DXFileData:: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'ID3DXFileData:: Unlock (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821210"
---
# <a name="id3dxfiledataunlock-method"></a><span data-ttu-id="cab16-103">ID3DXFileData:: Unlock (método)</span><span class="sxs-lookup"><span data-stu-id="cab16-103">ID3DXFileData::Unlock method</span></span>

<span data-ttu-id="cab16-104">Finaliza la duración del puntero *ppData* devuelto por [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="cab16-104">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cab16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cab16-105">Syntax</span></span>


```C++
BOOL Unlock();
```



## <a name="parameters"></a><span data-ttu-id="cab16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cab16-106">Parameters</span></span>

<span data-ttu-id="cab16-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cab16-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cab16-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cab16-108">Return value</span></span>

<span data-ttu-id="cab16-109">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cab16-109">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cab16-110">El valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cab16-110">The return value is S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab16-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cab16-111">Remarks</span></span>

<span data-ttu-id="cab16-112">Debe asegurarse de que el número de llamadas a [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) coincide con el número de llamadas a **ID3DXFileData:: Unlock** .</span><span class="sxs-lookup"><span data-stu-id="cab16-112">You must ensure that the number of [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) calls matches the number of **ID3DXFileData::Unlock** calls.</span></span> <span data-ttu-id="cab16-113">Después de llamar a Unlock, el puntero ppData devuelto por **ID3DXFileData:: Lock** ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cab16-113">After calling Unlock, the ppData pointer returned by **ID3DXFileData::Lock** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab16-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cab16-114">Requirements</span></span>



| <span data-ttu-id="cab16-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cab16-115">Requirement</span></span> | <span data-ttu-id="cab16-116">Value</span><span class="sxs-lookup"><span data-stu-id="cab16-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cab16-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cab16-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cab16-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="cab16-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="cab16-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cab16-119">Library</span></span><br/> | <dl> <span data-ttu-id="cab16-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cab16-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cab16-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="cab16-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab16-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="cab16-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
