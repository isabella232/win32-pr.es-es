---
description: 'Constructor CTransInPlaceOutputPin.CTransInPlaceOutputPin: método constructor.'
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: Constructor CTransInPlaceOutputPin.CTransInPlaceOutputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b63ee3aa52bc0363bcab90275be4148659b3bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094713"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a><span data-ttu-id="1c048-103">Constructor CTransInPlaceOutputPin.CTransInPlaceOutputPin</span><span class="sxs-lookup"><span data-stu-id="1c048-103">CTransInPlaceOutputPin.CTransInPlaceOutputPin constructor</span></span>

<span data-ttu-id="1c048-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="1c048-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c048-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c048-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="1c048-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c048-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c048-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="1c048-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="1c048-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="1c048-108">String containing the debug name of the object.</span></span> <span data-ttu-id="1c048-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="1c048-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c048-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="1c048-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="1c048-111">Puntero al filtro que creó este pin, que debe ser [**un objeto CTransInPlaceFilter.**](ctransinplacefilter.md)</span><span class="sxs-lookup"><span data-stu-id="1c048-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1c048-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="1c048-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1c048-113">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o el error del método.</span><span class="sxs-lookup"><span data-stu-id="1c048-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="1c048-114">Inicialice el valor en S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="1c048-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="1c048-115">El valor solo se cambia si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="1c048-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="1c048-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="1c048-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1c048-117">Cadena de caracteres anchos que contiene el nombre del pin.</span><span class="sxs-lookup"><span data-stu-id="1c048-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c048-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c048-118">Remarks</span></span>

<span data-ttu-id="1c048-119">El *parámetro pName* especifica el nombre del pin, que devuelve el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="1c048-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="1c048-120">Sin embargo, la cadena no se usa para el identificador de pin.</span><span class="sxs-lookup"><span data-stu-id="1c048-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="1c048-121">El identificador de pin de esta clase siempre es "Out".</span><span class="sxs-lookup"><span data-stu-id="1c048-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="1c048-122">Para obtener más información, vea [**QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="1c048-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c048-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c048-123">Requirements</span></span>



| <span data-ttu-id="1c048-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c048-124">Requirement</span></span> | <span data-ttu-id="1c048-125">Value</span><span class="sxs-lookup"><span data-stu-id="1c048-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c048-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c048-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1c048-127"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c048-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c048-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c048-128">Library</span></span><br/> | <dl> <span data-ttu-id="1c048-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1c048-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c048-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c048-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c048-131">**CTransInPlaceOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="1c048-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




