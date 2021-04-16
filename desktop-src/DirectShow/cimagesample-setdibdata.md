---
description: El método SetDIBData especifica información sobre el mapa de bits independiente del dispositivo GDI (DIB) que este objeto administra. Llame a este método para inicializar el objeto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Método CImageSample. SetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670487"
---
# <a name="cimagesamplesetdibdata-method"></a><span data-ttu-id="3b966-104">CImageSample. SetDIBData, método</span><span class="sxs-lookup"><span data-stu-id="3b966-104">CImageSample.SetDIBData method</span></span>

<span data-ttu-id="3b966-105">El `SetDIBData` método especifica información sobre el mapa de bits independiente del dispositivo GDI (DIB) que este objeto administra.</span><span class="sxs-lookup"><span data-stu-id="3b966-105">The `SetDIBData` method specifies information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span> <span data-ttu-id="3b966-106">Llame a este método para inicializar el objeto **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="3b966-106">Call this method to initialize the **CImageSample** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b966-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b966-107">Syntax</span></span>


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a><span data-ttu-id="3b966-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b966-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b966-109">*pDibData*</span><span class="sxs-lookup"><span data-stu-id="3b966-109">*pDibData*</span></span> 
</dt> <dd>

<span data-ttu-id="3b966-110">Puntero a una estructura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3b966-110">Pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b966-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b966-111">Return value</span></span>

<span data-ttu-id="3b966-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3b966-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b966-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b966-113">Requirements</span></span>



| <span data-ttu-id="3b966-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b966-114">Requirement</span></span> | <span data-ttu-id="3b966-115">Value</span><span class="sxs-lookup"><span data-stu-id="3b966-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b966-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b966-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3b966-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b966-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b966-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b966-118">Library</span></span><br/> | <dl> <span data-ttu-id="3b966-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3b966-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b966-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b966-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b966-121">**Clase CImageSample**</span><span class="sxs-lookup"><span data-stu-id="3b966-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




