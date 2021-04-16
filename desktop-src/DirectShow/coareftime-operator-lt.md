---
description: Este operador comprueba si una hora de referencia es menor que otra.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: Método COARefTime. Operator< (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671252"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="2c3f6-103">COARefTime. Operator< método)</span><span class="sxs-lookup"><span data-stu-id="2c3f6-103">COARefTime.operator< method</span></span>

<span data-ttu-id="2c3f6-104">Este operador comprueba si una hora de referencia es menor que otra.</span><span class="sxs-lookup"><span data-stu-id="2c3f6-104">This operator tests if one reference time is less than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c3f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c3f6-105">Syntax</span></span>


```C++
BOOL operator<(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="2c3f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c3f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c3f6-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="2c3f6-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2c3f6-108">Referencia al objeto **COARefTime** que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="2c3f6-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c3f6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c3f6-109">Return value</span></span>

<span data-ttu-id="2c3f6-110">Devuelve **true** si este objeto es estrictamente menor que *RT*.</span><span class="sxs-lookup"><span data-stu-id="2c3f6-110">Returns **TRUE** if this object is strictly less than *rt*.</span></span> <span data-ttu-id="2c3f6-111">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="2c3f6-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c3f6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c3f6-112">Requirements</span></span>



| <span data-ttu-id="2c3f6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c3f6-113">Requirement</span></span> | <span data-ttu-id="2c3f6-114">Value</span><span class="sxs-lookup"><span data-stu-id="2c3f6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3f6-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c3f6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2c3f6-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c3f6-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c3f6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c3f6-117">Library</span></span><br/> | <dl> <span data-ttu-id="2c3f6-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2c3f6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c3f6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c3f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c3f6-120">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="2c3f6-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




