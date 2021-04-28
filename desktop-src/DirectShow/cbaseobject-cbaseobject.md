---
description: 'Constructor CBaseObject.CBaseObject: método constructor.'
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Constructor CBaseObject.CBaseObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099623"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="3ad3c-103">Constructor CBaseObject.CBaseObject</span><span class="sxs-lookup"><span data-stu-id="3ad3c-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="3ad3c-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad3c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ad3c-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="3ad3c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ad3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad3c-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3ad3c-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3ad3c-108">Cadena que contiene el nombre del objeto, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ad3c-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ad3c-109">Remarks</span></span>

<span data-ttu-id="3ad3c-110">Este método incrementa el recuento de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-110">This method increments the active-object count.</span></span> <span data-ttu-id="3ad3c-111">(Vea [**CBaseObject::ObjectsActive).**](cbaseobject-objectsactive.md)</span><span class="sxs-lookup"><span data-stu-id="3ad3c-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="3ad3c-112">Asigne el *parámetro pName* en la memoria estática:</span><span class="sxs-lookup"><span data-stu-id="3ad3c-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="3ad3c-113">La [**macro NAME**](name.md) se compila en NULL **en** las compilaciones comerciales, de modo que las cadenas estáticas solo aparecen en las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="3ad3c-114">Para obtener más información, [**vea DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="3ad3c-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad3c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ad3c-115">Requirements</span></span>



| <span data-ttu-id="3ad3c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ad3c-116">Requirement</span></span> | <span data-ttu-id="3ad3c-117">Value</span><span class="sxs-lookup"><span data-stu-id="3ad3c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad3c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ad3c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3ad3c-119"><dt>Combase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ad3c-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3ad3c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ad3c-120">Library</span></span><br/> | <dl> <span data-ttu-id="3ad3c-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3ad3c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ad3c-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3ad3c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad3c-123">**CBaseObject (clase)**</span><span class="sxs-lookup"><span data-stu-id="3ad3c-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




