---
title: Punteros (RPC)
description: Punteros
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149779"
---
# <a name="pointers-rpc"></a><span data-ttu-id="1b24d-103">Punteros (RPC)</span><span class="sxs-lookup"><span data-stu-id="1b24d-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="1b24d-104">Punteros comunes</span><span class="sxs-lookup"><span data-stu-id="1b24d-104">Common Pointers</span></span>

<span data-ttu-id="1b24d-105">Un puntero común se define como todo lo que no sea punteros de interfaz y punteros de recuento de bytes.</span><span class="sxs-lookup"><span data-stu-id="1b24d-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="1b24d-106">Hay dos diseños posibles para la descripción:</span><span class="sxs-lookup"><span data-stu-id="1b24d-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="1b24d-107">-o bien-</span><span class="sxs-lookup"><span data-stu-id="1b24d-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="1b24d-108">El primer formato se utiliza si el puntero es un puntero a un tipo simple o un puntero de cadena sin tamaño.</span><span class="sxs-lookup"><span data-stu-id="1b24d-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="1b24d-109">El segundo formato se utiliza para punteros a todos los demás tipos.</span><span class="sxs-lookup"><span data-stu-id="1b24d-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="1b24d-110">Los atributos de puntero indican qué diseño de la descripción es con la \_ marca de puntero simple de FC \_ .</span><span class="sxs-lookup"><span data-stu-id="1b24d-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="1b24d-111">\_el tipo de puntero<1> es uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="1b24d-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="1b24d-112">Carácter de formato</span><span class="sxs-lookup"><span data-stu-id="1b24d-112">Format character</span></span> | <span data-ttu-id="1b24d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b24d-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="1b24d-114">RP de FC \_</span><span class="sxs-lookup"><span data-stu-id="1b24d-114">FC\_RP</span></span>           | <span data-ttu-id="1b24d-115">Puntero de referencia.</span><span class="sxs-lookup"><span data-stu-id="1b24d-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="1b24d-116">FC \_ up</span><span class="sxs-lookup"><span data-stu-id="1b24d-116">FC\_UP</span></span>           | <span data-ttu-id="1b24d-117">Un puntero único.</span><span class="sxs-lookup"><span data-stu-id="1b24d-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="1b24d-118">FP de FC \_</span><span class="sxs-lookup"><span data-stu-id="1b24d-118">FC\_FP</span></span>           | <span data-ttu-id="1b24d-119">Puntero completo.</span><span class="sxs-lookup"><span data-stu-id="1b24d-119">A full pointer.</span></span>                          |
| <span data-ttu-id="1b24d-120">OP de FC \_</span><span class="sxs-lookup"><span data-stu-id="1b24d-120">FC\_OP</span></span>           | <span data-ttu-id="1b24d-121">Un puntero único en una interfaz de objeto.</span><span class="sxs-lookup"><span data-stu-id="1b24d-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="1b24d-122">La razón para distinguir FC \_ op es semántica: en las interfaces de objeto, \[ \] se debe liberar un puntero in, out antes de quitar las referencias a un nuevo objeto y asignar un nuevo valor de puntero.</span><span class="sxs-lookup"><span data-stu-id="1b24d-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="1b24d-123">Los \_ atributos de puntero<1> pueden tener cualquiera de las marcas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1b24d-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="1b24d-124">Marca</span><span class="sxs-lookup"><span data-stu-id="1b24d-124">Flag</span></span> | <span data-ttu-id="1b24d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b24d-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b24d-126">01</span><span class="sxs-lookup"><span data-stu-id="1b24d-126">01</span></span>   | <span data-ttu-id="1b24d-127">\_asignación de \_ todos los \_ nodos de FC</span><span class="sxs-lookup"><span data-stu-id="1b24d-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="1b24d-128">El puntero es una parte de un esquema de asignación de asignación (todos los \_ nodos).</span><span class="sxs-lookup"><span data-stu-id="1b24d-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1b24d-129">02</span><span class="sxs-lookup"><span data-stu-id="1b24d-129">02</span></span>   | <span data-ttu-id="1b24d-130">FC \_ \_ sin disponibilidad</span><span class="sxs-lookup"><span data-stu-id="1b24d-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="1b24d-131">Puntero de asignación (no \_ disponible).</span><span class="sxs-lookup"><span data-stu-id="1b24d-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="1b24d-132">04</span><span class="sxs-lookup"><span data-stu-id="1b24d-132">04</span></span>   | <span data-ttu-id="1b24d-133">\_ALLOCED \_ de FC en la \_ pila</span><span class="sxs-lookup"><span data-stu-id="1b24d-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="1b24d-134">Puntero cuyo referente se asigna en la pila del código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="1b24d-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="1b24d-135">08</span><span class="sxs-lookup"><span data-stu-id="1b24d-135">08</span></span>   | <span data-ttu-id="1b24d-136">\_puntero simple \_ FC</span><span class="sxs-lookup"><span data-stu-id="1b24d-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="1b24d-137">Un puntero a un tipo simple o una cadena compatible sin tamaño.</span><span class="sxs-lookup"><span data-stu-id="1b24d-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="1b24d-138">Esta marca se establece indica el diseño de la descripción del puntero como el diseño de puntero simple descrito anteriormente; de lo contrario, se indica el formato de descriptor con el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="1b24d-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="1b24d-139">10</span><span class="sxs-lookup"><span data-stu-id="1b24d-139">10</span></span>   | <span data-ttu-id="1b24d-140">\_puntero FC \_ deref</span><span class="sxs-lookup"><span data-stu-id="1b24d-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="1b24d-141">Puntero al que se debe desreferenciar antes de controlar el referente del puntero.</span><span class="sxs-lookup"><span data-stu-id="1b24d-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="1b24d-142">Los punteros cuyo tamaño \_ es (), Max \_ is (), length \_ is (), Last \_ is (), y/o First \_ is () aplicados que tienen descripciones de cadena de formato idénticas a un puntero a una matriz del tipo apropiado (por ejemplo, una matriz compatible Si se \_ aplica size (), se aplica una matriz de variación compatible Si el tamaño \_ es () y se aplica la longitud \_ .</span><span class="sxs-lookup"><span data-stu-id="1b24d-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="1b24d-143">Punteros de interfaz</span><span class="sxs-lookup"><span data-stu-id="1b24d-143">Interface Pointers</span></span>

<span data-ttu-id="1b24d-144">Una cadena de formato de puntero de interfaz de objeto tiene uno de dos formatos, dependiendo de si el compilador conoce el IID correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b24d-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="1b24d-145">Un puntero de interfaz con un IID constante tiene la siguiente descripción:</span><span class="sxs-lookup"><span data-stu-id="1b24d-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="1b24d-146">El IID<16> parte es el IID real para el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="1b24d-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="1b24d-147">El IID se escribe en la cadena de formato en un formato idéntico al de la estructura de datos GUID: Long, Short, Short, Char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="1b24d-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="1b24d-148">La descripción de un puntero de interfaz con IID \_ es () aplicada:</span><span class="sxs-lookup"><span data-stu-id="1b24d-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="1b24d-149">La descripción del IID \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="1b24d-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="1b24d-150">El valor calculado por la función **NdrComputeConformance** es el puntero IID.</span><span class="sxs-lookup"><span data-stu-id="1b24d-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="1b24d-151">Punteros de recuento de bytes</span><span class="sxs-lookup"><span data-stu-id="1b24d-151">Byte Count Pointers</span></span>

<span data-ttu-id="1b24d-152">Los punteros de recuento de bytes están relacionados con un atributo de optimización especial denominado \[ **\_ recuento de bytes** \] .</span><span class="sxs-lookup"><span data-stu-id="1b24d-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="1b24d-153">Se utilizan los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="1b24d-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="1b24d-154">etc</span><span class="sxs-lookup"><span data-stu-id="1b24d-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="1b24d-155">La descripción del recuento de bytes \_ \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="1b24d-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="1b24d-156">La descripción del puntero \_<> es una descripción del tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="1b24d-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
