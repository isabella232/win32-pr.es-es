---
description: La clase LockIt es una clase interna que bloquea y desbloquea DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Clase IMediaObjectImpl:: LockIt (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679272"
---
# <a name="imediaobjectimpllockit-class"></a><span data-ttu-id="e29c9-103">IMediaObjectImpl:: LockIt (clase)</span><span class="sxs-lookup"><span data-stu-id="e29c9-103">IMediaObjectImpl::LockIt Class</span></span>

<span data-ttu-id="e29c9-104">La `LockIt` clase es una clase interna que bloquea y desbloquea DMO.</span><span class="sxs-lookup"><span data-stu-id="e29c9-104">The `LockIt` class is an internal class that locks and unlocks the DMO.</span></span>

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a><span data-ttu-id="e29c9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e29c9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e29c9-106"><span id="p"></span><span id="P"></span>*m*</span><span class="sxs-lookup"><span data-stu-id="e29c9-106"><span id="p"></span><span id="P"></span>*p*</span></span>
</dt> <dd>

<span data-ttu-id="e29c9-107">Puntero al objeto derivado.</span><span class="sxs-lookup"><span data-stu-id="e29c9-107">Pointer to the derived object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e29c9-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e29c9-108">Remarks</span></span>

<span data-ttu-id="e29c9-109">El `LockIt` constructor bloquea DMO y el destructor desbloquea el DMO.</span><span class="sxs-lookup"><span data-stu-id="e29c9-109">The `LockIt` constructor locks the DMO, and the destructor unlocks the DMO.</span></span> <span data-ttu-id="e29c9-110">Para bloquear el objeto desde dentro de la clase derivada, declare una variable local de tipo `LockIt` .</span><span class="sxs-lookup"><span data-stu-id="e29c9-110">To lock the object from inside your derived class, declare a local variable of type `LockIt`.</span></span> <span data-ttu-id="e29c9-111">DMO está bloqueado mientras el `LockIt` objeto permanece en el ámbito:</span><span class="sxs-lookup"><span data-stu-id="e29c9-111">The DMO is locked while the `LockIt` object remains in scope:</span></span>


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



<span data-ttu-id="e29c9-112">Los métodos de **IMediaObjectImpl** bloquean automáticamente DMO.</span><span class="sxs-lookup"><span data-stu-id="e29c9-112">The methods in **IMediaObjectImpl** automatically lock the DMO.</span></span>

## <a name="requirements"></a><span data-ttu-id="e29c9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e29c9-113">Requirements</span></span>



| <span data-ttu-id="e29c9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e29c9-114">Requirement</span></span> | <span data-ttu-id="e29c9-115">Value</span><span class="sxs-lookup"><span data-stu-id="e29c9-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e29c9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e29c9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e29c9-117"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e29c9-117"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="e29c9-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e29c9-118">Library</span></span><br/> | <dl> <span data-ttu-id="e29c9-119"><dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e29c9-119"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e29c9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e29c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e29c9-121">**Plantilla de clase IMediaObjectImpl**</span><span class="sxs-lookup"><span data-stu-id="e29c9-121">**IMediaObjectImpl Class Template**</span></span>](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




