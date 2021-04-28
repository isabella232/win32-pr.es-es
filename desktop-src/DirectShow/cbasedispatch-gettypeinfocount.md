---
description: 'Método CBaseDispatch.GetTypeInfoCount: el método GetTypeInfoCount recupera el número de interfaces de información de tipo que proporciona el objeto .'
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Método CBaseDispatch.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099893"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="efb7d-103">CBaseDispatch.GetTypeInfoCount (método)</span><span class="sxs-lookup"><span data-stu-id="efb7d-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="efb7d-104">El `GetTypeInfoCount` método recupera el número de interfaces de información de tipo que proporciona el objeto .</span><span class="sxs-lookup"><span data-stu-id="efb7d-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efb7d-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="efb7d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efb7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb7d-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="efb7d-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="efb7d-108">Puntero a una variable que recibe el número de interfaces de información de tipos proporcionadas por el objeto .</span><span class="sxs-lookup"><span data-stu-id="efb7d-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="efb7d-109">Cuando el método vuelve, el valor es 1.</span><span class="sxs-lookup"><span data-stu-id="efb7d-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb7d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efb7d-110">Return value</span></span>

<span data-ttu-id="efb7d-111">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="efb7d-111">Returns one of the following values.</span></span>



| <span data-ttu-id="efb7d-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="efb7d-112">Return code</span></span>                                                                               | <span data-ttu-id="efb7d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="efb7d-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="efb7d-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="efb7d-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="efb7d-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="efb7d-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="efb7d-116"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="efb7d-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="efb7d-117">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="efb7d-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="efb7d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efb7d-118">Requirements</span></span>



| <span data-ttu-id="efb7d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="efb7d-119">Requirement</span></span> | <span data-ttu-id="efb7d-120">Value</span><span class="sxs-lookup"><span data-stu-id="efb7d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb7d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efb7d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="efb7d-122"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="efb7d-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efb7d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efb7d-123">Library</span></span><br/> | <dl> <span data-ttu-id="efb7d-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="efb7d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb7d-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="efb7d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb7d-126">**CBaseDispatch (clase)**</span><span class="sxs-lookup"><span data-stu-id="efb7d-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




