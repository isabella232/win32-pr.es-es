---
description: Este operador sobrecarga el operador de asignación para copiar un tipo de medio.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'CMediaType. CMediaType:: Operator = método (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 748ad2efae39fc6a7b26c39d10351c44a5cee8a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690866"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="37584-103">CMediaType. CMediaType:: Operator = método (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="37584-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="37584-104">Este operador sobrecarga el operador de asignación para copiar un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="37584-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="37584-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37584-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="37584-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37584-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37584-107">*mtype* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="37584-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="37584-108">Referencia a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="37584-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37584-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37584-109">Return value</span></span>

<span data-ttu-id="37584-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="37584-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="37584-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37584-111">Requirements</span></span>



| <span data-ttu-id="37584-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="37584-112">Requirement</span></span> | <span data-ttu-id="37584-113">Value</span><span class="sxs-lookup"><span data-stu-id="37584-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37584-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37584-114">Header</span></span><br/>  | <dl> <span data-ttu-id="37584-115"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37584-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="37584-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37584-116">Library</span></span><br/> | <dl> <span data-ttu-id="37584-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="37584-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37584-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="37584-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37584-119">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="37584-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




