---
description: Marca que indica si se ha producido un error en tiempo de ejecución.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Miembro CBasePin:: m_bRunTimeError (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661253"
---
# <a name="cbasepinm_bruntimeerror-member"></a><span data-ttu-id="b1517-103">Miembro bRunTimeError CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="b1517-103">CBasePin::m\_bRunTimeError member</span></span>

<span data-ttu-id="b1517-104">Marca que indica si se ha producido un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b1517-104">Flag that indicates whether a run-time error has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1517-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1517-105">Syntax</span></span>


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a><span data-ttu-id="b1517-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1517-106">Remarks</span></span>

<span data-ttu-id="b1517-107">El valor predeterminado de esta marca **es false**.</span><span class="sxs-lookup"><span data-stu-id="b1517-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="b1517-108">Establezca la marca en **true** si se produce un error de tiempo de ejecución durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="b1517-108">Set the flag to **TRUE** if a run-time error occurs during streaming.</span></span> <span data-ttu-id="b1517-109">El método [**CBasePin:: Inactive**](cbasepin-inactive.md) restablece la marca en **false**.</span><span class="sxs-lookup"><span data-stu-id="b1517-109">The [**CBasePin::Inactive**](cbasepin-inactive.md) method resets the flag to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1517-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1517-110">Requirements</span></span>



| <span data-ttu-id="b1517-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1517-111">Requirement</span></span> | <span data-ttu-id="b1517-112">Value</span><span class="sxs-lookup"><span data-stu-id="b1517-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1517-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1517-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b1517-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1517-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b1517-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1517-115">Library</span></span><br/> | <dl> <span data-ttu-id="b1517-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b1517-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1517-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1517-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1517-118">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="b1517-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




