---
description: Método de constructor.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Constructor CPersistStream. CPersistStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680378"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="25311-103">Constructor CPersistStream. CPersistStream</span><span class="sxs-lookup"><span data-stu-id="25311-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="25311-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="25311-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="25311-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25311-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="25311-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25311-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25311-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="25311-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="25311-108">Puntero a la interfaz **IUnknown** del objeto que delega.</span><span class="sxs-lookup"><span data-stu-id="25311-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="25311-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="25311-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="25311-110">Puntero al valor devuelto de COM general.</span><span class="sxs-lookup"><span data-stu-id="25311-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="25311-111">Este valor solo se cambia si se produce un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="25311-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25311-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25311-112">Requirements</span></span>



| <span data-ttu-id="25311-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="25311-113">Requirement</span></span> | <span data-ttu-id="25311-114">Value</span><span class="sxs-lookup"><span data-stu-id="25311-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25311-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25311-115">Header</span></span><br/>  | <dl> <span data-ttu-id="25311-116"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25311-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="25311-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25311-117">Library</span></span><br/> | <dl> <span data-ttu-id="25311-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="25311-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25311-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="25311-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25311-120">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="25311-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




