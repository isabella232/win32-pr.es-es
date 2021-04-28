---
description: 'Constructor CSeekingPassThru.CSeekingPassThru: método constructor.'
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Constructor CSeekingPassThru.CSeekingPassThru (Seekpt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085383"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="c7630-103">Constructor CSeekingPassThru.CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="c7630-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="c7630-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="c7630-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7630-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7630-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="c7630-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7630-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="c7630-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c7630-108">Cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="c7630-108">String containing the name of the object.</span></span> <span data-ttu-id="c7630-109">Vea [**CBaseObject para**](cbaseobject.md) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c7630-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c7630-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="c7630-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c7630-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="c7630-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="c7630-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="c7630-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="c7630-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="c7630-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c7630-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="c7630-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c7630-115">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c7630-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="c7630-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c7630-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7630-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7630-117">Requirements</span></span>



| <span data-ttu-id="c7630-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7630-118">Requirement</span></span> | <span data-ttu-id="c7630-119">Value</span><span class="sxs-lookup"><span data-stu-id="c7630-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7630-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7630-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c7630-121"><dt>Seekpt.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7630-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c7630-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7630-122">Library</span></span><br/> | <dl> <span data-ttu-id="c7630-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c7630-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7630-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c7630-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7630-125">**CSeekingPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="c7630-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




