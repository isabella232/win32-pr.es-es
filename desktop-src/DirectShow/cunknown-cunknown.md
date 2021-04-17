---
description: Método de constructor.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Constructor CUnknown. CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660355"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="3260c-103">Constructor CUnknown. CUnknown</span><span class="sxs-lookup"><span data-stu-id="3260c-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="3260c-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="3260c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3260c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3260c-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="3260c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3260c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3260c-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3260c-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3260c-108">Cadena que contiene el nombre del objeto; se usa en el constructor [**CBaseObject**](cbaseobject.md) para la depuración.</span><span class="sxs-lookup"><span data-stu-id="3260c-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="3260c-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="3260c-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3260c-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="3260c-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="3260c-111">Si se agrega el objeto, pase un puntero a la interfaz IUnknown del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="3260c-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="3260c-112">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="3260c-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3260c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3260c-113">Remarks</span></span>

<span data-ttu-id="3260c-114">El objeto se inicializa con un recuento de referencias de cero.</span><span class="sxs-lookup"><span data-stu-id="3260c-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3260c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3260c-115">Requirements</span></span>



| <span data-ttu-id="3260c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3260c-116">Requirement</span></span> | <span data-ttu-id="3260c-117">Value</span><span class="sxs-lookup"><span data-stu-id="3260c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3260c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3260c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3260c-119"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3260c-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3260c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3260c-120">Library</span></span><br/> | <dl> <span data-ttu-id="3260c-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3260c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




