---
description: El método UpdateFormat rellena algunos miembros opcionales de la estructura de videoinfo.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: Método CImageDisplay. UpdateFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660625"
---
# <a name="cimagedisplayupdateformat-method"></a><span data-ttu-id="55174-103">CImageDisplay. UpdateFormat, método</span><span class="sxs-lookup"><span data-stu-id="55174-103">CImageDisplay.UpdateFormat method</span></span>

<span data-ttu-id="55174-104">El `UpdateFormat` método rellena algunos miembros opcionales de la estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="55174-104">The `UpdateFormat` method fills in some optional members of the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="55174-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55174-105">Syntax</span></span>


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="55174-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55174-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55174-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="55174-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="55174-108">Puntero a una estructura de **videoinfo** .</span><span class="sxs-lookup"><span data-stu-id="55174-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55174-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55174-109">Return value</span></span>

<span data-ttu-id="55174-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="55174-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="55174-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55174-111">Remarks</span></span>

<span data-ttu-id="55174-112">Este método establece los miembros **biClrUsed**, **biClrImportant** y **biSizeImage** en los valores correctos y borra los rectángulos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="55174-112">This method sets the **biClrUsed**, **biClrImportant**, and **biSizeImage** members to the correct values, and clears the source and target rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="55174-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55174-113">Requirements</span></span>



| <span data-ttu-id="55174-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="55174-114">Requirement</span></span> | <span data-ttu-id="55174-115">Value</span><span class="sxs-lookup"><span data-stu-id="55174-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55174-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55174-116">Header</span></span><br/>  | <dl> <span data-ttu-id="55174-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55174-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55174-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55174-118">Library</span></span><br/> | <dl> <span data-ttu-id="55174-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="55174-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55174-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="55174-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55174-121">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="55174-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




