---
title: byte_count atributo)
description: El atributo @ byte \_ Count \ ACF es un atributo de parámetro que asocia un tamaño, en bytes, con el área de memoria indicada por el puntero.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count el atributo MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358210"
---
# <a name="byte_count-attribute"></a><span data-ttu-id="07343-104">byte \_ Count (atributo)</span><span class="sxs-lookup"><span data-stu-id="07343-104">byte\_count attribute</span></span>

<span data-ttu-id="07343-105">El atributo ACF de **\[ \_ recuento \] de bytes** es un atributo de parámetro que asocia un tamaño, en bytes, con el área de memoria indicada por el puntero.</span><span class="sxs-lookup"><span data-stu-id="07343-105">The **\[byte\_count\]** ACF attribute is a parameter attribute that associates a size, in bytes, with the memory area indicated by the pointer.</span></span>

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a><span data-ttu-id="07343-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07343-107">*lista de atributos de función*</span><span class="sxs-lookup"><span data-stu-id="07343-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="07343-108">Especifica cero o más atributos de función ACF.</span><span class="sxs-lookup"><span data-stu-id="07343-108">Specifies zero or more ACF function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="07343-109">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="07343-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="07343-110">Especifica el nombre de la función definida en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="07343-110">Specifies the name of the function defined in the IDL file.</span></span> <span data-ttu-id="07343-111">El nombre de la función es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="07343-111">The function name is required.</span></span>

</dd> <dt>

<span data-ttu-id="07343-112">*Length-variable-Name*</span><span class="sxs-lookup"><span data-stu-id="07343-112">*length-variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="07343-113">Especifica el nombre del parámetro de solo [**\[ en \]**](in.md)que especifica el tamaño, en bytes, del área de memoria a la que hace referencia el *parámetro-name*.</span><span class="sxs-lookup"><span data-stu-id="07343-113">Specifies the name of the [**\[in\]**](in.md)-only parameter that specifies the size, in bytes, of the memory area referenced by *parameter-name*.</span></span>

</dd> <dt>

<span data-ttu-id="07343-114">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="07343-114">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="07343-115">Especifica el nombre del parámetro de puntero de solo [**\[ salida \]**](out-idl.md)definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="07343-115">Specifies the name of the [**\[out\]**](out-idl.md)-only pointer parameter defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07343-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07343-116">Remarks</span></span>

<span data-ttu-id="07343-117">El **\[ \_ número \] de bytes** del atributo ACF representa una extensión de Microsoft para DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="07343-117">The ACF attribute **\[byte\_count\]** represents a Microsoft extension to DCE IDL.</span></span> <span data-ttu-id="07343-118">Por lo tanto, este atributo no está disponible cuando se usa el modificador de compilador MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="07343-118">Therefore, this attribute is not available when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

