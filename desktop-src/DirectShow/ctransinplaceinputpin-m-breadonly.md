---
Description: Marca que especifica si el flujo de entrada es de solo lectura. El filtro de nivel superior especifica esta información cuando llama al método NotifyAllocator. De forma predeterminada, el valor es FALSE.
ms.assetid: d5a71c00-326c-45b4-b9c5-b67a0fe71bf5
title: 'Miembro CTransInPlaceInputPin:: m_bReadOnly (TRANSip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bReadOnly
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2f66296c08b2461440e0615b225c62405fd99a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660362"
---
# <a name="ctransinplaceinputpinm_breadonly-member"></a><span data-ttu-id="032a8-105">Miembro bReadOnly CTransInPlaceInputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="032a8-105">CTransInPlaceInputPin::m\_bReadOnly member</span></span>

<span data-ttu-id="032a8-106">Marca que especifica si el flujo de entrada es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="032a8-106">Flag that specifies whether the input stream is read-only.</span></span> <span data-ttu-id="032a8-107">El filtro de nivel superior especifica esta información cuando llama al método [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="032a8-107">The upstream filter specifies this information when it calls the [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md) method.</span></span> <span data-ttu-id="032a8-108">De forma predeterminada, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="032a8-108">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="032a8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="032a8-109">Syntax</span></span>


```C++
BOOL m_bReadOnly;
```



## <a name="requirements"></a><span data-ttu-id="032a8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032a8-110">Requirements</span></span>



| <span data-ttu-id="032a8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="032a8-111">Requirement</span></span> | <span data-ttu-id="032a8-112">Value</span><span class="sxs-lookup"><span data-stu-id="032a8-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032a8-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="032a8-113">Header</span></span><br/>  | <dl> <span data-ttu-id="032a8-114"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="032a8-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="032a8-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="032a8-115">Library</span></span><br/> | <dl> <span data-ttu-id="032a8-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="032a8-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032a8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="032a8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032a8-118">**Clase CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="032a8-118">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




