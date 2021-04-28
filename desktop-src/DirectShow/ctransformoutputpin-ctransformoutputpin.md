---
description: 'Constructor CTransformOutputPin.CTransformOutputPin: método constructor.'
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Constructor CTransformOutputPin.CTransformOutputPin (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1f7cb9dd811c878eba258a6087e00a85d4c24a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084873"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a><span data-ttu-id="0b6c1-103">Constructor CTransformOutputPin.CTransformOutputPin</span><span class="sxs-lookup"><span data-stu-id="0b6c1-103">CTransformOutputPin.CTransformOutputPin constructor</span></span>

<span data-ttu-id="0b6c1-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="0b6c1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b6c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b6c1-105">Syntax</span></span>


```C++
CTransformOutputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="0b6c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b6c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b6c1-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="0b6c1-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="0b6c1-108">Cadena que contiene el nombre de depuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="0b6c1-108">String containing the debug name of the object.</span></span> <span data-ttu-id="0b6c1-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0b6c1-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c1-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="0b6c1-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0b6c1-111">Puntero al filtro que creó este pin, que debe ser un [**objeto CTransformFilter.**](ctransformfilter.md)</span><span class="sxs-lookup"><span data-stu-id="0b6c1-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0b6c1-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="0b6c1-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0b6c1-113">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.</span><span class="sxs-lookup"><span data-stu-id="0b6c1-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="0b6c1-114">Inicialice el valor en S \_ OK antes de crear el objeto .</span><span class="sxs-lookup"><span data-stu-id="0b6c1-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="0b6c1-115">El valor solo se cambia si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="0b6c1-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="0b6c1-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="0b6c1-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0b6c1-117">Cadena de caracteres anchos que contiene el nombre del pin.</span><span class="sxs-lookup"><span data-stu-id="0b6c1-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b6c1-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b6c1-118">Remarks</span></span>

<span data-ttu-id="0b6c1-119">El *parámetro pName* especifica el nombre del pin, que devuelve el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="0b6c1-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="0b6c1-120">Sin embargo, la cadena no se usa para el identificador de pin.</span><span class="sxs-lookup"><span data-stu-id="0b6c1-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="0b6c1-121">El identificador de pin de esta clase siempre es "Out".</span><span class="sxs-lookup"><span data-stu-id="0b6c1-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="0b6c1-122">Para obtener más información, vea [**QueryId**](ctransformoutputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="0b6c1-122">For more information, see [**QueryId**](ctransformoutputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6c1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6c1-123">Requirements</span></span>



| <span data-ttu-id="0b6c1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6c1-124">Requirement</span></span> | <span data-ttu-id="0b6c1-125">Value</span><span class="sxs-lookup"><span data-stu-id="0b6c1-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6c1-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b6c1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0b6c1-127"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c1-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0b6c1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b6c1-128">Library</span></span><br/> | <dl> <span data-ttu-id="0b6c1-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c1-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




