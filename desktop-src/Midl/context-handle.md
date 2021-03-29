---
title: context_handle atributo)
description: El atributo \ context \_ handler identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre las llamadas a procedimiento remoto.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle el atributo MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789868"
---
# <a name="context_handle-attribute"></a><span data-ttu-id="2b071-104">atributo de identificador de contexto \_</span><span class="sxs-lookup"><span data-stu-id="2b071-104">context\_handle attribute</span></span>

<span data-ttu-id="2b071-105">El atributo de **\[ \_ identificador \] de contexto** identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre las llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="2b071-105">The **\[context\_handle\]** attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span>

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a><span data-ttu-id="2b071-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b071-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b071-107">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="2b071-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-108">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="2b071-108">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="2b071-109">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="2b071-109">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-110">Especifica un tipo de puntero o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="2b071-110">Specifies a pointer type or a type identifier.</span></span> <span data-ttu-id="2b071-111">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="2b071-111">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="2b071-112">*declarador y lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="2b071-112">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-113">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="2b071-113">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="2b071-114">El declarador de un identificador de contexto debe incluir al menos un declarador de puntero.</span><span class="sxs-lookup"><span data-stu-id="2b071-114">The declarator for a context handle must include at least one pointer declarator.</span></span> <span data-ttu-id="2b071-115">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="2b071-115">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="2b071-116">La *lista de declaradores* consta de uno o varios declaradores, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="2b071-116">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="2b071-117">El identificador de nombre de parámetro en el declarador de función es opcional.</span><span class="sxs-lookup"><span data-stu-id="2b071-117">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="2b071-118">*function-ATTR-List*</span><span class="sxs-lookup"><span data-stu-id="2b071-118">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-119">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="2b071-119">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="2b071-120">Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[ \_ identificador \] de contexto**.</span><span class="sxs-lookup"><span data-stu-id="2b071-120">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="2b071-121">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="2b071-121">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-122">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="2b071-122">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="2b071-123">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del **\*** designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="2b071-123">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b071-124">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="2b071-124">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-125">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="2b071-125">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="2b071-126">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="2b071-126">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-127">Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="2b071-127">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="2b071-128">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="2b071-128">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="2b071-129">*context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="2b071-129">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2b071-130">Especifica el identificador que especifica el tipo de identificador de contexto tal y como se define en una declaración [**typedef**](typedef.md) que toma el atributo de **\[ \_ identificador \] de contexto** .</span><span class="sxs-lookup"><span data-stu-id="2b071-130">Specifies the identifier that specifies the context handle type as defined in a [**typedef**](typedef.md) declaration that takes the **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="2b071-131">La rutina de informe detallado es opcional.</span><span class="sxs-lookup"><span data-stu-id="2b071-131">The rundown routine is optional.</span></span>

<span data-ttu-id="2b071-132">**Windows server 2003 y Windows XP:** Una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado).</span><span class="sxs-lookup"><span data-stu-id="2b071-132">**Windows ServerÂ 2003 and WindowsÂ XP:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="2b071-133">Estas capacidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores).</span><span class="sxs-lookup"><span data-stu-id="2b071-133">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="2b071-134">Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="2b071-134">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="2b071-135">Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados.</span><span class="sxs-lookup"><span data-stu-id="2b071-135">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="2b071-136">Tenga en cuenta que los métodos de creación se serializan implícitamente.</span><span class="sxs-lookup"><span data-stu-id="2b071-136">Note that creation methods are implicitly serialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b071-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b071-137">Remarks</span></span>

