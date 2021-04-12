---
title: ncadg_ip_udp atributo)
description: La \_ \_ palabra clave UDP de IP de ncadg identifica la versión de DATAGRAMA de TCP/IP como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp el atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149218"
---
# <a name="ncadg_ip_udp-attribute"></a><span data-ttu-id="35859-105">\_atributo UDP de IP ncadg \_</span><span class="sxs-lookup"><span data-stu-id="35859-105">ncadg\_ip\_udp attribute</span></span>

<span data-ttu-id="35859-106">La palabra clave **\_ \_ UDP de IP de ncadg** identifica la versión de DATAGRAMA de TCP/IP como la familia de protocolos para el extremo.</span><span class="sxs-lookup"><span data-stu-id="35859-106">The **ncadg\_ip\_udp** keyword identifies the datagram version of TCP/IP as the protocol family for the endpoint.</span></span> <span data-ttu-id="35859-107">Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="35859-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="35859-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35859-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35859-109">*nombre del servidor*</span><span class="sxs-lookup"><span data-stu-id="35859-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="35859-110">Especifica el nombre o la dirección de Internet del servidor, o host, del equipo.</span><span class="sxs-lookup"><span data-stu-id="35859-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="35859-111">El nombre es una cadena de caracteres y puede ser un nombre de dominio completo.</span><span class="sxs-lookup"><span data-stu-id="35859-111">The name is a character string and may be a fully qualified domain name.</span></span> <span data-ttu-id="35859-112">La dirección de Internet es una notación de dirección de Internet común.</span><span class="sxs-lookup"><span data-stu-id="35859-112">The internet address is a common internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="35859-113">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="35859-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="35859-114">Especifica un número de 16 bits opcional.</span><span class="sxs-lookup"><span data-stu-id="35859-114">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="35859-115">Los valores de menos de 1024 suelen estar reservados.</span><span class="sxs-lookup"><span data-stu-id="35859-115">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="35859-116">Si no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de Puerto* válido.</span><span class="sxs-lookup"><span data-stu-id="35859-116">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35859-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35859-117">Remarks</span></span>

<span data-ttu-id="35859-118">Las siguientes restricciones se aplican a los protocolos de datagramas, [**ncadg \_ IPX**](ncadg-ipx.md) y **ncadg \_ IP \_ UDP**:</span><span class="sxs-lookup"><span data-stu-id="35859-118">The following restrictions apply to the datagram protocols, [**ncadg\_ipx**](ncadg-ipx.md) and **ncadg\_ip\_udp**:</span></span>

-   <span data-ttu-id="35859-119">No admiten las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="35859-119">They do not support callbacks.</span></span> <span data-ttu-id="35859-120">**\[** [](callback.md) Se producirá un error en todas las funciones que utilicen el **\]** atributo callback.</span><span class="sxs-lookup"><span data-stu-id="35859-120">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="35859-121">No admiten el uso del constructor de tipo de [**canalización**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="35859-121">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="35859-122">La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación IDL.</span><span class="sxs-lookup"><span data-stu-id="35859-122">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="35859-123">El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="35859-123">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="35859-124">Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="35859-124">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="35859-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="35859-125">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="35859-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="35859-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35859-127">**finales**</span><span class="sxs-lookup"><span data-stu-id="35859-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="35859-128">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="35859-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="35859-129">**ncacn \_ en \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="35859-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="35859-130">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="35859-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="35859-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="35859-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="35859-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="35859-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="35859-133">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="35859-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="35859-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="35859-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="35859-135">**\_TCP NB \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="35859-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="35859-136">**NP de ncacn \_**</span><span class="sxs-lookup"><span data-stu-id="35859-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="35859-137">**ncacn \_ redes virtuales \_ spp**</span><span class="sxs-lookup"><span data-stu-id="35859-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="35859-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="35859-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="35859-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="35859-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="35859-140">Enlace de cadenas</span><span class="sxs-lookup"><span data-stu-id="35859-140">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 