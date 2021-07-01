---
title: Punteros (RPC)
description: Obtenga información sobre un puntero común RPC, que se define como todo lo que no sea punteros de interfaz y punteros de recuento de bytes.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119710"
---
# <a name="pointers-rpc"></a><span data-ttu-id="8b39f-103">Punteros (RPC)</span><span class="sxs-lookup"><span data-stu-id="8b39f-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="8b39f-104">Punteros comunes</span><span class="sxs-lookup"><span data-stu-id="8b39f-104">Common Pointers</span></span>

<span data-ttu-id="8b39f-105">Un puntero común se define como todo lo que no sea punteros de interfaz y punteros de recuento de bytes.</span><span class="sxs-lookup"><span data-stu-id="8b39f-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="8b39f-106">Hay dos diseños posibles para la descripción:</span><span class="sxs-lookup"><span data-stu-id="8b39f-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="8b39f-107">-o bien-</span><span class="sxs-lookup"><span data-stu-id="8b39f-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="8b39f-108">El primer formato se usa si el puntero es un puntero a un tipo simple o a un puntero de cadena no especificado.</span><span class="sxs-lookup"><span data-stu-id="8b39f-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="8b39f-109">El segundo formato se usa para punteros a todos los demás tipos.</span><span class="sxs-lookup"><span data-stu-id="8b39f-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="8b39f-110">Los atributos de puntero indican qué diseño de descripción es con la marca \_ FC SIMPLE \_ POINTER.</span><span class="sxs-lookup"><span data-stu-id="8b39f-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="8b39f-111">el \_ tipo de<1> es uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b39f-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="8b39f-112">Carácter de formato</span><span class="sxs-lookup"><span data-stu-id="8b39f-112">Format character</span></span> | <span data-ttu-id="8b39f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b39f-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="8b39f-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="8b39f-114">FC\_RP</span></span>           | <span data-ttu-id="8b39f-115">Puntero de referencia.</span><span class="sxs-lookup"><span data-stu-id="8b39f-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="8b39f-116">FC \_ UP</span><span class="sxs-lookup"><span data-stu-id="8b39f-116">FC\_UP</span></span>           | <span data-ttu-id="8b39f-117">Puntero único.</span><span class="sxs-lookup"><span data-stu-id="8b39f-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="8b39f-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="8b39f-118">FC\_FP</span></span>           | <span data-ttu-id="8b39f-119">Puntero completo.</span><span class="sxs-lookup"><span data-stu-id="8b39f-119">A full pointer.</span></span>                          |
| <span data-ttu-id="8b39f-120">FC \_ OP</span><span class="sxs-lookup"><span data-stu-id="8b39f-120">FC\_OP</span></span>           | <span data-ttu-id="8b39f-121">Puntero único en una interfaz de objeto.</span><span class="sxs-lookup"><span data-stu-id="8b39f-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="8b39f-122">La razón para distinguir FC OP es semántica: en las interfaces de objeto, se debe liberar un puntero in-out antes de desmarque un nuevo objeto y asignar un nuevo valor \_ \[ de \] puntero.</span><span class="sxs-lookup"><span data-stu-id="8b39f-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="8b39f-123">Los \_ atributos<1> pueden tener cualquiera de las marcas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8b39f-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="8b39f-124">Atributo</span><span class="sxs-lookup"><span data-stu-id="8b39f-124">Attribute</span></span> | <span data-ttu-id="8b39f-125">Marca</span><span class="sxs-lookup"><span data-stu-id="8b39f-125">Flag</span></span>              | <span data-ttu-id="8b39f-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b39f-126">Description</span></span>                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b39f-127">01</span><span class="sxs-lookup"><span data-stu-id="8b39f-127">01</span></span>   | <span data-ttu-id="8b39f-128">FC \_ ASIGNA TODOS LOS \_ \_ NODOS</span><span class="sxs-lookup"><span data-stu-id="8b39f-128">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="8b39f-129">El puntero forma parte de un esquema de asignación allocate(all \_ nodes).</span><span class="sxs-lookup"><span data-stu-id="8b39f-129">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="8b39f-130">02</span><span class="sxs-lookup"><span data-stu-id="8b39f-130">02</span></span>   | <span data-ttu-id="8b39f-131">FC \_ DONT \_ FREE</span><span class="sxs-lookup"><span data-stu-id="8b39f-131">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="8b39f-132">Puntero allocate(don't \_ free).</span><span class="sxs-lookup"><span data-stu-id="8b39f-132">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="8b39f-133">04</span><span class="sxs-lookup"><span data-stu-id="8b39f-133">04</span></span>   | <span data-ttu-id="8b39f-134">FC \_ ALLOCED \_ ON \_ STACK</span><span class="sxs-lookup"><span data-stu-id="8b39f-134">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="8b39f-135">Puntero cuyo referencia se asigna en la pila del código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="8b39f-135">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="8b39f-136">08</span><span class="sxs-lookup"><span data-stu-id="8b39f-136">08</span></span>   | <span data-ttu-id="8b39f-137">PUNTERO \_ SIMPLE DE \_ FC</span><span class="sxs-lookup"><span data-stu-id="8b39f-137">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="8b39f-138">Puntero a un tipo simple o cadena compatible no compatible.</span><span class="sxs-lookup"><span data-stu-id="8b39f-138">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="8b39f-139">Esta marca que se establece indica el diseño de la descripción del puntero como el diseño de puntero simple descrito anteriormente; de lo contrario, se indica el formato del descriptor con el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="8b39f-139">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="8b39f-140">10</span><span class="sxs-lookup"><span data-stu-id="8b39f-140">10</span></span>   | <span data-ttu-id="8b39f-141">FC \_ POINTER \_ DEREF</span><span class="sxs-lookup"><span data-stu-id="8b39f-141">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="8b39f-142">Puntero que se debe desreferenciar antes de controlar el referenciador del puntero.</span><span class="sxs-lookup"><span data-stu-id="8b39f-142">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="8b39f-143">Los punteros que tienen size \_ is(), max \_ is(), length \_ is(), last \_ is() o first \_ is() aplicados \_ \_ \_ tienen descripciones de cadenas de formato idénticas a un puntero a una matriz del tipo adecuado (por ejemplo, una matriz compatible si size is() se aplica, una matriz variable conforme si size is() y length se aplica).</span><span class="sxs-lookup"><span data-stu-id="8b39f-143">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="8b39f-144">Punteros de interfaz</span><span class="sxs-lookup"><span data-stu-id="8b39f-144">Interface Pointers</span></span>

