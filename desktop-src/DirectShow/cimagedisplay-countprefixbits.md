---
description: El método CountPrefixBits calcula el número de bits cero al principio de un campo de bits especificado.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Método CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660935"
---
# <a name="cimagedisplaycountprefixbits-method"></a><span data-ttu-id="4b285-103">CImageDisplay. CountPrefixBits, método</span><span class="sxs-lookup"><span data-stu-id="4b285-103">CImageDisplay.CountPrefixBits method</span></span>

<span data-ttu-id="4b285-104">El `CountPrefixBits` método calcula el número de bits cero al principio de un campo de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="4b285-104">The `CountPrefixBits` method calculates the number of zero bits at the start of a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b285-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b285-105">Syntax</span></span>


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="4b285-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b285-107">*Campo*</span><span class="sxs-lookup"><span data-stu-id="4b285-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="4b285-108">Especifica un campo de bits como un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="4b285-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b285-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b285-109">Return value</span></span>

<span data-ttu-id="4b285-110">Devuelve el número de bits cero que se producen antes del primer bit 1 o 0x80000000 si todos los bits son cero.</span><span class="sxs-lookup"><span data-stu-id="4b285-110">Returns the number of zero bits that occur before the first 1 bit, or 0x80000000 if all bits are zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b285-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b285-111">Remarks</span></span>

<span data-ttu-id="4b285-112">Este método es útil para trabajar con máscaras de colores en estructuras de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="4b285-112">This method is useful for working with color masks in [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b285-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b285-113">Requirements</span></span>



| <span data-ttu-id="4b285-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b285-114">Requirement</span></span> | <span data-ttu-id="4b285-115">Value</span><span class="sxs-lookup"><span data-stu-id="4b285-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b285-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b285-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4b285-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b285-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4b285-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b285-118">Library</span></span><br/> | <dl> <span data-ttu-id="4b285-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4b285-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b285-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b285-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b285-121">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="4b285-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




