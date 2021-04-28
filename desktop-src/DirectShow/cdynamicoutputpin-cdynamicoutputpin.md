---
description: 'Constructor CDynamicOutputPin.CDynamicOutputPin: método constructor.'
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Constructor CDynamicOutputPin.CDynamicOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099313"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="eb7b2-103">Constructor CDynamicOutputPin.CDynamicOutputPin</span><span class="sxs-lookup"><span data-stu-id="eb7b2-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="eb7b2-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb7b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb7b2-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="eb7b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb7b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb7b2-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="eb7b2-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7b2-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="eb7b2-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="eb7b2-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb7b2-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="eb7b2-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7b2-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="eb7b2-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="eb7b2-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7b2-113">Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="eb7b2-114">Use la misma sección crítica que el bloqueo de filtro, [ **CBaseFilter::m \_ pLock.**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="eb7b2-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="eb7b2-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="eb7b2-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7b2-116">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="eb7b2-117">Inicialice el valor en S \_ OK antes de crear el objeto .</span><span class="sxs-lookup"><span data-stu-id="eb7b2-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="eb7b2-118">El valor solo se cambia si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="eb7b2-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="eb7b2-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7b2-120">Puntero a una cadena de caracteres anchos que contiene el identificador de pin.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="eb7b2-121">Para obtener más información, [**vea IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="eb7b2-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb7b2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb7b2-122">Requirements</span></span>



| <span data-ttu-id="eb7b2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb7b2-123">Requirement</span></span> | <span data-ttu-id="eb7b2-124">Value</span><span class="sxs-lookup"><span data-stu-id="eb7b2-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb7b2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb7b2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eb7b2-126"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb7b2-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb7b2-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb7b2-127">Library</span></span><br/> | <dl> <span data-ttu-id="eb7b2-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="eb7b2-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb7b2-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eb7b2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb7b2-130">**CDynamicOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="eb7b2-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




