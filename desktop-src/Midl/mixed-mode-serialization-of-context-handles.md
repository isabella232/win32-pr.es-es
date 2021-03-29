---
title: Serialización en modo mixto de identificadores de contexto
description: En Microsoft Windows XP, una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que se denomina serialización en modo mixto.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- Referencia del lenguaje MIDL (MIDL), serialización en modo mixto de identificadores de contexto
- identificadores de contexto MIDL
- MIDL de serialización en modo mixto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903440"
---
# <a name="mixed-mode-serialization-of-context-handles"></a><span data-ttu-id="45303-106">Serialización en modo mixto de identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="45303-106">Mixed Mode Serialization of Context Handles</span></span>

<span data-ttu-id="45303-107">A partir de Windows XP, una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado).</span><span class="sxs-lookup"><span data-stu-id="45303-107">Starting with Windows XP, a single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="45303-108">Para obtener más información sobre los identificadores de contexto, vea los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="45303-108">For more information about context handles, see the following attributes:</span></span>

-   [<span data-ttu-id="45303-109">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="45303-109">**context\_handle**</span></span>](context-handle.md)
-   [<span data-ttu-id="45303-110">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="45303-110">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
-   [<span data-ttu-id="45303-111">**identificador de contexto de \_ \_ noserialización**</span><span class="sxs-lookup"><span data-stu-id="45303-111">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)

<span data-ttu-id="45303-112">Las capacidades de acceso de modo de uso compartido y en serie son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores).</span><span class="sxs-lookup"><span data-stu-id="45303-112">Serialized and shared mode access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="45303-113">Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="45303-113">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="45303-114">Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados.</span><span class="sxs-lookup"><span data-stu-id="45303-114">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="45303-115">El uso de un identificador de contexto en modo mixto puede mejorar considerablemente la escalabilidad de un servidor, especialmente cuando varios subprocesos realizan llamadas simultáneas al mismo identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="45303-115">Using a context handle in mixed mode can substantially improve the scalability of a server, especially when multiple threads make simultaneous calls to the same context handle.</span></span>

<span data-ttu-id="45303-116">RPC no exige "bloqueo de escritura" en los métodos que usan un identificador de contexto en modo compartido, lo que significa que las aplicaciones deben asegurarse de que los identificadores de contexto del modo compartido no se modifiquen.</span><span class="sxs-lookup"><span data-stu-id="45303-116">RPC does not enforce "write lock" on methods using a context handle in shared mode, which means applications must ensure that shared mode context handles are not modified.</span></span> <span data-ttu-id="45303-117">La modificación de un identificador de contexto que se usa en modo compartido puede dar lugar a daños sutiles en el contenido de los identificadores de contexto, que son imposibles de depurar.</span><span class="sxs-lookup"><span data-stu-id="45303-117">Modification of a context handle used in shared mode can result in subtle corruptions of context handle contents, which are impossible to debug.</span></span>

<span data-ttu-id="45303-118">El cambio de la lógica de serialización de un identificador de contexto solo afecta al servidor.</span><span class="sxs-lookup"><span data-stu-id="45303-118">Changing the serialization logic of a context handle affects only the server.</span></span> <span data-ttu-id="45303-119">Además, el cambio de la lógica de serialización de un identificador de contexto no afecta al formato de conexión y, por lo tanto, los cambios en la lógica de serialización en un servidor no afectan a la capacidad de los clientes existentes para interactuar con el servidor.</span><span class="sxs-lookup"><span data-stu-id="45303-119">Also, changing the serialization logic of a context handle does not affect the wire format, and therefore, changes to serialization logic on a server do not affect existing clients' capability to interact with the server.</span></span>

<span data-ttu-id="45303-120">No se recomienda usar solo identificadores de contexto no serializados.</span><span class="sxs-lookup"><span data-stu-id="45303-120">Using only nonserialized context handles is not recommended.</span></span> <span data-ttu-id="45303-121">Los servidores que usan identificadores no serializados deben cambiar al acceso serializado para el método que cierra el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="45303-121">Servers that use nonserialized handles are should switch to serialized access for the method that closes the context handle.</span></span>

<span data-ttu-id="45303-122">\[ \] Los métodos de creación suelen usar identificadores de contexto que no son de solo uso y no requieren ninguna serialización.</span><span class="sxs-lookup"><span data-stu-id="45303-122">Context handles that are \[out\]-only are typically used by creation methods, and do not require any serialization.</span></span> <span data-ttu-id="45303-123">Por lo tanto, el atributo de serialización que se aplica a los \[ \] identificadores de contexto de solo salida, como [**\_ \_ serializar identificador**](context-handle-serialize.md) de contexto o [**identificador de contexto \_ \_ noserialización**](context-handle-noserialize.md), lo omite RPC.</span><span class="sxs-lookup"><span data-stu-id="45303-123">Therefore, any serialization attribute applied to \[out\]-only context handles, such as [**context\_handle\_serialize**](context-handle-serialize.md) or [**context\_handle\_noserialize**](context-handle-noserialize.md), is ignored by RPC.</span></span>

> [!Note]  
> <span data-ttu-id="45303-124">Los métodos de creación se serializan implícitamente.</span><span class="sxs-lookup"><span data-stu-id="45303-124">Creation methods are implicitly serialized.</span></span>

 

## <a name="examples"></a><span data-ttu-id="45303-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="45303-125">Examples</span></span>

<span data-ttu-id="45303-126">Los dos ejemplos siguientes muestran cómo habilitar la serialización en modo mixto de identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="45303-126">The following two examples show how to enable mixed mode serialization of context handles.</span></span>

<span data-ttu-id="45303-127">En el primer ejemplo se muestra cómo hacerlo en el archivo IDL:</span><span class="sxs-lookup"><span data-stu-id="45303-127">The first example shows how to do so in the IDL file:</span></span>

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

<span data-ttu-id="45303-128">En el segundo ejemplo se muestra cómo habilitar la serialización en modo mixto de identificadores de contexto en el archivo ACF:</span><span class="sxs-lookup"><span data-stu-id="45303-128">The second example shows how to enable mixed mode serialization of context handles in the ACF file:</span></span>

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a><span data-ttu-id="45303-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45303-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45303-130">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="45303-130">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="45303-131">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="45303-131">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="45303-132">**identificador de contexto de \_ \_ noserialización**</span><span class="sxs-lookup"><span data-stu-id="45303-132">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> </dl>

 

 




