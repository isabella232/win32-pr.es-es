---
description: La función GetSubtypeName recupera el nombre legible de un subtipo de vídeo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Función GetSubtypeName (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653836"
---
# <a name="getsubtypename-function"></a><span data-ttu-id="3e55e-103">GetSubtypeName función)</span><span class="sxs-lookup"><span data-stu-id="3e55e-103">GetSubtypeName function</span></span>

<span data-ttu-id="3e55e-104">La `GetSubtypeName` función recupera el nombre legible de un subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3e55e-104">The `GetSubtypeName` function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e55e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e55e-105">Syntax</span></span>


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="3e55e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e55e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e55e-107">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="3e55e-107">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="3e55e-108">Puntero a un **GUID** de subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3e55e-108">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e55e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e55e-109">Return value</span></span>

<span data-ttu-id="3e55e-110">Devuelve una cadena que contiene el nombre.</span><span class="sxs-lookup"><span data-stu-id="3e55e-110">Returns a string containing the name.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e55e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e55e-111">Requirements</span></span>



| <span data-ttu-id="3e55e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e55e-112">Requirement</span></span> | <span data-ttu-id="3e55e-113">Value</span><span class="sxs-lookup"><span data-stu-id="3e55e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e55e-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e55e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3e55e-115"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e55e-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3e55e-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e55e-116">Library</span></span><br/> | <dl> <span data-ttu-id="3e55e-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3e55e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e55e-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e55e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e55e-119">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="3e55e-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