> [!Note]  
> <span data-ttu-id="07343-119">El atributo de **\[ recuento \] de bytes** ya no se admite en la sintaxis de NDR64 debido a la dificultad en la estimación del tamaño necesario para todos los parámetros de [**\[ salida \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="07343-119">The **\[byte count\]** attribute is no longer supported in NDR64 syntax due to the difficulty in estimating the size required for all [**\[out\]**](out-idl.md) parameters.</span></span>

 

<span data-ttu-id="07343-120">La memoria a la que hace referencia el parámetro de puntero es contigua y no la asigna ni libera el código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="07343-120">Memory referenced by the pointer parameter is contiguous and is not allocated or freed by the client stubs.</span></span> <span data-ttu-id="07343-121">Esta característica del atributo **\[ \_ recuento \] de bytes** le permite crear un área de búfer persistente en la memoria del cliente que se puede reutilizar durante más de una llamada al procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="07343-121">This feature of the **\[byte\_count\]** attribute lets you create a persistent buffer area in client memory that can be reused during more than one call to the remote procedure.</span></span>

<span data-ttu-id="07343-122">La capacidad de desactivar la asignación de memoria de código auxiliar de cliente permite optimizar la aplicación para mejorar la eficacia.</span><span class="sxs-lookup"><span data-stu-id="07343-122">The ability to turn off the client stub memory allocation lets you tune the application for efficiency.</span></span> <span data-ttu-id="07343-123">Por ejemplo, las funciones de proveedor de servicios que usan Microsoft RPC pueden utilizar el atributo de **\[ \_ recuento \] de bytes** .</span><span class="sxs-lookup"><span data-stu-id="07343-123">For example, the **\[byte\_count\]** attribute can be used by service-provider functions that use Microsoft RPC.</span></span> <span data-ttu-id="07343-124">Cuando una aplicación de usuario llama a la API del proveedor de servicios y envía un puntero a un búfer, el proveedor de servicios puede pasar el puntero de búfer a la función remota.</span><span class="sxs-lookup"><span data-stu-id="07343-124">When a user application calls the service-provider API and sends a pointer to a buffer, the service provider can pass the buffer pointer on to the remote function.</span></span> <span data-ttu-id="07343-125">El proveedor de servicios puede volver a usar el búfer durante varias llamadas remotas sin forzar al usuario a reasignar el área de memoria.</span><span class="sxs-lookup"><span data-stu-id="07343-125">The service provider can reuse the buffer during multiple remote calls without forcing the user to reallocate the memory area.</span></span>

<span data-ttu-id="07343-126">El área de memoria puede contener estructuras de datos complejas que se componen de varios punteros.</span><span class="sxs-lookup"><span data-stu-id="07343-126">The memory area can contain complex data structures that consist of multiple pointers.</span></span> <span data-ttu-id="07343-127">Dado que el área de memoria es contiguo, la aplicación no tiene que realizar varias llamadas para liberar cada puntero y estructura de forma individual.</span><span class="sxs-lookup"><span data-stu-id="07343-127">Because the memory area is contiguous, the application does not have to make several calls to individually free each pointer and structure.</span></span> <span data-ttu-id="07343-128">En su lugar, puede asignar o liberar el área de memoria con una llamada a la asignación de memoria o la rutina libre.</span><span class="sxs-lookup"><span data-stu-id="07343-128">Instead, it can allocate or free the memory area with one call to the memory allocation or free routine.</span></span>

<span data-ttu-id="07343-129">El búfer debe ser un parámetro de solo [**\[ salida \]**](out-idl.md), mientras que la longitud del búfer en bytes debe ser un parámetro solo [**\[ en \]**](in.md).</span><span class="sxs-lookup"><span data-stu-id="07343-129">The buffer must be an [**\[out\]**](out-idl.md)-only parameter, while the buffer length in bytes must be an [**\[in\]**](in.md)-only parameter.</span></span>

<span data-ttu-id="07343-130">Especifique un búfer que sea lo suficientemente grande como para contener todos los parámetros de [**\[ salida \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="07343-130">Specify a buffer that is large enough to contain all the [**\[out\]**](out-idl.md) parameters.</span></span> <span data-ttu-id="07343-131">Debido al relleno oculto, utilice las sobreestimaciones en lugar de los recuentos exactos.</span><span class="sxs-lookup"><span data-stu-id="07343-131">Because of hidden padding, use overestimates rather than exact counts.</span></span> <span data-ttu-id="07343-132">Por ejemplo, no se calculan las referencias de los punteros de 4 bytes en un límite alineado de 4 bytes en plataformas de 32 bits y punteros de 8 bytes en un límite de 8 bytes en plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="07343-132">For example, 4-byte pointers are unmarshaled on a 4-byte aligned boundary on 32-bit platforms and 8-byte pointers on an 8-byte boundary on 64-bit platforms.</span></span> <span data-ttu-id="07343-133">Por lo tanto, el relleno de alineación que realizará el código auxiliar se debe tener en cuenta en el espacio del búfer.</span><span class="sxs-lookup"><span data-stu-id="07343-133">Therefore, the alignment padding the stubs will perform must be accounted for in the space for the buffer.</span></span> <span data-ttu-id="07343-134">Además, los niveles de empaquetado utilizados durante la compilación del lenguaje C pueden variar.</span><span class="sxs-lookup"><span data-stu-id="07343-134">In addition, packing levels used during C-language compilation can vary.</span></span> <span data-ttu-id="07343-135">Use un valor de recuento de bytes que tenga en cuenta los bytes de empaquetado adicionales agregados para el nivel de empaquetado usado durante la compilación del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="07343-135">Use a byte count value that accounts for additional packing bytes added for the packing level used during C-language compilation.</span></span> <span data-ttu-id="07343-136">Una práctica segura que abarque las plataformas de 32 bits y las plataformas de 64 bits es suponer que cada objeto que entra en el bloque de gran memoria comienza en una dirección que es un múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="07343-136">A safe practice that covers both 32 bit platforms and 64 bit platforms is to assume that each object going into the big memory block starts at an address that is a multiple of 8.</span></span>

## <a name="examples"></a><span data-ttu-id="07343-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="07343-137">Examples</span></span>

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a><span data-ttu-id="07343-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="07343-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07343-139">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="07343-139">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="07343-140">**de**</span><span class="sxs-lookup"><span data-stu-id="07343-140">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="07343-141">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="07343-141">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="07343-142">**/osf**</span><span class="sxs-lookup"><span data-stu-id="07343-142">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="07343-143">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="07343-143">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="07343-144">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="07343-144">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 




