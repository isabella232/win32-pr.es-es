---
description: Método de constructor.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Constructor CBaseObject. CBaseObject (ComBase. h)
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
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670412"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="cdb20-103">Constructor CBaseObject. CBaseObject</span><span class="sxs-lookup"><span data-stu-id="cdb20-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="cdb20-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="cdb20-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb20-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdb20-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="cdb20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdb20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb20-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="cdb20-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cdb20-108">Cadena que contiene el nombre del objeto, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="cdb20-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdb20-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdb20-109">Remarks</span></span>

<span data-ttu-id="cdb20-110">Este método incrementa el recuento de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="cdb20-110">This method increments the active-object count.</span></span> <span data-ttu-id="cdb20-111">(Vea [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md)).</span><span class="sxs-lookup"><span data-stu-id="cdb20-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="cdb20-112">Asigne el parámetro *pName* en la memoria estática:</span><span class="sxs-lookup"><span data-stu-id="cdb20-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="cdb20-113">La macro [**Name**](name.md) se compila como **null** en las compilaciones comerciales, de modo que las cadenas estáticas solo aparecen en las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="cdb20-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="cdb20-114">Para obtener más información, vea [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="cdb20-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb20-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdb20-115">Requirements</span></span>



| <span data-ttu-id="cdb20-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdb20-116">Requirement</span></span> | <span data-ttu-id="cdb20-117">Value</span><span class="sxs-lookup"><span data-stu-id="cdb20-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb20-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdb20-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cdb20-119"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdb20-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cdb20-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdb20-120">Library</span></span><br/> | <dl> <span data-ttu-id="cdb20-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cdb20-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdb20-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdb20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb20-123">**Clase CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="cdb20-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