<span data-ttu-id="8b39f-145">Una cadena de formato de puntero de interfaz de objeto tiene uno de dos formatos, dependiendo de si el compilador conoce el IID correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8b39f-145">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="8b39f-146">Un puntero de interfaz con un IID constante tiene la descripción siguiente:</span><span class="sxs-lookup"><span data-stu-id="8b39f-146">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="8b39f-147">El valor de<16> es el IID real del puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="8b39f-147">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="8b39f-148">El iid se escribe en la cadena de formato en un formato idéntico a la estructura de datos GUID: long, short, short, char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="8b39f-148">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="8b39f-149">La descripción de un puntero de interfaz con \_ iid is() aplicado a él es:</span><span class="sxs-lookup"><span data-stu-id="8b39f-149">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="8b39f-150">La descripción de iid<> descriptor de correlación y tiene 4 o 6 bytes, dependiendo de \_ si [**se usa /robust.**](/windows/desktop/Midl/-robust)</span><span class="sxs-lookup"><span data-stu-id="8b39f-150">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="8b39f-151">El valor calculado por **la función ComputeConformance** es el puntero IID.</span><span class="sxs-lookup"><span data-stu-id="8b39f-151">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="8b39f-152">Punteros de recuento de bytes</span><span class="sxs-lookup"><span data-stu-id="8b39f-152">Byte Count Pointers</span></span>

<span data-ttu-id="8b39f-153">Los punteros de recuento de bytes se relacionan con un atributo de optimización especial denominado \[ **recuento de \_ bytes.** \]</span><span class="sxs-lookup"><span data-stu-id="8b39f-153">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="8b39f-154">Se usan los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="8b39f-154">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="8b39f-155">–y –</span><span class="sxs-lookup"><span data-stu-id="8b39f-155">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="8b39f-156">La descripción del recuento<> es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de \_ \_ si se usa [**/robust.**](/windows/desktop/Midl/-robust)</span><span class="sxs-lookup"><span data-stu-id="8b39f-156">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="8b39f-157">La descripción \_ de<> es una descripción del tipo más importante.</span><span class="sxs-lookup"><span data-stu-id="8b39f-157">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
