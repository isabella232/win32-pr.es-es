---
description: Este operador comprueba la desigualdad entre dos tiempos de referencia.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: Método COARefTime. Operator! = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671246"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="ec377-103">COARefTime. Operator! = (método)</span><span class="sxs-lookup"><span data-stu-id="ec377-103">COARefTime.operator!= method</span></span>

<span data-ttu-id="ec377-104">Este operador comprueba la desigualdad entre dos tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="ec377-104">This operator tests for inequality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec377-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec377-105">Syntax</span></span>


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="ec377-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec377-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec377-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="ec377-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ec377-108">Referencia al objeto **COARefTime** que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="ec377-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec377-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec377-109">Return value</span></span>

<span data-ttu-id="ec377-110">Devuelve **true** si los dos objetos no son iguales.</span><span class="sxs-lookup"><span data-stu-id="ec377-110">Returns **TRUE** if the two objects are not equal.</span></span> <span data-ttu-id="ec377-111">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="ec377-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec377-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec377-112">Requirements</span></span>



| <span data-ttu-id="ec377-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec377-113">Requirement</span></span> | <span data-ttu-id="ec377-114">Value</span><span class="sxs-lookup"><span data-stu-id="ec377-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec377-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec377-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ec377-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec377-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec377-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec377-117">Library</span></span><br/> | <dl> <span data-ttu-id="ec377-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ec377-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec377-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec377-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec377-120">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="ec377-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




