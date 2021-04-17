---
description: Método de constructor.
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: Constructor CSystemClock. CSystemClock (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fea99d95aa4c1b1cadefbb95384fb871374362f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660939"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="57610-103">Constructor CSystemClock. CSystemClock</span><span class="sxs-lookup"><span data-stu-id="57610-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="57610-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="57610-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57610-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57610-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="57610-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57610-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57610-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="57610-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="57610-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="57610-108">String containing the debug name of the object.</span></span> <span data-ttu-id="57610-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="57610-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="57610-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="57610-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="57610-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="57610-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="57610-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="57610-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="57610-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="57610-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="57610-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="57610-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="57610-115">Puntero al valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57610-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="57610-116">Si se produce un error, el método devuelve un código de error en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="57610-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57610-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57610-117">Requirements</span></span>



| <span data-ttu-id="57610-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="57610-118">Requirement</span></span> | <span data-ttu-id="57610-119">Value</span><span class="sxs-lookup"><span data-stu-id="57610-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57610-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57610-120">Header</span></span><br/>  | <dl> <span data-ttu-id="57610-121"><dt>Sysclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57610-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="57610-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57610-122">Library</span></span><br/> | <dl> <span data-ttu-id="57610-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="57610-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




