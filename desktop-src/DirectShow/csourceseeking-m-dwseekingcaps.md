---
description: Funciones de búsqueda.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Miembro CSourceSeeking:: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660774"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a><span data-ttu-id="baeb0-103">Miembro dwSeekingCaps CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="baeb0-103">CSourceSeeking::m\_dwSeekingCaps member</span></span>

<span data-ttu-id="baeb0-104">Funciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="baeb0-104">Seeking capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="baeb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baeb0-105">Syntax</span></span>


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a><span data-ttu-id="baeb0-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="baeb0-106">Remarks</span></span>

<span data-ttu-id="baeb0-107">De forma predeterminada, el valor se establece en la combinación bit a bit de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="baeb0-107">By default, the value is set to the bitwise combination of the following flags:</span></span>

-   <span data-ttu-id="baeb0-108">\_Búsqueda de \_ CanSeekForwards</span><span class="sxs-lookup"><span data-stu-id="baeb0-108">AM\_SEEKING\_CanSeekForwards</span></span>
-   <span data-ttu-id="baeb0-109">\_Búsqueda de \_ CanSeekBackwards</span><span class="sxs-lookup"><span data-stu-id="baeb0-109">AM\_SEEKING\_CanSeekBackwards</span></span>
-   <span data-ttu-id="baeb0-110">\_Búsqueda de \_ CanSeekAbsolute</span><span class="sxs-lookup"><span data-stu-id="baeb0-110">AM\_SEEKING\_CanSeekAbsolute</span></span>
-   <span data-ttu-id="baeb0-111">\_Búsqueda de \_ CanGetStopPos</span><span class="sxs-lookup"><span data-stu-id="baeb0-111">AM\_SEEKING\_CanGetStopPos</span></span>
-   <span data-ttu-id="baeb0-112">\_Búsqueda de \_ CanGetDuration</span><span class="sxs-lookup"><span data-stu-id="baeb0-112">AM\_SEEKING\_CanGetDuration</span></span>

<span data-ttu-id="baeb0-113">Si el filtro admite un conjunto diferente de funcionalidades, Invalide este valor.</span><span class="sxs-lookup"><span data-stu-id="baeb0-113">If the filter supports a different set of capabilities, override this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="baeb0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baeb0-114">Requirements</span></span>



| <span data-ttu-id="baeb0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="baeb0-115">Requirement</span></span> | <span data-ttu-id="baeb0-116">Value</span><span class="sxs-lookup"><span data-stu-id="baeb0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baeb0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="baeb0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="baeb0-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="baeb0-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="baeb0-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="baeb0-119">Library</span></span><br/> | <dl> <span data-ttu-id="baeb0-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="baeb0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baeb0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="baeb0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baeb0-122">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="baeb0-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




