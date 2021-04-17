---
description: Cambia la marca de modificado del flujo actual.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Método CPersistStream. SetDirty (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680373"
---
# <a name="cpersiststreamsetdirty-method"></a><span data-ttu-id="3c109-103">CPersistStream. SetDirty, método</span><span class="sxs-lookup"><span data-stu-id="3c109-103">CPersistStream.SetDirty method</span></span>

<span data-ttu-id="3c109-104">Cambia la marca de modificado del flujo actual.</span><span class="sxs-lookup"><span data-stu-id="3c109-104">Changes the dirty flag for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c109-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c109-105">Syntax</span></span>


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a><span data-ttu-id="3c109-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c109-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c109-107">*fDirty*</span><span class="sxs-lookup"><span data-stu-id="3c109-107">*fDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="3c109-108">Nueva marca de modificado para esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="3c109-108">New dirty flag for this stream.</span></span> <span data-ttu-id="3c109-109">**True** significa que los datos no se han guardado.</span><span class="sxs-lookup"><span data-stu-id="3c109-109">**TRUE** means that the data has not been saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c109-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c109-110">Return value</span></span>

<span data-ttu-id="3c109-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c109-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c109-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c109-112">Requirements</span></span>



| <span data-ttu-id="3c109-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c109-113">Requirement</span></span> | <span data-ttu-id="3c109-114">Value</span><span class="sxs-lookup"><span data-stu-id="3c109-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c109-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c109-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3c109-116"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c109-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c109-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c109-117">Library</span></span><br/> | <dl> <span data-ttu-id="3c109-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3c109-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c109-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c109-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c109-120">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="3c109-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




