---
description: 'El método GetPointer recupera un puntero de lectura/escritura al búfer. Este método implementa el método IMediaSample:: GetPointer.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Método CMediaSample. GetPointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679332"
---
# <a name="cmediasamplegetpointer-method"></a><span data-ttu-id="636b2-104">CMediaSample. GetPointer, método</span><span class="sxs-lookup"><span data-stu-id="636b2-104">CMediaSample.GetPointer method</span></span>

<span data-ttu-id="636b2-105">El `GetPointer` método recupera un puntero de lectura/escritura en el búfer.</span><span class="sxs-lookup"><span data-stu-id="636b2-105">The `GetPointer` method retrieves a read/write pointer to the buffer.</span></span> <span data-ttu-id="636b2-106">Este método implementa el método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) .</span><span class="sxs-lookup"><span data-stu-id="636b2-106">This method implements the [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="636b2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="636b2-107">Syntax</span></span>


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="636b2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="636b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="636b2-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="636b2-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="636b2-110">Dirección de una variable que recibe un puntero al búfer.</span><span class="sxs-lookup"><span data-stu-id="636b2-110">Address of a variable that receives a pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="636b2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="636b2-111">Return value</span></span>

<span data-ttu-id="636b2-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="636b2-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="636b2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="636b2-113">Requirements</span></span>



| <span data-ttu-id="636b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="636b2-114">Requirement</span></span> | <span data-ttu-id="636b2-115">Value</span><span class="sxs-lookup"><span data-stu-id="636b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="636b2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="636b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="636b2-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="636b2-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="636b2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="636b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="636b2-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="636b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="636b2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="636b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636b2-121">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="636b2-121">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




