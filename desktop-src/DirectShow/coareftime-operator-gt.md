---
description: Este operador comprueba si una hora de referencia es mayor que otra.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: Método COARefTime. Operator> (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671717"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="52653-103">COARefTime. Operator> método)</span><span class="sxs-lookup"><span data-stu-id="52653-103">COARefTime.operator> method</span></span>

<span data-ttu-id="52653-104">Este operador comprueba si una hora de referencia es mayor que otra.</span><span class="sxs-lookup"><span data-stu-id="52653-104">This operator tests if one reference time is greater than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="52653-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52653-105">Syntax</span></span>


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="52653-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52653-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52653-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="52653-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="52653-108">Referencia al objeto **COARefTime** que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="52653-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52653-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52653-109">Return value</span></span>

<span data-ttu-id="52653-110">Devuelve **true** si este objeto es estrictamente mayor que *RT*.</span><span class="sxs-lookup"><span data-stu-id="52653-110">Returns **TRUE** if this object is strictly greater than *rt*.</span></span> <span data-ttu-id="52653-111">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="52653-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="52653-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52653-112">Requirements</span></span>



| <span data-ttu-id="52653-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="52653-113">Requirement</span></span> | <span data-ttu-id="52653-114">Value</span><span class="sxs-lookup"><span data-stu-id="52653-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52653-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52653-115">Header</span></span><br/>  | <dl> <span data-ttu-id="52653-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52653-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="52653-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52653-117">Library</span></span><br/> | <dl> <span data-ttu-id="52653-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="52653-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52653-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="52653-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52653-120">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="52653-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




