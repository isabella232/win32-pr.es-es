---
description: Método de constructor.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Constructor CBaseStreamControl. CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d325a48476fe2a80b7424850eb71a9d667cb60e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670689"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a><span data-ttu-id="e7060-103">Constructor CBaseStreamControl. CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="e7060-103">CBaseStreamControl.CBaseStreamControl constructor</span></span>

<span data-ttu-id="e7060-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="e7060-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7060-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7060-105">Syntax</span></span>


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="e7060-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7060-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7060-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="e7060-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e7060-108">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7060-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="e7060-109">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="e7060-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="e7060-110">Si esto ocurre, el objeto no tiene un estado válido.</span><span class="sxs-lookup"><span data-stu-id="e7060-110">If this occurs, the object is not in a valid state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7060-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7060-111">Requirements</span></span>



| <span data-ttu-id="e7060-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7060-112">Requirement</span></span> | <span data-ttu-id="e7060-113">Value</span><span class="sxs-lookup"><span data-stu-id="e7060-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7060-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7060-114">Header</span></span><br/>  | <dl> <span data-ttu-id="e7060-115"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7060-115"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7060-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7060-116">Library</span></span><br/> | <dl> <span data-ttu-id="e7060-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e7060-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7060-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7060-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7060-119">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="e7060-119">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




