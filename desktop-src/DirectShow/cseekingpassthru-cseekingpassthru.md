---
description: Método de constructor.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Constructor CSeekingPassThru. CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a93ed9706762b9a1672bfae85550ee4c2aceeead
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670403"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="43249-103">Constructor CSeekingPassThru. CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="43249-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="43249-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="43249-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43249-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43249-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="43249-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43249-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43249-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="43249-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="43249-108">Cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="43249-108">String containing the name of the object.</span></span> <span data-ttu-id="43249-109">Vea [**CBaseObject**](cbaseobject.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="43249-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="43249-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="43249-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="43249-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="43249-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="43249-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="43249-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="43249-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="43249-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43249-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="43249-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="43249-115">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43249-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="43249-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="43249-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43249-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43249-117">Requirements</span></span>



| <span data-ttu-id="43249-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="43249-118">Requirement</span></span> | <span data-ttu-id="43249-119">Value</span><span class="sxs-lookup"><span data-stu-id="43249-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43249-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43249-120">Header</span></span><br/>  | <dl> <span data-ttu-id="43249-121"><dt>Seekpt. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43249-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="43249-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43249-122">Library</span></span><br/> | <dl> <span data-ttu-id="43249-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="43249-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43249-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="43249-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43249-125">**Clase CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="43249-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




