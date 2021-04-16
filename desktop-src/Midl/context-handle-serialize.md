---
title: context_handle_serialize atributo)
description: El atributo \ context \_ Handle \_ SERIALIZE \ ACF garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize el atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685694"
---
# <a name="context_handle_serialize-attribute"></a><span data-ttu-id="facb0-104">\_atributo Serialize del controlador de contexto \_</span><span class="sxs-lookup"><span data-stu-id="facb0-104">context\_handle\_serialize attribute</span></span>

<span data-ttu-id="facb0-105">El atributo **\[ identificador de contexto \_ \_ Serialize \]** de serialización garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="facb0-105">The **\[context\_handle\_serialize\]** ACF attribute guarantees that a context handle will always be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="facb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="facb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="facb0-107">*tipo-ACF-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="facb0-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="facb0-108">Cualquier otro atributo ACF que se aplique al tipo.</span><span class="sxs-lookup"><span data-stu-id="facb0-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="facb0-109">*context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="facb0-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="facb0-110">El identificador que especifica el tipo de identificador de contexto, tal y como se define en una declaración [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="facb0-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="facb0-111">Este es el tipo que recibe el atributo **\[ \_ \_ Serialize \] de identificador de contexto** en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="facb0-111">This is the type that receives the **\[context\_handle\_serialize\]** attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="facb0-112">*function-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="facb0-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="facb0-113">Cualquier atributo ACF adicional que se aplique a la función.</span><span class="sxs-lookup"><span data-stu-id="facb0-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="facb0-114">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="facb0-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="facb0-115">Nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="facb0-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="facb0-116">*parámetro-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="facb0-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="facb0-117">Cualquier otro atributo ACF que se aplique al parámetro.</span><span class="sxs-lookup"><span data-stu-id="facb0-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="facb0-118">*param: nombre*</span><span class="sxs-lookup"><span data-stu-id="facb0-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="facb0-119">Nombre del parámetro tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="facb0-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="facb0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="facb0-120">Remarks</span></span>

<span data-ttu-id="facb0-121">El atributo **\[ \_ \_ Serialize \] del controlador de contexto** identifica un identificador de enlace que mantiene la información de contexto o de estado en el servidor entre las llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="facb0-121">The **\[context\_handle\_serialize\]** attribute identifies a binding handle that maintains context or state information on the server between remote procedure calls.</span></span> <span data-ttu-id="facb0-122">El atributo puede aparecer como un atributo de tipo [**typedef**](typedef.md) de IDL, como un atributo de tipo de valor devuelto de función, o como un atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="facb0-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="facb0-123">De forma predeterminada, las llamadas a los identificadores de contexto se serializan, pero una aplicación puede llamar a [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) para invalidar este comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="facb0-123">By default, calls on context handles are serialized, but an application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="facb0-124">El uso del atributo **\[ \_ \_ Serialize \] de identificador de contexto** en un archivo ACF garantiza que las llamadas en este identificador de contexto determinado se serializarán, incluso si la aplicación que realiza la llamada ha invalidado la serialización predeterminada.</span><span class="sxs-lookup"><span data-stu-id="facb0-124">Using the **\[context\_handle\_serialize\]** attribute in an ACF file guarantees that calls on this particular context handle will be serialized, even if the calling application has overridden the default serialization.</span></span> <span data-ttu-id="facb0-125">Una rutina de informe detallado de contexto es opcional.</span><span class="sxs-lookup"><span data-stu-id="facb0-125">A context rundown routine is optional.</span></span>

<span data-ttu-id="facb0-126">Este atributo está disponible en la versión 5,0 de MIDL.</span><span class="sxs-lookup"><span data-stu-id="facb0-126">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="facb0-127">**Windows server 2003 y Windows XP o posterior:** Una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado).</span><span class="sxs-lookup"><span data-stu-id="facb0-127">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="facb0-128">Estas capacidades de acceso son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores).</span><span class="sxs-lookup"><span data-stu-id="facb0-128">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="facb0-129">Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="facb0-129">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="facb0-130">Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados.</span><span class="sxs-lookup"><span data-stu-id="facb0-130">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="facb0-131">Tenga en cuenta que los métodos de creación se serializan implícitamente.</span><span class="sxs-lookup"><span data-stu-id="facb0-131">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="facb0-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="facb0-132">Examples</span></span>

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="facb0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="facb0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="facb0-134">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="facb0-134">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="facb0-135">Atributos ACF</span><span class="sxs-lookup"><span data-stu-id="facb0-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="facb0-136">**identificador de contexto de \_ \_ noserialización**</span><span class="sxs-lookup"><span data-stu-id="facb0-136">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="facb0-137">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="facb0-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="facb0-138">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="facb0-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="facb0-139">**RpcSsDontSerializeContext**</span><span class="sxs-lookup"><span data-stu-id="facb0-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="facb0-140">Rutina de ejecución de contexto de servidor</span><span class="sxs-lookup"><span data-stu-id="facb0-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="facb0-141">Clientes multiproceso y controladores de contexto</span><span class="sxs-lookup"><span data-stu-id="facb0-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="facb0-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="facb0-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 