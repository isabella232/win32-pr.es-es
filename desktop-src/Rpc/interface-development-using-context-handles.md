---
title: Desarrollo de interfaces con identificadores de contexto
description: Normalmente, se crea un identificador de contexto especificando el atributo \ context \_ Handle \ en una definición de tipo en el archivo IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793132"
---
# <a name="interface-development-using-context-handles"></a><span data-ttu-id="70c67-103">Desarrollo de interfaces con identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="70c67-103">Interface Development Using Context Handles</span></span>

<span data-ttu-id="70c67-104">Normalmente, se crea un identificador de contexto al especificar el \[ atributo de [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) \] en una definición de tipo en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="70c67-104">Typically, you create a context handle by specifying the \[[**context\_handle**](/windows/desktop/Midl/context-handle)\] attribute on a type definition in the IDL file.</span></span> <span data-ttu-id="70c67-105">La definición de tipo también especifica implícitamente una rutina de ejecución de contexto que debe proporcionar.</span><span class="sxs-lookup"><span data-stu-id="70c67-105">The type definition also implicitly specifies a context run-down routine, which you must provide.</span></span> <span data-ttu-id="70c67-106">Si se interrumpe la comunicación entre el cliente y el servidor, el tiempo de ejecución del servidor invoca esta rutina para realizar cualquier limpieza necesaria.</span><span class="sxs-lookup"><span data-stu-id="70c67-106">If communication between the client and server breaks down, the server run time invokes this routine to perform any needed cleanup.</span></span> <span data-ttu-id="70c67-107">Para obtener más información sobre las rutinas de ejecución de contexto, vea [rutina de ejecución de contexto de servidor](server-context-run-down-routine.md).</span><span class="sxs-lookup"><span data-stu-id="70c67-107">For more information on context run-down routines, see [Server Context Run-down Routine](server-context-run-down-routine.md).</span></span>

<span data-ttu-id="70c67-108">Una interfaz que utiliza un identificador de contexto debe tener un identificador de enlace para el enlace inicial, que tiene que tener lugar antes de que el servidor pueda devolver un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="70c67-108">An interface that uses a context handle must have a binding handle for the initial binding, which has to take place before the server can return a context handle.</span></span> <span data-ttu-id="70c67-109">Puede usar un identificador de enlace automático, implícito o explícito para crear el enlace y establecer el contexto.</span><span class="sxs-lookup"><span data-stu-id="70c67-109">You can use an automatic, implicit, or explicit binding handle to create the binding and establish the context.</span></span>

<span data-ttu-id="70c67-110">Un identificador de contexto debe ser del [**tipo \* void**](/windows/desktop/Midl/void) o un tipo que se resuelva como [**void \***](/windows/desktop/Midl/void).</span><span class="sxs-lookup"><span data-stu-id="70c67-110">A context handle must be of the [**void \***](/windows/desktop/Midl/void) type, or a type that resolves to [**void \***](/windows/desktop/Midl/void).</span></span> <span data-ttu-id="70c67-111">El programa de servidor lo convierte al tipo requerido.</span><span class="sxs-lookup"><span data-stu-id="70c67-111">The server program casts it to the required type.</span></span>

> [!Note]  
> <span data-ttu-id="70c67-112">Se desaconseja el uso de \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] para los parámetros de identificador de contexto, excepto para las rutinas que cierran los identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="70c67-112">The use of \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] for context handle parameters is discouraged except for routines that close context handles.</span></span> <span data-ttu-id="70c67-113">Si los parámetros de control de contexto marcados \[ [**en**](/windows/desktop/Midl/in), [](/windows/desktop/Midl/out-idl) \] se usan out, no pase un identificador de contexto **nulo** o no inicializado desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="70c67-113">If context handles parameters marked \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] are used, do not pass a **NULL** or uninitialized context handle from the client to the server.</span></span> <span data-ttu-id="70c67-114">En su lugar, se debe pasar un puntero **null** a un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="70c67-114">A **NULL** pointer to a context handle should be passed instead.</span></span> <span data-ttu-id="70c67-115">Tenga en cuenta que los parámetros de identificador de contexto marcados \[ [**en**](/windows/desktop/Midl/in) \] no aceptan punteros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="70c67-115">Please note, context handle parameters marked \[[**in**](/windows/desktop/Midl/in)\] do not accept **NULL** pointers.</span></span>

 

