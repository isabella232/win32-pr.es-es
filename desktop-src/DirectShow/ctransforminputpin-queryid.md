---
description: 'Método CTransformInputPin.QueryId: el método QueryId recupera un identificador para el pin. Este método implementa el método IPin::QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Método CTransformInputPin.QueryId (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8407e649814fcb12f699c2362f0f89137e941d19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095013"
---
# <a name="ctransforminputpinqueryid-method"></a><span data-ttu-id="92b84-104">Método CTransformInputPin.QueryId</span><span class="sxs-lookup"><span data-stu-id="92b84-104">CTransformInputPin.QueryId method</span></span>

<span data-ttu-id="92b84-105">El `QueryId` método recupera un identificador para el pin.</span><span class="sxs-lookup"><span data-stu-id="92b84-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="92b84-106">Este método implementa el [**método IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)</span><span class="sxs-lookup"><span data-stu-id="92b84-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b84-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92b84-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="92b84-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92b84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b84-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="92b84-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="92b84-110">Recibe una cadena que contiene el identificador de pin.</span><span class="sxs-lookup"><span data-stu-id="92b84-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b84-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92b84-111">Return value</span></span>

<span data-ttu-id="92b84-112">Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="92b84-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="92b84-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="92b84-113">Return code</span></span>                                                                                   | <span data-ttu-id="92b84-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="92b84-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="92b84-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92b84-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="92b84-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="92b84-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="92b84-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="92b84-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="92b84-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="92b84-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="92b84-119"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="92b84-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="92b84-120">**Argumento de** puntero NULL</span><span class="sxs-lookup"><span data-stu-id="92b84-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92b84-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92b84-121">Remarks</span></span>

<span data-ttu-id="92b84-122">El identificador de pin se usa para la persistencia del grafo.</span><span class="sxs-lookup"><span data-stu-id="92b84-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="92b84-123">El identificador de pin de esta clase es In.</span><span class="sxs-lookup"><span data-stu-id="92b84-123">The pin identifier for this class is In.</span></span> <span data-ttu-id="92b84-124">Esta clase invalida el comportamiento de la [**clase CBasePin.**](cbasepin.md)</span><span class="sxs-lookup"><span data-stu-id="92b84-124">This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="92b84-125">En la **clase CBasePin,** el identificador de pin es el mismo que el nombre del pin, especificado en el constructor de clase.</span><span class="sxs-lookup"><span data-stu-id="92b84-125">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="92b84-126">En la **clase CTransformInputPin,** el identificador de pin y el nombre del pin no son los mismos.</span><span class="sxs-lookup"><span data-stu-id="92b84-126">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b84-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92b84-127">Requirements</span></span>



| <span data-ttu-id="92b84-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b84-128">Requirement</span></span> | <span data-ttu-id="92b84-129">Value</span><span class="sxs-lookup"><span data-stu-id="92b84-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b84-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92b84-130">Header</span></span><br/>  | <dl> <span data-ttu-id="92b84-131"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="92b84-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="92b84-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92b84-132">Library</span></span><br/> | <dl> <span data-ttu-id="92b84-133"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="92b84-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




