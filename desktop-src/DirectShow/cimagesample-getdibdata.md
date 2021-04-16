---
description: El método GetDIBData recupera información sobre el mapa de bits independiente del dispositivo GDI (DIB) que este objeto administra.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Método CImageSample. GetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679033"
---
# <a name="cimagesamplegetdibdata-method"></a><span data-ttu-id="9bacb-103">CImageSample. GetDIBData, método</span><span class="sxs-lookup"><span data-stu-id="9bacb-103">CImageSample.GetDIBData method</span></span>

<span data-ttu-id="9bacb-104">El `GetDIBData` método recupera información sobre el mapa de bits independiente del dispositivo GDI (DIB) que este objeto administra.</span><span class="sxs-lookup"><span data-stu-id="9bacb-104">The `GetDIBData` method retrieves information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bacb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bacb-105">Syntax</span></span>


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a><span data-ttu-id="9bacb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9bacb-106">Parameters</span></span>

<span data-ttu-id="9bacb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9bacb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9bacb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bacb-108">Return value</span></span>

<span data-ttu-id="9bacb-109">Devuelve un puntero a una estructura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9bacb-109">Returns a pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bacb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bacb-110">Remarks</span></span>

<span data-ttu-id="9bacb-111">El autor de la llamada debe inicializar la estructura **DIBDATA** antes de llamar a este método; Compruebe el valor de **CImageSample:: m \_ bInit**.</span><span class="sxs-lookup"><span data-stu-id="9bacb-111">The caller must initialize the **DIBDATA** structure before calling this method; check the value of **CImageSample::m\_bInit**.</span></span> <span data-ttu-id="9bacb-112">Para inicializar la estructura, llame al método [**CImageSample:: SetDIBData**](cimagesample-setdibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9bacb-112">To initialize the structure, call the [**CImageSample::SetDIBData**](cimagesample-setdibdata.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bacb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bacb-113">Requirements</span></span>



| <span data-ttu-id="9bacb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bacb-114">Requirement</span></span> | <span data-ttu-id="9bacb-115">Value</span><span class="sxs-lookup"><span data-stu-id="9bacb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bacb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9bacb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9bacb-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bacb-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9bacb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9bacb-118">Library</span></span><br/> | <dl> <span data-ttu-id="9bacb-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9bacb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bacb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bacb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bacb-121">**Clase CImageSample**</span><span class="sxs-lookup"><span data-stu-id="9bacb-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




