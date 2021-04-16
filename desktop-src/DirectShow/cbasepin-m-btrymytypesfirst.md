---
description: Marca que indica si el PIN intenta sus propios tipos de medios preferidos antes de los del PIN receptor.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Miembro CBasePin:: m_bTryMyTypesFirst (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671446"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a><span data-ttu-id="eb9a3-103">Miembro bTryMyTypesFirst CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="eb9a3-103">CBasePin::m\_bTryMyTypesFirst member</span></span>

<span data-ttu-id="eb9a3-104">Marca que indica si el PIN intenta sus propios tipos de medios preferidos antes de los del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="eb9a3-104">Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb9a3-105">Syntax</span></span>


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a><span data-ttu-id="eb9a3-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb9a3-106">Remarks</span></span>

<span data-ttu-id="eb9a3-107">El valor predeterminado de esta marca **es false**.</span><span class="sxs-lookup"><span data-stu-id="eb9a3-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="eb9a3-108">Si la marca es **true**, el método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) invierte el orden en el que prueba los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="eb9a3-108">If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9a3-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb9a3-109">Requirements</span></span>



| <span data-ttu-id="eb9a3-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb9a3-110">Requirement</span></span> | <span data-ttu-id="eb9a3-111">Value</span><span class="sxs-lookup"><span data-stu-id="eb9a3-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9a3-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb9a3-112">Header</span></span><br/>  | <dl> <span data-ttu-id="eb9a3-113"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb9a3-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb9a3-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb9a3-114">Library</span></span><br/> | <dl> <span data-ttu-id="eb9a3-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="eb9a3-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb9a3-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb9a3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9a3-117">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="eb9a3-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




