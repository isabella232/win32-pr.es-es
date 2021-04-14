---
title: atributo Message
description: El atributo \ Message \ indica que la llamada a procedimiento remoto se tratará como un mensaje desde el cliente al servidor.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- atributo de mensaje MIDL
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487631"
---
# <a name="message-attribute"></a><span data-ttu-id="cce01-104">atributo Message</span><span class="sxs-lookup"><span data-stu-id="cce01-104">message attribute</span></span>

<span data-ttu-id="cce01-105">El atributo **\[ Message \]** indica que la llamada a procedimiento remoto se tratará como un mensaje desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="cce01-105">The **\[message\]** attribute indicates that the remote procedure call is to be treated as a message from the client to the server.</span></span>

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="cce01-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cce01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce01-107">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="cce01-107">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="cce01-108">Otros atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="cce01-108">Other attributes that apply to the function.</span></span> <span data-ttu-id="cce01-109">Solo **\[** [](local.md) **\]** **\[** se pueden usar los atributos local, [**nocode**](nocode.md) **\]** , **\[** [**code**](code.md)**\]** y **\[** [**Optimize**](optimize.md) **\]** con el atributo **\[ Message \]** .</span><span class="sxs-lookup"><span data-stu-id="cce01-109">Only the **\[**[**local**](local.md)**\]**, **\[**[**nocode**](nocode.md)**\]**, **\[**[**code**](code.md)**\],** and **\[**[**optimize**](optimize.md)**\]** attributes may be used with the **\[message\]** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="cce01-110">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="cce01-110">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cce01-111">Nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="cce01-111">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="cce01-112">*opcional-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="cce01-112">*optional-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="cce01-113">Cero o más atributos de MIDL que se aplicarán al parámetro.</span><span class="sxs-lookup"><span data-stu-id="cce01-113">Zero or more MIDL attributes that will be applied to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cce01-114">*param: nombre*</span><span class="sxs-lookup"><span data-stu-id="cce01-114">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cce01-115">Nombre del parámetro tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="cce01-115">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cce01-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cce01-116">Remarks</span></span>

