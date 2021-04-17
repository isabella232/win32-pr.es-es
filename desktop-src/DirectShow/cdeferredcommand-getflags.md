---
description: El método GetFlags recupera las marcas de contexto asociadas al comando diferido.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: CDeferredCommand. GetFlags (método) (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681196"
---
# <a name="cdeferredcommandgetflags-method"></a><span data-ttu-id="c8771-103">CDeferredCommand. GetFlags (método)</span><span class="sxs-lookup"><span data-stu-id="c8771-103">CDeferredCommand.GetFlags method</span></span>

<span data-ttu-id="c8771-104">El `GetFlags` método recupera las marcas de contexto asociadas al comando diferido.</span><span class="sxs-lookup"><span data-stu-id="c8771-104">The `GetFlags` method retrieves the context flags associated with the deferred command.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8771-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8771-105">Syntax</span></span>


```C++
short GetFlags();
```



## <a name="parameters"></a><span data-ttu-id="c8771-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8771-106">Parameters</span></span>

<span data-ttu-id="c8771-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c8771-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8771-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8771-108">Return value</span></span>

<span data-ttu-id="c8771-109">Devuelve una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="c8771-109">Returns one of the following:</span></span>



| <span data-ttu-id="c8771-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c8771-110">Return code</span></span>                                                                                             | <span data-ttu-id="c8771-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8771-111">Description</span></span>                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8771-112"><dt>**DISPATCH ( \_ método)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8771-112"><dt>**DISPATCH\_METHOD**</dt></span></span> </dl>         | <span data-ttu-id="c8771-113">Ejecute el miembro como un método.</span><span class="sxs-lookup"><span data-stu-id="c8771-113">Run the member as a method.</span></span> <span data-ttu-id="c8771-114">Si una propiedad tiene el mismo nombre, se pueden establecer tanto esta marca como la de envío \_ PropertyGet (.</span><span class="sxs-lookup"><span data-stu-id="c8771-114">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span><br/>                                               |
| <dl> <span data-ttu-id="c8771-115"><dt>**ENVIAR \_ PropertyGet (**</dt></span><span class="sxs-lookup"><span data-stu-id="c8771-115"><dt>**DISPATCH\_PROPERTYGET**</dt></span></span> </dl>    | <span data-ttu-id="c8771-116">El miembro se recupera como una propiedad o miembro de datos.</span><span class="sxs-lookup"><span data-stu-id="c8771-116">The member is being retrieved as a property or data member.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="c8771-117"><dt>**ENVIAR \_ PROPERTYPUT**</dt></span><span class="sxs-lookup"><span data-stu-id="c8771-117"><dt>**DISPATCH\_PROPERTYPUT**</dt></span></span> </dl>    | <span data-ttu-id="c8771-118">El miembro se está cambiando como una propiedad o un miembro de datos.</span><span class="sxs-lookup"><span data-stu-id="c8771-118">The member is being changed as a property or data member.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="c8771-119"><dt>**ENVIAR \_ PROPERTYPUTREF**</dt></span><span class="sxs-lookup"><span data-stu-id="c8771-119"><dt>**DISPATCH\_PROPERTYPUTREF**</dt></span></span> </dl> | <span data-ttu-id="c8771-120">El miembro se está cambiando a través de una asignación de referencia, en lugar de una asignación de valores.</span><span class="sxs-lookup"><span data-stu-id="c8771-120">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="c8771-121">Esta marca solo es válida cuando la propiedad acepta una referencia a un objeto.</span><span class="sxs-lookup"><span data-stu-id="c8771-121">This flag is valid only when the property accepts a reference to an object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c8771-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8771-122">Requirements</span></span>



| <span data-ttu-id="c8771-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8771-123">Requirement</span></span> | <span data-ttu-id="c8771-124">Value</span><span class="sxs-lookup"><span data-stu-id="c8771-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8771-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8771-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c8771-126"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8771-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8771-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8771-127">Library</span></span><br/> | <dl> <span data-ttu-id="c8771-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c8771-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8771-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8771-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8771-130">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="c8771-130">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




