---
title: Atributo ncalrpc
description: La palabra clave ncalrpc identifica la comunicación entre procesos local como la familia de protocolos para el punto de conexión. Esta palabra clave es uno de los nombres de familia de protocolo válidos que se deben usar con el atributo \endpoint\.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- MidL del atributo ncalrpc
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5d22b572eb9ad2f2e46b029ec242b48d5cd684
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386884"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="cb43b-105">Atributo ncalrpc</span><span class="sxs-lookup"><span data-stu-id="cb43b-105">ncalrpc attribute</span></span>

<span data-ttu-id="cb43b-106">La **palabra clave ncalrpc** identifica la comunicación entre procesos local como la familia de protocolos para el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="cb43b-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="cb43b-107">Esta palabra clave es uno de los nombres de familia de protocolo válidos que se deben usar con el atributo **\[** [**de punto de**](endpoint.md) **\]** conexión.</span><span class="sxs-lookup"><span data-stu-id="cb43b-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="cb43b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb43b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb43b-109">*port-name*</span><span class="sxs-lookup"><span data-stu-id="cb43b-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cb43b-110">Cadena de caracteres que especifica el puerto de comunicación (una aplicación, un servicio o una instancia de un servicio) que un cliente usa para realizar llamadas entre procesos a un servidor.</span><span class="sxs-lookup"><span data-stu-id="cb43b-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="cb43b-111">La cadena puede contener hasta 53 caracteres y no debe contener caracteres de barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="cb43b-111">The string can contain up to 53 characters and should not contain any backslash (\\) characters.</span></span> <span data-ttu-id="cb43b-112">El nombre del equipo no debe usarse con la **palabra clave ncalrpc.**</span><span class="sxs-lookup"><span data-stu-id="cb43b-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb43b-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb43b-113">Remarks</span></span>

<span data-ttu-id="cb43b-114">La sintaxis de la cadena de puerto de interproceso-comunicación local, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL.</span><span class="sxs-lookup"><span data-stu-id="cb43b-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="cb43b-115">El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="cb43b-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="cb43b-116">Algunas clases de errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="cb43b-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="cb43b-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cb43b-117">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="cb43b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb43b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb43b-119">**Extremo**</span><span class="sxs-lookup"><span data-stu-id="cb43b-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="cb43b-120">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="cb43b-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="cb43b-121">**ncacn \_ en \_ dsp**</span><span class="sxs-lookup"><span data-stu-id="cb43b-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="cb43b-122">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="cb43b-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="cb43b-123">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="cb43b-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="cb43b-124">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="cb43b-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="cb43b-125">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="cb43b-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="cb43b-126">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="cb43b-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="cb43b-127">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="cb43b-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="cb43b-128">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="cb43b-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="cb43b-129">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="cb43b-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="cb43b-130">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="cb43b-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="cb43b-131">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="cb43b-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="cb43b-132">Enlace de cadena</span><span class="sxs-lookup"><span data-stu-id="cb43b-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 