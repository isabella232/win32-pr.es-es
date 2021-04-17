---
description: Método de constructor.
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Constructor CMediaControl. CMediaControl (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63b965ff2484d4db7f7de41d8d524bc74c31ac73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680243"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a><span data-ttu-id="6296c-103">Constructor CMediaControl. CMediaControl</span><span class="sxs-lookup"><span data-stu-id="6296c-103">CMediaControl.CMediaControl constructor</span></span>

<span data-ttu-id="6296c-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="6296c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6296c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6296c-105">Syntax</span></span>


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="6296c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6296c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6296c-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6296c-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6296c-108">Puntero al nombre del objeto para la depuración.</span><span class="sxs-lookup"><span data-stu-id="6296c-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="6296c-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="6296c-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6296c-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="6296c-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6296c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6296c-111">Remarks</span></span>

<span data-ttu-id="6296c-112">Asigne el parámetro *pName* en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="6296c-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="6296c-113">Este nombre aparece en el terminal de depuración al crear y eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="6296c-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6296c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6296c-114">Requirements</span></span>



| <span data-ttu-id="6296c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6296c-115">Requirement</span></span> | <span data-ttu-id="6296c-116">Value</span><span class="sxs-lookup"><span data-stu-id="6296c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6296c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6296c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6296c-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6296c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6296c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6296c-119">Library</span></span><br/> | <dl> <span data-ttu-id="6296c-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6296c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6296c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="6296c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6296c-122">**Clase CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="6296c-122">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