<span data-ttu-id="70c67-116">En el fragmento siguiente de una definición de interfaz de ejemplo se muestra cómo una aplicación distribuida puede usar un identificador de contexto para que un servidor abra y actualice un archivo de datos para cada cliente.</span><span class="sxs-lookup"><span data-stu-id="70c67-116">The following fragment of a sample interface definition shows how a distributed application can use a context handle to have a server open and update a data file for each client.</span></span>

<span data-ttu-id="70c67-117">La interfaz debe contener una llamada a procedimiento remoto para inicializar el identificador y establecerlo en un valor distinto de **null** .</span><span class="sxs-lookup"><span data-stu-id="70c67-117">The interface must contain a remote procedure call to initialize the handle and set it to a non-**null** value.</span></span> <span data-ttu-id="70c67-118">En este ejemplo, la función RemoteOpen realiza esta operación.</span><span class="sxs-lookup"><span data-stu-id="70c67-118">In this example, the RemoteOpen function performs this operation.</span></span> <span data-ttu-id="70c67-119">Especifica el identificador de contexto con un \[ [](/windows/desktop/Midl/out-idl) \] atributo direccional out.</span><span class="sxs-lookup"><span data-stu-id="70c67-119">It specifies the context handle with an \[[**out**](/windows/desktop/Midl/out-idl)\] directional attribute.</span></span> <span data-ttu-id="70c67-120">Como alternativa, podría devolver el identificador de contexto como el valor devuelto del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="70c67-120">Alternatively, you could return the context handle as the procedure's return value.</span></span> <span data-ttu-id="70c67-121">Sin embargo, en este ejemplo, pasaremos el controlador de contexto a través de la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="70c67-121">However in this example, we'll pass the context handle out through the parameter list.</span></span>

<span data-ttu-id="70c67-122">En este ejemplo, la información de contexto es un identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="70c67-122">In this example, the context information is a file handle.</span></span> <span data-ttu-id="70c67-123">Realiza un seguimiento de la ubicación actual en el archivo.</span><span class="sxs-lookup"><span data-stu-id="70c67-123">It keeps track of the current location in the file.</span></span> <span data-ttu-id="70c67-124">La interfaz empaqueta el identificador de archivo como un identificador de contexto y lo pasa como un parámetro a las llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="70c67-124">The interface packages the file handle as a context handle and passes it as a parameter to remote procedure calls.</span></span> <span data-ttu-id="70c67-125">Una estructura contiene el nombre de archivo y el identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="70c67-125">A structure contains the file name and the file handle.</span></span>

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

<span data-ttu-id="70c67-126">La función RemoteOpen crea un identificador de contexto válido y no **nulo** .</span><span class="sxs-lookup"><span data-stu-id="70c67-126">The RemoteOpen function creates a valid, non-**null** context handle.</span></span> <span data-ttu-id="70c67-127">Pasa el identificador de contexto al cliente.</span><span class="sxs-lookup"><span data-stu-id="70c67-127">It passes the context handle to the client.</span></span> <span data-ttu-id="70c67-128">Las llamadas a procedimientos remotos posteriores, como RemoteRead, usan el identificador de contexto como un puntero in.</span><span class="sxs-lookup"><span data-stu-id="70c67-128">Subsequent remote procedure calls, such as RemoteRead, use the context handle as an in pointer.</span></span>

<span data-ttu-id="70c67-129">Además del procedimiento remoto que inicializa el identificador de contexto, la interfaz debe contener un procedimiento que libere el contexto del servidor y establezca el identificador de contexto en **null**.</span><span class="sxs-lookup"><span data-stu-id="70c67-129">In addition to the remote procedure that initializes the context handle, the interface must contain a procedure that frees the server context and sets context handle to **NULL**.</span></span> <span data-ttu-id="70c67-130">En el ejemplo anterior, la función RemoteClose realiza esta operación.</span><span class="sxs-lookup"><span data-stu-id="70c67-130">In the preceding example, the RemoteClose function performs this operation.</span></span>

 

 