---
description: 'Constructor CUnknown.CUnknown: método constructor.'
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Constructor CUnknown.CUnknown (Combase.h)
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
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084613"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="e8456-103">Constructor CUnknown.CUnknown</span><span class="sxs-lookup"><span data-stu-id="e8456-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="e8456-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="e8456-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8456-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8456-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="e8456-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8456-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8456-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e8456-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e8456-108">Cadena que contiene el nombre del objeto; se usa en el constructor [**CBaseObject**](cbaseobject.md) para la depuración.</span><span class="sxs-lookup"><span data-stu-id="e8456-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="e8456-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="e8456-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e8456-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="e8456-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="e8456-111">Si el objeto se agrega, pase un puntero a la interfaz IUnknown del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="e8456-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="e8456-112">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e8456-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8456-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8456-113">Remarks</span></span>

<span data-ttu-id="e8456-114">El objeto se inicializa con un recuento de referencias de cero.</span><span class="sxs-lookup"><span data-stu-id="e8456-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8456-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8456-115">Requirements</span></span>



| <span data-ttu-id="e8456-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8456-116">Requirement</span></span> | <span data-ttu-id="e8456-117">Value</span><span class="sxs-lookup"><span data-stu-id="e8456-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8456-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8456-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e8456-119"><dt>Combase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8456-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e8456-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8456-120">Library</span></span><br/> | <dl> <span data-ttu-id="e8456-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e8456-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




