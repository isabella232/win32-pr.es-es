---
description: 'Constructor CTransInPlaceInputPin.CTransInPlaceInputPin: método constructor.'
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Constructor CTransInPlaceInputPin.CTransInPlaceInputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f97c89142e43691c91b2a4c0d04721d9112ed49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084763"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="17888-103">Constructor CTransInPlaceInputPin.CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="17888-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="17888-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="17888-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17888-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17888-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="17888-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17888-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="17888-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="17888-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="17888-108">String containing the debug name of the object.</span></span> <span data-ttu-id="17888-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="17888-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="17888-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="17888-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="17888-111">Puntero al filtro que creó este pin, que debe ser [**un objeto CTransInPlaceFilter.**](ctransinplacefilter.md)</span><span class="sxs-lookup"><span data-stu-id="17888-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="17888-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="17888-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="17888-113">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.</span><span class="sxs-lookup"><span data-stu-id="17888-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="17888-114">Inicialice el valor en S \_ OK antes de crear el objeto .</span><span class="sxs-lookup"><span data-stu-id="17888-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="17888-115">El valor solo se cambia si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="17888-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="17888-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="17888-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="17888-117">Cadena de caracteres anchos que contiene el nombre del pin.</span><span class="sxs-lookup"><span data-stu-id="17888-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17888-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17888-118">Remarks</span></span>

<span data-ttu-id="17888-119">El *parámetro pName* especifica el nombre del pin, que devuelve el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="17888-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="17888-120">Sin embargo, esta cadena no se usa para el identificador de pin.</span><span class="sxs-lookup"><span data-stu-id="17888-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="17888-121">El identificador de pin de esta clase siempre es In.</span><span class="sxs-lookup"><span data-stu-id="17888-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="17888-122">Para obtener más información, [**vea CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="17888-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17888-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17888-123">Requirements</span></span>



| <span data-ttu-id="17888-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="17888-124">Requirement</span></span> | <span data-ttu-id="17888-125">Value</span><span class="sxs-lookup"><span data-stu-id="17888-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17888-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17888-126">Header</span></span><br/>  | <dl> <span data-ttu-id="17888-127"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="17888-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17888-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17888-128">Library</span></span><br/> | <dl> <span data-ttu-id="17888-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="17888-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17888-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="17888-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17888-131">**CTransInPlaceInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="17888-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




