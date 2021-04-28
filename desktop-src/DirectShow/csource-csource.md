---
description: 'Constructor CSource.CSource: método constructor.'
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: Constructor CSource.CSource (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fab398f3f4e3fdd8c23ce1e1c08f5c130478dfb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085363"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="3f692-103">Constructor CSource.CSource</span><span class="sxs-lookup"><span data-stu-id="3f692-103">CSource.CSource constructor</span></span>

<span data-ttu-id="3f692-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="3f692-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f692-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f692-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="3f692-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f692-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f692-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3f692-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3f692-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="3f692-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="3f692-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3f692-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f692-110">*l steam*</span><span class="sxs-lookup"><span data-stu-id="3f692-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="3f692-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="3f692-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="3f692-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="3f692-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="3f692-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="3f692-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3f692-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="3f692-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="3f692-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="3f692-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f692-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f692-116">Requirements</span></span>



| <span data-ttu-id="3f692-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f692-117">Requirement</span></span> | <span data-ttu-id="3f692-118">Value</span><span class="sxs-lookup"><span data-stu-id="3f692-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f692-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f692-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3f692-120"><dt>Source.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f692-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3f692-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f692-121">Library</span></span><br/> | <dl> <span data-ttu-id="3f692-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3f692-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f692-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3f692-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f692-124">**CSource (clase)**</span><span class="sxs-lookup"><span data-stu-id="3f692-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




