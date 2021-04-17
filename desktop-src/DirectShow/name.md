---
description: La macro NAME genera una cadena de solo depuración.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NOMBRE (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690410"
---
# <a name="name"></a><span data-ttu-id="d838d-103">NAME</span><span class="sxs-lookup"><span data-stu-id="d838d-103">NAME</span></span>

<span data-ttu-id="d838d-104">La macro **Name** genera una cadena de solo depuración.</span><span class="sxs-lookup"><span data-stu-id="d838d-104">The **NAME** macro generates a debug-only string.</span></span>

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="d838d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d838d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d838d-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="d838d-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="d838d-107">Cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d838d-107">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d838d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d838d-108">Remarks</span></span>

<span data-ttu-id="d838d-109">En las compilaciones de depuración, esta macro es equivalente a la macro **Text** .</span><span class="sxs-lookup"><span data-stu-id="d838d-109">In debug builds, this macro is equivalent to the **TEXT** macro.</span></span> <span data-ttu-id="d838d-110">En las compilaciones comerciales, se resuelve como (TCHAR \* ) **null**.</span><span class="sxs-lookup"><span data-stu-id="d838d-110">In retail builds, it resolves to (TCHAR\*) **NULL**.</span></span> <span data-ttu-id="d838d-111">Esta macro es útil al declarar el nombre de un objeto que deriva de la clase [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="d838d-111">This macro is useful when declaring the name of an object that derives from the [**CBaseObject**](cbaseobject.md) class.</span></span>


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a><span data-ttu-id="d838d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d838d-112">Requirements</span></span>



| <span data-ttu-id="d838d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d838d-113">Requirement</span></span> | <span data-ttu-id="d838d-114">Value</span><span class="sxs-lookup"><span data-stu-id="d838d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d838d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d838d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d838d-116"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d838d-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d838d-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d838d-117">Library</span></span><br/> | <dl> <span data-ttu-id="d838d-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d838d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d838d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d838d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d838d-120">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="d838d-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