<span data-ttu-id="cce01-117">Como mensajes del cliente, las llamadas a procedimientos remotos con el atributo **\[ Message \]** se entregan al servidor de forma asincrónica a través del transporte de cola de mensajes de [**ncadg \_ MQ**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="cce01-117">As messages from the client, remote procedure calls with the **\[message\]** attribute are delivered to the server asynchronously over the [**ncadg\_mq**](ncadg-mq.md) message-queuing transport.</span></span> <span data-ttu-id="cce01-118">Puede indicar la mensajería de modo sincrónico especificando el protocolo de **transporte \_ MQ ncadg** sin usar el atributo **\[ Message \]** .</span><span class="sxs-lookup"><span data-stu-id="cce01-118">You can indicate synchronous-mode messaging by specifying the **ncadg\_mq** transport protocol without using the **\[message\]** attribute.</span></span>

<span data-ttu-id="cce01-119">Al especificar la mensajería de modo asincrónico, el atributo de **\[ mensaje \]** permite al cliente realizar la llamada a procedimiento remoto y volver inmediatamente, incluso cuando la aplicación de servidor no responde.</span><span class="sxs-lookup"><span data-stu-id="cce01-119">By specifying asynchronous-mode messaging, the **\[message\]** attribute allows the client to make the remote procedure call and return immediately, even when the server application is not responding.</span></span> <span data-ttu-id="cce01-120">Si el servidor de destino no está disponible, la llamada se almacenará hasta que el servidor esté disponible.</span><span class="sxs-lookup"><span data-stu-id="cce01-120">If the target server is not available, the call will be stored until the server becomes available.</span></span>

<span data-ttu-id="cce01-121">Además, la mensajería de modo asincrónico le permite controlar las propiedades de la cola de mensajes de la cola de recepción del servidor.</span><span class="sxs-lookup"><span data-stu-id="cce01-121">In addition, asynchronous-mode messaging lets you control message-queue properties of the receive queue for the server.</span></span> <span data-ttu-id="cce01-122">Vea [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) para obtener más información sobre cómo seleccionar la calidad de servicio, la prioridad de llamada y la duración de la llamada para el proceso de servidor.</span><span class="sxs-lookup"><span data-stu-id="cce01-122">See [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) for more information on selecting quality of service, call priority, and call lifetime for the server process.</span></span>

<span data-ttu-id="cce01-123">Las restricciones siguientes también se aplican al atributo **\[ Message \]** :</span><span class="sxs-lookup"><span data-stu-id="cce01-123">The following restrictions also apply to the **\[message\]** attribute:</span></span>

-   <span data-ttu-id="cce01-124">Microsoft Message Queuing debe implementarse en los sistemas cliente y servidor, y los sistemas deben ser visibles entre sí según lo determinado por el ámbito de la instalación de la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cce01-124">Microsoft Message Queuing must be implemented in the client and server systems and the systems must be visible to each other as determined by the scope of the message queue installation.</span></span>
-   <span data-ttu-id="cce01-125">El enlace debe usar puntos de conexión conocidos y el protocolo de transporte [**\_ MQ de ncadg**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="cce01-125">The binding must use well-known endpoints and the [**ncadg\_mq**](ncadg-mq.md) transport protocol.</span></span>
-   <span data-ttu-id="cce01-126">La función no puede contener parámetros de salida ni un tipo de valor devuelto distinto de [**void**](void.md).</span><span class="sxs-lookup"><span data-stu-id="cce01-126">The function cannot contain output parameters or a return type other than [**void**](void.md).</span></span> <span data-ttu-id="cce01-127">Tenga en cuenta que la última restricción hace que el atributo de **\[ mensaje \]** no sea adecuado para los métodos de interfaz com (objeto), en este momento.</span><span class="sxs-lookup"><span data-stu-id="cce01-127">Note that the latter restriction makes the **\[message\]** attribute unsuitable for COM (object) interface methods, at this time.</span></span> <span data-ttu-id="cce01-128">La siguiente versión de MIDL permitirá que las funciones de **\[ mensaje \]** devuelvan el estado de error \_ \_ t o HRESULT.</span><span class="sxs-lookup"><span data-stu-id="cce01-128">The next release of MIDL will permit **\[message\]** functions to return error\_status\_t or HRESULT.</span></span>
-   <span data-ttu-id="cce01-129">Cualquier interfaz que contenga al menos una llamada de **\[ mensaje \]** se debe registrar llamando a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) antes de llamar a [**RpcServerUseProtseqEpEx (ncadg \_ MQ)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span><span class="sxs-lookup"><span data-stu-id="cce01-129">Any interface that contains at least one **\[message\]** call must be registered by calling [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) or [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) before calling [**RpcServerUseProtseqEpEx(ncadg\_mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span></span> <span data-ttu-id="cce01-130">De lo contrario, las llamadas que estaban esperando en la cola del servidor se leerán antes de que se registre la interfaz y se producirá un error en las llamadas.</span><span class="sxs-lookup"><span data-stu-id="cce01-130">Otherwise, calls that were waiting on the queue for the server will be read before the interface is registered, and the calls will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="cce01-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cce01-131">Examples</span></span>

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a><span data-ttu-id="cce01-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="cce01-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce01-133">**codifica**</span><span class="sxs-lookup"><span data-stu-id="cce01-133">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="cce01-134">**localizar**</span><span class="sxs-lookup"><span data-stu-id="cce01-134">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="cce01-135">**ncadg \_ MQ**</span><span class="sxs-lookup"><span data-stu-id="cce01-135">**ncadg\_mq**</span></span>](ncadg-mq.md)
</dt> <dt>

[<span data-ttu-id="cce01-136">**nocode**</span><span class="sxs-lookup"><span data-stu-id="cce01-136">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="cce01-137">**optimiz**</span><span class="sxs-lookup"><span data-stu-id="cce01-137">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="cce01-138">Message Queue Server de RPC</span><span class="sxs-lookup"><span data-stu-id="cce01-138">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="cce01-139">**RpcBindingSetOption**</span><span class="sxs-lookup"><span data-stu-id="cce01-139">**RpcBindingSetOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="cce01-140">**RpcBindingInqOption**</span><span class="sxs-lookup"><span data-stu-id="cce01-140">**RpcBindingInqOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="cce01-141">**void**</span><span class="sxs-lookup"><span data-stu-id="cce01-141">**void**</span></span>](void.md)
</dt> </dl>

 

 