<span data-ttu-id="2b071-138">El atributo de **\[ \_ identificador \] de contexto** puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función o como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="2b071-138">The **\[context\_handle\]** attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span> <span data-ttu-id="2b071-139">Al aplicar el atributo de **\[ \_ identificador \] de contexto** a una definición de tipo, también debe proporcionar una rutina de Resumen de contexto.</span><span class="sxs-lookup"><span data-stu-id="2b071-139">When you apply the **\[context\_handle\]** attribute to a type definition, you must also provide a context rundown routine.</span></span> <span data-ttu-id="2b071-140">Vea [rutina de ejecución de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2b071-140">See [Server Context Run-down Routine](/windows/desktop/Rpc/server-context-run-down-routine) for details.</span></span>

<span data-ttu-id="2b071-141">Cuando se usa el compilador MIDL en modo predeterminado ([**/MS \_ ext**](-ms-ext.md)), un identificador de contexto puede ser cualquier tipo de puntero seleccionado por el usuario, siempre que cumpla los requisitos de los identificadores de contexto que se describen aquí.</span><span class="sxs-lookup"><span data-stu-id="2b071-141">When you use the MIDL compiler in default ([**/ms\_ext**](-ms-ext.md)) mode, a context handle can be any pointer type selected by the user, as long as it complies with the requirements for context handles described here.</span></span> <span data-ttu-id="2b071-142">Los datos asociados a este tipo de identificador de contexto no se transmiten en la red y solo la aplicación de servidor debe manipularlos.</span><span class="sxs-lookup"><span data-stu-id="2b071-142">The data associated with such a context handle type is not transmitted on the network and should only be manipulated by the server application.</span></span> <span data-ttu-id="2b071-143">Los compiladores de DCE IDL restringen los identificadores de contexto a punteros de tipo [**void**](void.md) **\*** .</span><span class="sxs-lookup"><span data-stu-id="2b071-143">DCE IDL compilers restrict context handles to pointers of type [**void**](void.md) **\***.</span></span> <span data-ttu-id="2b071-144">Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="2b071-144">Therefore this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="2b071-145">Como con otros tipos de identificadores, el identificador de contexto es opaco para la aplicación cliente y no se transmite ningún dato asociado a él.</span><span class="sxs-lookup"><span data-stu-id="2b071-145">As with other handle types, the context handle is opaque to the client application, and any data associated with it is not transmitted.</span></span> <span data-ttu-id="2b071-146">En el servidor, el identificador de contexto actúa como un identificador en el contexto activo y se puede tener acceso a todos los datos asociados al tipo de identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="2b071-146">On the server, the context handle serves as a handle on active context, and all data associated with the context handle type is accessible.</span></span>

<span data-ttu-id="2b071-147">Para crear un identificador de contexto, el cliente pasa al servidor un **\[** puntero [**out**](out-idl.md) **\]** , **\[** [**ref**](ref.md) **\]** a un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="2b071-147">To create a context handle, the client passes to the server an **\[**[**out**](out-idl.md)**\]**, **\[**[**ref**](ref.md)**\]** pointer to a context handle.</span></span> <span data-ttu-id="2b071-148">(El propio identificador de contexto puede tener un valor **null** o distinto de **null** , siempre que su valor sea coherente con sus atributos de puntero.</span><span class="sxs-lookup"><span data-stu-id="2b071-148">(The context handle itself can have a **NULL** or non-**NULL** value—as long as its value is consistent with its pointer attributes.</span></span> <span data-ttu-id="2b071-149">Por ejemplo, cuando el tipo de identificador de contexto tiene **\[** [](ref.md) **\]** aplicado el atributo ref, no puede tener un valor **null** . Se debe proporcionar otro identificador de enlace para realizar el enlace hasta que se cree el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="2b071-149">For example, when the context handle type has the **\[**[**ref**](ref.md)**\]** attribute applied to it, it cannot have a **NULL** value.) Another binding handle must be supplied to accomplish the binding until the context handle is created.</span></span> <span data-ttu-id="2b071-150">Cuando no se especifica ningún identificador explícito, se utiliza el enlace implícito.</span><span class="sxs-lookup"><span data-stu-id="2b071-150">When no explicit handle is specified, implicit binding is used.</span></span> <span data-ttu-id="2b071-151">Cuando no hay ningún **\[** atributo de [**\_ identificador implícito**](implicit-handle.md) **\]** presente, se utiliza un identificador automático.</span><span class="sxs-lookup"><span data-stu-id="2b071-151">When no **\[**[**implicit\_handle**](implicit-handle.md)**\]** attribute is present, an auto handle is used.</span></span>

<span data-ttu-id="2b071-152">El procedimiento remoto en el servidor crea un identificador de contexto activo.</span><span class="sxs-lookup"><span data-stu-id="2b071-152">The remote procedure on the server creates an active context handle.</span></span> <span data-ttu-id="2b071-153">El cliente debe utilizar ese identificador de contexto como un **\[** [](in.md) **\]** parámetro in o **\[ in**, **out \]** en las llamadas posteriores.</span><span class="sxs-lookup"><span data-stu-id="2b071-153">The client must use that context handle as an **\[**[**in**](in.md)**\]** or **\[in**, **out\]** parameter in subsequent calls.</span></span> <span data-ttu-id="2b071-154">Un identificador **\[ \] de** contexto solo se puede usar como identificador de enlace, por lo que debe tener un valor distinto de **null** .</span><span class="sxs-lookup"><span data-stu-id="2b071-154">An **\[in\]**-only context handle can be used as a binding handle, so it must have a non-**NULL** value.</span></span> <span data-ttu-id="2b071-155">Un identificador **\[ de contexto de solo en \]** no refleja los cambios de estado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="2b071-155">An **\[in\]**-only context handle does not reflect state changes on the server.</span></span>

<span data-ttu-id="2b071-156">En el servidor, el procedimiento llamado puede interpretar el identificador de contexto según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2b071-156">On the server, the called procedure can interpret the context handle as needed.</span></span> <span data-ttu-id="2b071-157">Por ejemplo, el procedimiento llamado puede asignar almacenamiento de montón y usar el identificador de contexto como un puntero a este almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2b071-157">For example, the called procedure can allocate heap storage and use the context handle as a pointer to this storage.</span></span>

<span data-ttu-id="2b071-158">Para cerrar un identificador de contexto, el cliente pasa el identificador de contexto como un **\[** argumento [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2b071-158">To close a context handle, the client passes the context handle as an **\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]** argument.</span></span> <span data-ttu-id="2b071-159">El servidor debe devolver un identificador de contexto **nulo** cuando ya no se mantiene el contexto en nombre del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2b071-159">The server must return a **NULL** context handle when it is no longer maintaining context on behalf of the caller.</span></span> <span data-ttu-id="2b071-160">Por ejemplo, si el identificador de contexto representa un archivo abierto y la llamada cierra el archivo, el servidor debe establecer el identificador de contexto en **null** y devolverlo al cliente.</span><span class="sxs-lookup"><span data-stu-id="2b071-160">For example, if the context handle represents an open file and the call closes the file, the server must set the context handle to **NULL** and return it to the client.</span></span> <span data-ttu-id="2b071-161">Un valor **null** no es válido como un controlador de enlace en las llamadas subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="2b071-161">A **NULL** value is invalid as a binding handle on subsequent calls.</span></span>

<span data-ttu-id="2b071-162">Un identificador de contexto solo es válido para un servidor.</span><span class="sxs-lookup"><span data-stu-id="2b071-162">A context handle is only valid for one server.</span></span> <span data-ttu-id="2b071-163">Cuando una función tiene dos parámetros de identificador y el identificador de contexto no es **null**, los identificadores de enlace deben hacer referencia al mismo espacio de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2b071-163">When a function has two handle parameters and the context handle is not **NULL**, the binding handles must refer to the same address space.</span></span>

<span data-ttu-id="2b071-164">Cuando una función tiene un **\[** [**en**](in.md) **\]** o un identificador **\[ de contexto de** **salida \]** , su identificador de contexto se puede usar como identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="2b071-164">When a function has an **\[**[**in**](in.md)**\]** or an **\[in**, **out\]** context handle, its context handle can be used as the binding handle.</span></span> <span data-ttu-id="2b071-165">En este caso, no se utiliza el enlace implícito y **\[** se omite el [**\_ identificador implícito**](implicit-handle.md) **\]** o el atributo de **\[** [**\_ identificador automático**](auto-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2b071-165">In this case, implicit binding is not used and the **\[**[**implicit\_handle**](implicit-handle.md)**\]** or **\[**[**auto\_handle**](auto-handle.md)**\]** attribute is ignored.</span></span>

<span data-ttu-id="2b071-166">Las restricciones siguientes se aplican a los identificadores de contexto:</span><span class="sxs-lookup"><span data-stu-id="2b071-166">The following restrictions apply to context handles:</span></span>

-   <span data-ttu-id="2b071-167">Los identificadores de contexto no pueden ser elementos de matriz, miembros de estructura o miembros de Unión.</span><span class="sxs-lookup"><span data-stu-id="2b071-167">Context handles cannot be array elements, structure members, or union members.</span></span> <span data-ttu-id="2b071-168">Solo pueden ser parámetros.</span><span class="sxs-lookup"><span data-stu-id="2b071-168">They can only be parameters.</span></span>
-   <span data-ttu-id="2b071-169">Los identificadores de contexto no pueden tener el **\[** atributo [**transmitir \_ como**](transmit-as.md) **\]** o **\[** [**representar \_ como**](represent-as.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2b071-169">Context handles cannot have the **\[**[**transmit\_as**](transmit-as.md)**\]** or **\[**[**represent\_as**](represent-as.md)**\]** attribute.</span></span>
-   <span data-ttu-id="2b071-170">Los parámetros que son punteros a **\[** [](out-idl.md) **\]** identificadores de contexto de salida deben ser **\[** [](ref.md) **\]** punteros de referencia.</span><span class="sxs-lookup"><span data-stu-id="2b071-170">Parameters that are pointers to **\[**[**out**](out-idl.md)**\]** context handles must be **\[**[**ref**](ref.md)**\]** pointers.</span></span>
-   <span data-ttu-id="2b071-171">Se **\[** [](in.md) **\]** puede usar un en el identificador de contexto como identificador de enlace y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="2b071-171">An **\[**[**in**](in.md)**\]** context handle can be used as the binding handle and cannot be **NULL**.</span></span>
-   <span data-ttu-id="2b071-172">En, un identificador **\[ de contexto de** [**salida**](out-idl.md) puede ser **null** en la entrada, pero solo si el procedimiento tiene otro parámetro de identificador explícito.</span><span class="sxs-lookup"><span data-stu-id="2b071-172">An **\[in**, [**out**](out-idl.md) context handle can be **NULL** on input, but only if the procedure has another explicit handle parameter.</span></span> <span data-ttu-id="2b071-173">Si no hay ningún otro parámetro **\[ de identificador de** contexto no **nulo** explícito, el identificador de contexto de **salida \]** no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="2b071-173">If there are no other explicit non-**NULL** context handle parameters, the **\[in**, **out\]** context handle cannot be **NULL**.</span></span>
-   <span data-ttu-id="2b071-174">No se puede usar un identificador de contexto con devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="2b071-174">A context handle cannot be used with callbacks.</span></span>

## <a name="examples"></a><span data-ttu-id="2b071-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2b071-175">Examples</span></span>

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a><span data-ttu-id="2b071-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b071-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b071-177">**matrices**</span><span class="sxs-lookup"><span data-stu-id="2b071-177">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="2b071-178">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="2b071-178">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="2b071-179">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="2b071-179">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="2b071-180">Restablecimiento de contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="2b071-180">Client Context Reset</span></span>](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[<span data-ttu-id="2b071-181">**const**</span><span class="sxs-lookup"><span data-stu-id="2b071-181">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="2b071-182">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="2b071-182">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="2b071-183">**asa**</span><span class="sxs-lookup"><span data-stu-id="2b071-183">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="2b071-184">Enlace y controladores</span><span class="sxs-lookup"><span data-stu-id="2b071-184">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="2b071-185">**omitir**</span><span class="sxs-lookup"><span data-stu-id="2b071-185">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="2b071-186">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="2b071-186">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="2b071-187">**de**</span><span class="sxs-lookup"><span data-stu-id="2b071-187">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="2b071-188">**localizar**</span><span class="sxs-lookup"><span data-stu-id="2b071-188">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="2b071-189">Clientes multiproceso y controladores de contexto</span><span class="sxs-lookup"><span data-stu-id="2b071-189">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="2b071-190">**\_ext/MS**</span><span class="sxs-lookup"><span data-stu-id="2b071-190">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="2b071-191">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="2b071-191">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="2b071-192">**ptr**</span><span class="sxs-lookup"><span data-stu-id="2b071-192">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="2b071-193">**ref**</span><span class="sxs-lookup"><span data-stu-id="2b071-193">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="2b071-194">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="2b071-194">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="2b071-195">**RpcSsDestroyClientContext**</span><span class="sxs-lookup"><span data-stu-id="2b071-195">**RpcSsDestroyClientContext**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[<span data-ttu-id="2b071-196">Rutina de ejecución de contexto de servidor</span><span class="sxs-lookup"><span data-stu-id="2b071-196">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="2b071-197">**string**</span><span class="sxs-lookup"><span data-stu-id="2b071-197">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="2b071-198">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="2b071-198">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="2b071-199">**typedef**</span><span class="sxs-lookup"><span data-stu-id="2b071-199">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="2b071-200">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="2b071-200">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="2b071-201">**void**</span><span class="sxs-lookup"><span data-stu-id="2b071-201">**void**</span></span>](void.md)
</dt> </dl>

 

 