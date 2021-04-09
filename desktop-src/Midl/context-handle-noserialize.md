---
title: context_handle_noserialize atributo)
description: El atributo \ context \_ Handle \_ noserialization \ ACF garantiza que nunca se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize el atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789873"
---
# <a name="context_handle_noserialize-attribute"></a><span data-ttu-id="d8fce-104">atributo de identificador de contexto \_ \_ noserialización</span><span class="sxs-lookup"><span data-stu-id="d8fce-104">context\_handle\_noserialize attribute</span></span>

<span data-ttu-id="d8fce-105">El atributo **\[ identificador de contexto \_ \_ noserializate \]** ACF garantiza que nunca se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8fce-105">The **\[context\_handle\_noserialize\]** ACF attribute guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="d8fce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8fce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8fce-107">*tipo-ACF-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="d8fce-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d8fce-108">Cualquier otro atributo ACF que se aplique al tipo.</span><span class="sxs-lookup"><span data-stu-id="d8fce-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="d8fce-109">*context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="d8fce-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d8fce-110">El identificador que especifica el tipo de identificador de contexto, tal y como se define en una declaración [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="d8fce-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="d8fce-111">Este es el tipo que recibe el atributo de [**\[ \_ identificador \] de contexto**](context-handle.md) en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d8fce-111">This is the type that receives the [**\[context\_handle\]**](context-handle.md) attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="d8fce-112">*function-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d8fce-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d8fce-113">Cualquier atributo ACF adicional que se aplique a la función.</span><span class="sxs-lookup"><span data-stu-id="d8fce-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="d8fce-114">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="d8fce-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d8fce-115">Nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d8fce-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="d8fce-116">*parámetro-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d8fce-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d8fce-117">Cualquier otro atributo ACF que se aplique al parámetro.</span><span class="sxs-lookup"><span data-stu-id="d8fce-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d8fce-118">*param: nombre*</span><span class="sxs-lookup"><span data-stu-id="d8fce-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d8fce-119">Nombre del parámetro tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d8fce-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8fce-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8fce-120">Remarks</span></span>

<span data-ttu-id="d8fce-121">El atributo de [**\[ \_ identificador \] de contexto**](context-handle.md) identifica un identificador de enlace que mantiene el contexto o la información de estado en el servidor entre las llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="d8fce-121">The [**\[context\_handle\]**](context-handle.md) attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span> <span data-ttu-id="d8fce-122">El atributo puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función, o como un atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="d8fce-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="d8fce-123">De forma predeterminada, se serializan las llamadas en los identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="d8fce-123">By default, calls on context handles are serialized.</span></span> <span data-ttu-id="d8fce-124">Una aplicación puede llamar a [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) para invalidar este comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d8fce-124">An application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="d8fce-125">El uso del atributo de [**\[ \_ identificador \] de contexto**](context-handle.md) en un archivo ACF garantiza que las llamadas en este identificador de contexto determinado no se serializarán, independientemente del comportamiento de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="d8fce-125">Using the [**\[context\_handle\]**](context-handle.md) attribute in an ACF file guarantees that calls on this particular context handle will not be serialized, regardless of the calling application's behavior.</span></span> <span data-ttu-id="d8fce-126">Proporcionar una rutina de Resumen de contexto es opcional.</span><span class="sxs-lookup"><span data-stu-id="d8fce-126">Providing a context rundown routine is optional.</span></span>

<span data-ttu-id="d8fce-127">Este atributo está disponible en la versión 5,0 de MIDL.</span><span class="sxs-lookup"><span data-stu-id="d8fce-127">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="d8fce-128">**Windows server 2003 y Windows XP o posterior:** Una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado).</span><span class="sxs-lookup"><span data-stu-id="d8fce-128">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="d8fce-129">Estas capacidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores).</span><span class="sxs-lookup"><span data-stu-id="d8fce-129">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="d8fce-130">Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="d8fce-130">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="d8fce-131">Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados.</span><span class="sxs-lookup"><span data-stu-id="d8fce-131">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="d8fce-132">Tenga en cuenta que los métodos de creación se serializan implícitamente.</span><span class="sxs-lookup"><span data-stu-id="d8fce-132">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="d8fce-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d8fce-133">Examples</span></span>

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="d8fce-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8fce-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8fce-135">Atributos ACF</span><span class="sxs-lookup"><span data-stu-id="d8fce-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="d8fce-136">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="d8fce-136">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="d8fce-137">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="d8fce-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="d8fce-138">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="d8fce-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="d8fce-139">**RpcSsDontSerializeContext**</span><span class="sxs-lookup"><span data-stu-id="d8fce-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="d8fce-140">Rutina de ejecución de contexto de servidor</span><span class="sxs-lookup"><span data-stu-id="d8fce-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="d8fce-141">Clientes multiproceso y controladores de contexto</span><span class="sxs-lookup"><span data-stu-id="d8fce-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="d8fce-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="d8fce-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 