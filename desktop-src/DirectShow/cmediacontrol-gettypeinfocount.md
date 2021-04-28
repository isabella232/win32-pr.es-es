---
description: 'Método CMediaControl.GetTypeInfoCount: recupera el número de interfaces de información de tipos proporcionadas por un objeto .'
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Método CMediaControl.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b46838278414442d6c6fc64687fe21e02732e83
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095593"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="19c60-103">Método CMediaControl.GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="19c60-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="19c60-104">Recupera el número de interfaces de información de tipos proporcionadas por un objeto .</span><span class="sxs-lookup"><span data-stu-id="19c60-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19c60-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="19c60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19c60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c60-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="19c60-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="19c60-108">Puntero al número de interfaces de información de tipos que proporciona el objeto .</span><span class="sxs-lookup"><span data-stu-id="19c60-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="19c60-109">Si el objeto proporciona información de tipo, este número es 1; De lo contrario, el número es 0.</span><span class="sxs-lookup"><span data-stu-id="19c60-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c60-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19c60-110">Return value</span></span>

<span data-ttu-id="19c60-111">Devuelve E \_ POINTER si *pctinfo* no es válido; de lo contrario, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19c60-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c60-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19c60-112">Requirements</span></span>



| <span data-ttu-id="19c60-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="19c60-113">Requirement</span></span> | <span data-ttu-id="19c60-114">Value</span><span class="sxs-lookup"><span data-stu-id="19c60-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19c60-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19c60-115">Header</span></span><br/>  | <dl> <span data-ttu-id="19c60-116"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="19c60-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="19c60-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19c60-117">Library</span></span><br/> | <dl> <span data-ttu-id="19c60-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="19c60-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c60-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="19c60-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c60-120">**CMediaControl (clase)**</span><span class="sxs-lookup"><span data-stu-id="19c60-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




