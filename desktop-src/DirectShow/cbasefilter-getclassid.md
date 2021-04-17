---
description: 'El método GetClassID recupera el identificador de clase del filtro. Este método implementa el método IPersist:: GetClassID.'
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: Método CBaseFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660714"
---
# <a name="cbasefiltergetclassid-method"></a><span data-ttu-id="09aef-104">CBaseFilter. GetClassID (método)</span><span class="sxs-lookup"><span data-stu-id="09aef-104">CBaseFilter.GetClassID method</span></span>

<span data-ttu-id="09aef-105">El `GetClassID` método recupera el identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="09aef-105">The `GetClassID` method retrieves the class identifier of the filter.</span></span> <span data-ttu-id="09aef-106">Este método implementa el método **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="09aef-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09aef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09aef-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="09aef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09aef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09aef-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="09aef-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="09aef-110">Puntero a una variable que recibe el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="09aef-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09aef-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09aef-111">Return value</span></span>

<span data-ttu-id="09aef-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="09aef-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="09aef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09aef-113">Requirements</span></span>



| <span data-ttu-id="09aef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="09aef-114">Requirement</span></span> | <span data-ttu-id="09aef-115">Value</span><span class="sxs-lookup"><span data-stu-id="09aef-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09aef-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09aef-116">Header</span></span><br/>  | <dl> <span data-ttu-id="09aef-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09aef-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="09aef-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09aef-118">Library</span></span><br/> | <dl> <span data-ttu-id="09aef-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="09aef-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09aef-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="09aef-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09aef-121">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="09aef-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




