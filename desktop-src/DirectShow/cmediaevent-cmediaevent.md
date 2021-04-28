---
description: 'Constructor CMediaEvent.CMediaEvent: método constructor.'
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Constructor CMediaEvent.CMediaEvent (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095563"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="e237f-103">Constructor CMediaEvent.CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="e237f-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="e237f-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="e237f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e237f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e237f-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="e237f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e237f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e237f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e237f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e237f-108">Puntero al nombre del objeto con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="e237f-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="e237f-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="e237f-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e237f-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="e237f-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e237f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e237f-111">Remarks</span></span>

<span data-ttu-id="e237f-112">Asigne el *parámetro pName* en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="e237f-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="e237f-113">Este nombre aparece en el terminal de depuración tras la creación y eliminación del objeto.</span><span class="sxs-lookup"><span data-stu-id="e237f-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e237f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e237f-114">Requirements</span></span>



| <span data-ttu-id="e237f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e237f-115">Requirement</span></span> | <span data-ttu-id="e237f-116">Value</span><span class="sxs-lookup"><span data-stu-id="e237f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e237f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e237f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e237f-118"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e237f-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e237f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e237f-119">Library</span></span><br/> | <dl> <span data-ttu-id="e237f-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e237f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e237f-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e237f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e237f-122">**CMediaEvent (clase)**</span><span class="sxs-lookup"><span data-stu-id="e237f-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




