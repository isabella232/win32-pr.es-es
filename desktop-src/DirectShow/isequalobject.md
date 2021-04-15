---
description: La función IsEqualObject comprueba si dos interfaces están en el mismo objeto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Función IsEqualObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690179"
---
# <a name="isequalobject-function"></a><span data-ttu-id="a8b6c-103">IsEqualObject función)</span><span class="sxs-lookup"><span data-stu-id="a8b6c-103">IsEqualObject function</span></span>

<span data-ttu-id="a8b6c-104">La `IsEqualObject` función comprueba si dos interfaces están en el mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="a8b6c-104">The `IsEqualObject` function checks if two interfaces are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b6c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8b6c-105">Syntax</span></span>


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a><span data-ttu-id="a8b6c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8b6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b6c-107">*pFirst*</span><span class="sxs-lookup"><span data-stu-id="a8b6c-107">*pFirst*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b6c-108">Puntero a una interfaz.</span><span class="sxs-lookup"><span data-stu-id="a8b6c-108">Pointer to one interface.</span></span>

</dd> <dt>

<span data-ttu-id="a8b6c-109">*pSecond*</span><span class="sxs-lookup"><span data-stu-id="a8b6c-109">*pSecond*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b6c-110">Puntero a la otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="a8b6c-110">Pointer to the other interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b6c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8b6c-111">Return value</span></span>

<span data-ttu-id="a8b6c-112">Devuelve **true** si las interfaces están ambas en el mismo objeto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a8b6c-112">Returns **TRUE** if the interfaces are both on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b6c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8b6c-113">Requirements</span></span>



| <span data-ttu-id="a8b6c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b6c-114">Requirement</span></span> | <span data-ttu-id="a8b6c-115">Value</span><span class="sxs-lookup"><span data-stu-id="a8b6c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b6c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8b6c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a8b6c-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8b6c-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a8b6c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8b6c-118">Library</span></span><br/> | <dl> <span data-ttu-id="a8b6c-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a8b6c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b6c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8b6c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b6c-121">Funciones auxiliares misceláneas</span><span class="sxs-lookup"><span data-stu-id="a8b6c-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




