---
title: RPC_BINDING_HANDLE (Rpcdce. h)
description: El \_ tipo de datos de identificador de enlace RPC declara un identificador de enlace que contiene información que la biblioteca en tiempo de ejecución de RPC utiliza para obtener acceso a la información de enlace.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803992"
---
# <a name="rpc_binding_handle"></a><span data-ttu-id="7ed0f-104">\_identificador de enlace RPC \_</span><span class="sxs-lookup"><span data-stu-id="7ed0f-104">RPC\_BINDING\_HANDLE</span></span>

<span data-ttu-id="7ed0f-105">El tipo de datos de **\_ identificador de enlace RPC** declara un identificador de enlace que contiene información que la biblioteca en tiempo de ejecución de RPC utiliza para obtener acceso a la información de enlace.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-105">The **RPC\_BINDING HANDLE** data type declares a binding handle containing information that the RPC run-time library uses to access binding information.</span></span>


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="7ed0f-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ed0f-106">Remarks</span></span>

<span data-ttu-id="7ed0f-107">La biblioteca en tiempo de ejecución utiliza la información de enlace para establecer una relación cliente-servidor que permite la ejecución de llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-107">The run-time library uses binding information to establish a client-server relationship that allows the execution of remote procedure calls.</span></span> <span data-ttu-id="7ed0f-108">En función del contexto en el que se crea un identificador de enlace, se considera un identificador de enlace de servidor o un identificador de enlace del cliente.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-108">Based on the context in which a binding handle is created, it is considered a server-binding handle or a client-binding handle.</span></span>

<span data-ttu-id="7ed0f-109">Un identificador de enlace de servidor contiene la información necesaria para que un cliente establezca una relación con un servidor específico.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-109">A server-binding handle contains the information necessary for a client to establish a relationship with a specific server.</span></span> <span data-ttu-id="7ed0f-110">Cualquier número de rutinas en tiempo de ejecución de la API de RPC devuelve un identificador de enlace de servidor que se puede utilizar para realizar una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-110">Any number of RPC API run-time routines return a server-binding handle that can be used for making a remote procedure call.</span></span>

<span data-ttu-id="7ed0f-111">No se puede usar un identificador de enlace de cliente para realizar una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-111">A client-binding handle cannot be used to make a remote procedure call.</span></span> <span data-ttu-id="7ed0f-112">La biblioteca en tiempo de ejecución de RPC crea y proporciona un identificador de enlace de cliente a un procedimiento llamado-Server (también denominado rutina del administrador de servidores) como \_ parámetro de identificador de enlace RPC \_ .</span><span class="sxs-lookup"><span data-stu-id="7ed0f-112">The RPC run-time library creates and provides a client-binding handle to a called-server procedure (also called a server-manager routine) as the RPC\_BINDING\_HANDLE parameter.</span></span> <span data-ttu-id="7ed0f-113">El identificador de enlace de cliente contiene información sobre el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-113">The client-binding handle contains information about the calling client.</span></span>

<span data-ttu-id="7ed0f-114">Las funciones \*\* \* RpcBinding\* _ _*y \* RpcNsBinding*_ devuelven el código \_ de estado RPC S \_ \_ tipo incorrecto \_ de \_ enlace cuando una aplicación proporciona el tipo de identificador de enlace incorrecto.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-114">The **RpcBinding\** _ and _*RpcNsBinding\*\*_ functions return the status code RPC\_S\_WRONG\_KIND\_OF\_BINDING when an application provides the incorrect binding-handle type.</span></span>

<span data-ttu-id="7ed0f-115">Una aplicación puede compartir un único identificador de enlace entre varios subprocesos de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-115">An application can share a single binding handle across multiple threads of execution.</span></span> <span data-ttu-id="7ed0f-116">La biblioteca en tiempo de ejecución de RPC administra llamadas a procedimientos remotos simultáneas que usan un único identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-116">The RPC run-time library manages concurrent remote procedure calls that use a single binding handle.</span></span> <span data-ttu-id="7ed0f-117">Sin embargo, la aplicación es responsable de enlazar el control de simultaneidad para las operaciones que modifican un identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-117">However, the application is responsible for binding handle concurrency control for operations that modify a binding handle.</span></span> <span data-ttu-id="7ed0f-118">Estas operaciones incluyen las siguientes rutinas:</span><span class="sxs-lookup"><span data-stu-id="7ed0f-118">These operations include the following routines:</span></span>

-   [<span data-ttu-id="7ed0f-119">_ *RpcBindingFree*\*</span><span class="sxs-lookup"><span data-stu-id="7ed0f-119">_ *RpcBindingFree*\*</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [<span data-ttu-id="7ed0f-120">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="7ed0f-120">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [<span data-ttu-id="7ed0f-121">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="7ed0f-121">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [<span data-ttu-id="7ed0f-122">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="7ed0f-122">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

<span data-ttu-id="7ed0f-123">Por ejemplo, si una aplicación comparte un identificador de enlace entre dos subprocesos de ejecución y restablece el punto de conexión de controlador de enlace en uno de los subprocesos llamando a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-123">For example, if an application shares a binding handle across two threads of execution and resets the binding-handle endpoint in one of the threads by calling [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), the results are undefined.</span></span> <span data-ttu-id="7ed0f-124">También se puede restablecer el controlador de enlace en el otro subproceso o se puede producir un error en la operación o se puede bloquear el proceso.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-124">The binding handle on the other thread may also be reset, or the operation may fail, or the process may crash.</span></span> <span data-ttu-id="7ed0f-125">Un error común es liberar un identificador de enlace mientras se está realizando una llamada en él. Normalmente, Esto bloquea el proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-125">A common error is freeing a binding handle while a call on it is in progress; this usually crashes the calling process.</span></span>

<span data-ttu-id="7ed0f-126">Si no desea la simultaneidad, puede diseñar una aplicación para crear una copia de un identificador de enlace mediante una llamada a [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span><span class="sxs-lookup"><span data-stu-id="7ed0f-126">If you do not want concurrency, you can design an application to create a copy of a binding handle by calling [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span></span> <span data-ttu-id="7ed0f-127">En este caso, una operación al primer identificador de enlace no tiene ningún efecto en el segundo controlador de enlace.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-127">In this case, an operation to the first binding handle has no effect on the second binding handle.</span></span>

<span data-ttu-id="7ed0f-128">Las rutinas que requieren un identificador de enlace como parámetro muestran un tipo de datos de **\_ \_ identificador de enlace de RPC**.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-128">Routines requiring a binding handle as a parameter show a data type of **RPC\_BINDING\_HANDLE**.</span></span> <span data-ttu-id="7ed0f-129">Los parámetros de identificador de enlace se pasan por valor.</span><span class="sxs-lookup"><span data-stu-id="7ed0f-129">Binding-handle parameters are passed by value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed0f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ed0f-130">Requirements</span></span>



| <span data-ttu-id="7ed0f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ed0f-131">Requirement</span></span> | <span data-ttu-id="7ed0f-132">Value</span><span class="sxs-lookup"><span data-stu-id="7ed0f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed0f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ed0f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed0f-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7ed0f-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7ed0f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ed0f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed0f-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ed0f-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ed0f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ed0f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed0f-138"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ed0f-138"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





