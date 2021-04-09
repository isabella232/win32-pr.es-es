---
title: atributo ncalrpc
description: La palabra clave ncalrpc identifica la comunicación entre procesos locales como la familia de protocolos para el punto de conexión. Esta palabra clave es uno de los nombres de familia de protocolos válidos que se deben usar con el atributo \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- ncalrpc (atributo) MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995221"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="e02dc-105">atributo ncalrpc</span><span class="sxs-lookup"><span data-stu-id="e02dc-105">ncalrpc attribute</span></span>

<span data-ttu-id="e02dc-106">La palabra clave **ncalrpc** identifica la comunicación entre procesos locales como la familia de protocolos para el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="e02dc-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="e02dc-107">Esta palabra clave es uno de los nombres de familia de protocolos válidos que se deben usar con el atributo de **\[** [**extremo**](endpoint.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e02dc-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="e02dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e02dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e02dc-109">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="e02dc-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e02dc-110">Cadena de caracteres que especifica el puerto de comunicación (una aplicación, un servicio o una instancia de un servicio) que un cliente usa para realizar llamadas entre procesos a un servidor.</span><span class="sxs-lookup"><span data-stu-id="e02dc-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="e02dc-111">La cadena puede contener hasta 53 caracteres y no debe contener ninguna barra diagonal inversa ( \) caracteres).</span><span class="sxs-lookup"><span data-stu-id="e02dc-111">The string can contain up to 53 characters and should not contain any backslash (\) characters.</span></span> <span data-ttu-id="e02dc-112">El nombre del equipo no se debe utilizar con la palabra clave **ncalrpc** .</span><span class="sxs-lookup"><span data-stu-id="e02dc-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e02dc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e02dc-113">Remarks</span></span>

<span data-ttu-id="e02dc-114">La sintaxis de la cadena de puerto de comunicación entre procesos local, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL.</span><span class="sxs-lookup"><span data-stu-id="e02dc-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="e02dc-115">El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="e02dc-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="e02dc-116">Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="e02dc-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="e02dc-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e02dc-117">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="e02dc-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e02dc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e02dc-119">**finales**</span><span class="sxs-lookup"><span data-stu-id="e02dc-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="e02dc-120">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="e02dc-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e02dc-121">**ncacn \_ en \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="e02dc-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="e02dc-122">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="e02dc-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="e02dc-123">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="e02dc-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="e02dc-124">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="e02dc-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="e02dc-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="e02dc-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="e02dc-126">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="e02dc-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="e02dc-127">**\_TCP NB \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="e02dc-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="e02dc-128">**NP de ncacn \_**</span><span class="sxs-lookup"><span data-stu-id="e02dc-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="e02dc-129">**ncacn \_ redes virtuales \_ spp**</span><span class="sxs-lookup"><span data-stu-id="e02dc-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="e02dc-130">**ncadg \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="e02dc-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="e02dc-131">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="e02dc-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="e02dc-132">Enlace de cadenas</span><span class="sxs-lookup"><span data-stu-id="e02dc-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 