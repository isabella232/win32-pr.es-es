---
description: El método Addtail (anexa una lista al final de la lista.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: 'Método CGenericList. Addtail ((Wxlist. h): parámetro plist'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105660105"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a><span data-ttu-id="cb76c-103">Método CGenericList. Addtail ((Wxlist. h): parámetro plist</span><span class="sxs-lookup"><span data-stu-id="cb76c-103">CGenericList.AddTail method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="cb76c-104">El `AddTail` método anexa una lista al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="cb76c-104">The `AddTail` method appends a list to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb76c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb76c-105">Syntax</span></span>


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a><span data-ttu-id="cb76c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb76c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb76c-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="cb76c-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="cb76c-108">Puntero a la lista que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="cb76c-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb76c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb76c-109">Return value</span></span>

<span data-ttu-id="cb76c-110">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cb76c-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb76c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb76c-111">Requirements</span></span>

| <span data-ttu-id="cb76c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb76c-112">Requirement</span></span> | <span data-ttu-id="cb76c-113">Value</span><span class="sxs-lookup"><span data-stu-id="cb76c-113">Value</span></span> |
|-|-|
| <span data-ttu-id="cb76c-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb76c-114">Header</span></span> | <span data-ttu-id="cb76c-115">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="cb76c-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="cb76c-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb76c-116">Library</span></span>| <span data-ttu-id="cb76c-117">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="cb76c-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="cb76c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb76c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb76c-119">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="cb76c-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




