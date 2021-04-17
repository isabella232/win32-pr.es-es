---
description: 'El método GetClassID recupera el identificador de clase. Este método implementa el método IPersist:: GetClassID.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Método CBaseMediaFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660254"
---
# <a name="cbasemediafiltergetclassid-method"></a><span data-ttu-id="ca42e-104">CBaseMediaFilter. GetClassID (método)</span><span class="sxs-lookup"><span data-stu-id="ca42e-104">CBaseMediaFilter.GetClassID method</span></span>

<span data-ttu-id="ca42e-105">El `GetClassID` método recupera el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="ca42e-105">The `GetClassID` method retrieves the class identifier.</span></span> <span data-ttu-id="ca42e-106">Este método implementa el método **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="ca42e-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca42e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca42e-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="ca42e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca42e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca42e-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="ca42e-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="ca42e-110">Puntero a una variable que recibe el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="ca42e-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca42e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca42e-111">Return value</span></span>

<span data-ttu-id="ca42e-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="ca42e-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca42e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca42e-113">Requirements</span></span>



| <span data-ttu-id="ca42e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca42e-114">Requirement</span></span> | <span data-ttu-id="ca42e-115">Value</span><span class="sxs-lookup"><span data-stu-id="ca42e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca42e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca42e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ca42e-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca42e-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca42e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca42e-118">Library</span></span><br/> | <dl> <span data-ttu-id="ca42e-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ca42e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca42e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca42e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca42e-121">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="ca42e-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




