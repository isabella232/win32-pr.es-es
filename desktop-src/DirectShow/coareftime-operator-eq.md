---
description: Este operador comprueba la igualdad entre dos tiempos de referencia.
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: Método COARefTime. Operator = = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b19f7b75be840a293920b36fe5ab63d30520d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681161"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="efdaf-103">COARefTime. Operator = = (método)</span><span class="sxs-lookup"><span data-stu-id="efdaf-103">COARefTime.operator== method</span></span>

<span data-ttu-id="efdaf-104">Este operador comprueba la igualdad entre dos tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="efdaf-104">This operator tests for equality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="efdaf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efdaf-105">Syntax</span></span>


```C++
BOOL operator==(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="efdaf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efdaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efdaf-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="efdaf-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="efdaf-108">Referencia al objeto **COARefTime** que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="efdaf-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efdaf-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efdaf-109">Return value</span></span>

<span data-ttu-id="efdaf-110">Devuelve **true** si los dos objetos son iguales.</span><span class="sxs-lookup"><span data-stu-id="efdaf-110">Returns **TRUE** if the two objects are equal.</span></span> <span data-ttu-id="efdaf-111">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="efdaf-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="efdaf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efdaf-112">Requirements</span></span>



| <span data-ttu-id="efdaf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="efdaf-113">Requirement</span></span> | <span data-ttu-id="efdaf-114">Value</span><span class="sxs-lookup"><span data-stu-id="efdaf-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efdaf-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efdaf-115">Header</span></span><br/>  | <dl> <span data-ttu-id="efdaf-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efdaf-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efdaf-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efdaf-117">Library</span></span><br/> | <dl> <span data-ttu-id="efdaf-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="efdaf-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efdaf-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="efdaf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efdaf-120">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="efdaf-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




