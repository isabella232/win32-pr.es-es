---
description: 'Constructor CSystemClock.CSystemClock: método constructor.'
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: Constructor CSystemClock.CSystemClock (Sysclock.h)
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
ms.openlocfilehash: 11ba7449b086f84dc2caff19da922c03f9c7103b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095203"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="b8946-103">Constructor CSystemClock.CSystemClock</span><span class="sxs-lookup"><span data-stu-id="b8946-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="b8946-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="b8946-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8946-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8946-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b8946-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8946-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8946-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="b8946-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b8946-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8946-108">String containing the debug name of the object.</span></span> <span data-ttu-id="b8946-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="b8946-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8946-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="b8946-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b8946-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="b8946-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="b8946-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="b8946-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="b8946-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="b8946-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8946-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="b8946-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b8946-115">Puntero al **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b8946-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="b8946-116">Si se produce un error, el método devuelve un código de error en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="b8946-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8946-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8946-117">Requirements</span></span>



| <span data-ttu-id="b8946-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8946-118">Requirement</span></span> | <span data-ttu-id="b8946-119">Value</span><span class="sxs-lookup"><span data-stu-id="b8946-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8946-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8946-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b8946-121"><dt>Sysclock.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8946-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b8946-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8946-122">Library</span></span><br/> | <dl> <span data-ttu-id="b8946-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b8946-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




