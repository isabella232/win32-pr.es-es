---
title: difundir atributo
description: La palabra clave \ Broadcast \ especifica que las llamadas a procedimientos remotos se envíen a todos los servidores de una red local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- difundir atributo MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358211"
---
# <a name="broadcast-attribute"></a><span data-ttu-id="422df-104">difundir atributo</span><span class="sxs-lookup"><span data-stu-id="422df-104">broadcast attribute</span></span>

<span data-ttu-id="422df-105">La palabra clave **\[ Broadcast \]** especifica que las llamadas a procedimientos remotos se envían a todos los servidores de una red local.</span><span class="sxs-lookup"><span data-stu-id="422df-105">The keyword **\[broadcast\]** specifies that remote procedure calls be sent to all servers on a local network.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="422df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="422df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="422df-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="422df-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="422df-108">Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="422df-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="422df-109">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="422df-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="422df-110">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="422df-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="422df-111">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="422df-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="422df-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="422df-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="422df-113">Especifica los atributos adicionales que se van a aplicar a la función.</span><span class="sxs-lookup"><span data-stu-id="422df-113">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="422df-114">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="422df-114">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="422df-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="422df-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="422df-116">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="422df-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="422df-117">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="422df-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="422df-118">Especifica el nombre de la función a la que se aplicará el atributo de **\[ difusión \]** .</span><span class="sxs-lookup"><span data-stu-id="422df-118">Specifies the name of the function to which the **\[broadcast\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="422df-119">*params*</span><span class="sxs-lookup"><span data-stu-id="422df-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="422df-120">Lista de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="422df-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="422df-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="422df-121">Remarks</span></span>

<span data-ttu-id="422df-122">La palabra clave **\[ Broadcast \]** especifica que la rutina siempre se difunde a todos los servidores de la red, en lugar de entregarse a un servidor determinado. El cliente recibe la salida de la primera respuesta para que se devuelva correctamente, mientras que las respuestas subsiguientes se descartan.</span><span class="sxs-lookup"><span data-stu-id="422df-122">The **\[broadcast\]** keyword specifies that the routine is always broadcasted to all the servers on the network, rather than being delivered to one particular server.The client receives output from the first reply to return successfully, while subsequent replies are discarded.</span></span>

<span data-ttu-id="422df-123">Una operación con el atributo **\[ Broadcast \]** es implícitamente una operación [**\[ idempotente \]**](idempotent.md) .</span><span class="sxs-lookup"><span data-stu-id="422df-123">An operation with the **\[broadcast\]** attribute is implicitly an [**\[idempotent\]**](idempotent.md) operation.</span></span> <span data-ttu-id="422df-124">Sin embargo, el atributo **\[ Broadcast \]** especifica propiedades adicionales que funcionan con el atributo **\[ idempotente \]** .</span><span class="sxs-lookup"><span data-stu-id="422df-124">However, the **\[broadcast\]** attribute specifies additional properties that functions with the **\[idempotent\]** attribute don't have.</span></span> <span data-ttu-id="422df-125">En concreto, las funciones que usan el atributo **\[ Broadcast \]** especifican que se puede llamar varias veces a la rutina como resultado de una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="422df-125">Specifically, functions using the **\[broadcast\]** attribute specify that the routine can be called multiple times as the result of one remote procedure call.</span></span> <span data-ttu-id="422df-126">Al mismo tiempo, se pueden enviar a varios servidores.</span><span class="sxs-lookup"><span data-stu-id="422df-126">At the same time, they can be sent to multiple servers.</span></span> <span data-ttu-id="422df-127">Esto es diferente del atributo **\[ idempotente \]** , que especifica solo que se puede reintentar una llamada si no se completa.</span><span class="sxs-lookup"><span data-stu-id="422df-127">This is different from the **\[idempotent\]** attribute, which specifies only that a call can be retried if it is not completed.</span></span>

<span data-ttu-id="422df-128">Si un procedimiento remoto difunde su llamada a todos los hosts de una red local, debe usar la secuencia de protocolo [**\_ \_ UDP de ncadg**](ncadg-ip-udp.md) o [**ncadg \_**](ncadg-ipx.md) IP.</span><span class="sxs-lookup"><span data-stu-id="422df-128">If a remote procedure broadcasts its call to all hosts on a local network, it must use either the [**ncadg\_ip\_udp**](ncadg-ip-udp.md) or the [**ncadg\_ipx**](ncadg-ipx.md) protocol sequence.</span></span> <span data-ttu-id="422df-129">Tenga en cuenta que el servicio de datagramas determina el tamaño de un paquete de **\[ difusión \]** .</span><span class="sxs-lookup"><span data-stu-id="422df-129">Note that the size of a **\[broadcast\]** packet is determined by the datagram service in use.</span></span>

## <a name="see-also"></a><span data-ttu-id="422df-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="422df-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422df-131">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="422df-131">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="422df-132">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="422df-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="422df-133">**incluso**</span><span class="sxs-lookup"><span data-stu-id="422df-133">**maybe**</span></span>](maybe.md)
</dt> <dt>

[<span data-ttu-id="422df-134">**ncadg \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="422df-134">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="422df-135">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="422df-135">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> </dl>

 

 




