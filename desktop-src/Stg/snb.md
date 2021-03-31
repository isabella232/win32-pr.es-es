---
title: SNB (Objidl. h)
description: Un bloque de nombre de cadena (SNB) es un puntero a una matriz de punteros a cadenas, que finaliza en un puntero nulo.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996164"
---
# <a name="snb"></a><span data-ttu-id="252f4-104">SNB</span><span class="sxs-lookup"><span data-stu-id="252f4-104">SNB</span></span>

<span data-ttu-id="252f4-105">Un bloque de nombre de cadena (**SNB**) es un puntero a una matriz de punteros a cadenas, que finaliza en un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="252f4-105">A string name block (**SNB**) is a pointer to an array of pointers to strings, that ends in a **NULL** pointer.</span></span> <span data-ttu-id="252f4-106">Los bloques de nombre de cadena se utilizan en la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y las llamadas a funciones que abren objetos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="252f4-106">String name blocks are used by the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and by function calls that open storage objects.</span></span> <span data-ttu-id="252f4-107">Las cadenas apuntan a objetos de almacenamiento contenidos o flujos que se van a excluir en las llamadas abiertas.</span><span class="sxs-lookup"><span data-stu-id="252f4-107">The strings point to contained storage objects or streams that are to be excluded in the open calls.</span></span>


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

<span data-ttu-id="252f4-108">**SNB**</span><span class="sxs-lookup"><span data-stu-id="252f4-108">**SNB**</span></span>
</dt> <dd>

<span data-ttu-id="252f4-109">\[\_serialización de cable (wireSNB)\]</span><span class="sxs-lookup"><span data-stu-id="252f4-109">\[wire\_marshal(wireSNB)\]</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="252f4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="252f4-110">Remarks</span></span>

<span data-ttu-id="252f4-111">El **SNB** debe crearse mediante la asignación de un bloque de memoria contiguo en el que los punteros a cadenas van seguidos de un puntero **nulo** , que a continuación va seguido de las cadenas reales.</span><span class="sxs-lookup"><span data-stu-id="252f4-111">The **SNB** should be created by allocating a contiguous block of memory in which the pointers to strings are followed by a **NULL** pointer, which is then followed by the actual strings.</span></span>

<span data-ttu-id="252f4-112">El cálculo de referencias de un **SNB** se basa en la suposición de que el **SNB** que se pasó se creó de este modo.</span><span class="sxs-lookup"><span data-stu-id="252f4-112">The marshaling of an **SNB** is based on the assumption that the **SNB** that was passed in was created in this way.</span></span> <span data-ttu-id="252f4-113">Aunque podría almacenarse de otras maneras, el **SNB** creado de esta manera tiene la ventaja de requerir solo una operación de asignación y una liberación de memoria para todas las cadenas.</span><span class="sxs-lookup"><span data-stu-id="252f4-113">Although it could be stored in other ways, the **SNB** created in this manner has the advantage of requiring only one allocation operation and one freeing of memory for all the strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="252f4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="252f4-114">Requirements</span></span>



| <span data-ttu-id="252f4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="252f4-115">Requirement</span></span> | <span data-ttu-id="252f4-116">Value</span><span class="sxs-lookup"><span data-stu-id="252f4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="252f4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="252f4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="252f4-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="252f4-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="252f4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="252f4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="252f4-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="252f4-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="252f4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="252f4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="252f4-122"><dt>Objidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="252f4-122"><dt>Objidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="252f4-123">IDL</span><span class="sxs-lookup"><span data-stu-id="252f4-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="252f4-124"><dt>Objidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="252f4-124"><dt>Objidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="252f4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="252f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="252f4-126">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="252f4-126">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





