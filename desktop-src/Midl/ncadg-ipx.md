---
title: ncadg_ipx atributo)
description: La \_ palabra clave ncadg IPX identifica IPX como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx el atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790185"
---
# <a name="ncadg_ipx-attribute"></a><span data-ttu-id="b3c5e-105">ncadg \_ atributo IPX</span><span class="sxs-lookup"><span data-stu-id="b3c5e-105">ncadg\_ipx attribute</span></span>

<span data-ttu-id="b3c5e-106">La palabra clave **ncadg \_ IPX** identifica IPX como la familia de protocolos para el extremo.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-106">The **ncadg\_ipx** keyword identifies IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="b3c5e-107">Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="b3c5e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3c5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c5e-109">*Dirección de vínculo*</span><span class="sxs-lookup"><span data-stu-id="b3c5e-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c5e-110">Especifica el servidor host.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-110">Specifies the host server.</span></span> <span data-ttu-id="b3c5e-111">Puede ser una cadena de caracteres (el nombre del servidor) o un número hexadecimal de 20 dígitos que consta de la dirección de red del servidor host (8 dígitos) concatenada con la dirección del nodo (12 dígitos).</span><span class="sxs-lookup"><span data-stu-id="b3c5e-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="b3c5e-112">Vea la sección Comentarios para obtener instrucciones sobre cómo obtener la dirección de red y la dirección de nodo.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="b3c5e-113">Una cadena **nula** especifica el equipo local.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="b3c5e-114">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="b3c5e-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c5e-115">Especifica un número de 16 bits opcional que representa la dirección del socket.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="b3c5e-116">Los valores pueden oscilar entre 1 y 65535.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-116">Values can range from 1 to 65535.</span></span> <span data-ttu-id="b3c5e-117">Cuando no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de Puerto* válido.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3c5e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3c5e-118">Remarks</span></span>

<span data-ttu-id="b3c5e-119">Las siguientes restricciones se aplican a los protocolos de datagramas, **ncadg \_ IPX** y [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):</span><span class="sxs-lookup"><span data-stu-id="b3c5e-119">The following restrictions apply to the datagram protocols, **ncadg\_ipx** and [**ncadg\_ip\_udp**](ncadg-ip-udp.md):</span></span>

-   <span data-ttu-id="b3c5e-120">No admiten las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-120">They do not support callbacks.</span></span> <span data-ttu-id="b3c5e-121">**\[** [](callback.md) Se producirá un error en todas las funciones que utilicen el **\]** atributo callback.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-121">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="b3c5e-122">No admiten el uso del constructor de tipo de [**canalización**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c5e-122">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="b3c5e-123">Cuando se usa el transporte **\_ IPX ncadg** , el nombre del servidor es exactamente el mismo que el nombre de Windows Server de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-123">When using the **ncadg\_ipx** transport, the server name is exactly the same as the 32-bit Windows server name.</span></span> <span data-ttu-id="b3c5e-124">Sin embargo, puesto que los nombres se distribuyen mediante protocolos de Novell, deben cumplir las convenciones de nomenclatura de Novell.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-124">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="b3c5e-125">Si un nombre de servidor no es un nombre de Novell válido, los servidores no podrán crear extremos con el transporte **\_ IPX ncadg** .</span><span class="sxs-lookup"><span data-stu-id="b3c5e-125">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncadg\_ipx** transport.</span></span> <span data-ttu-id="b3c5e-126">La siguiente es una lista parcial de caracteres prohibidos en los nombres de servidor Novell:</span><span class="sxs-lookup"><span data-stu-id="b3c5e-126">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="b3c5e-127">" \* + .</span><span class="sxs-lookup"><span data-stu-id="b3c5e-127">" \* + .</span></span> <span data-ttu-id="b3c5e-128">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="b3c5e-128">/ : ; < = > ?</span></span> <span data-ttu-id="b3c5e-129">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="b3c5e-129">\[ \] \\ \|</span></span>

<span data-ttu-id="b3c5e-130">La versión de NWLink suministrada con el cliente 3,0 de MS admite el transporte **\_ IPX ncadg** .</span><span class="sxs-lookup"><span data-stu-id="b3c5e-130">The **ncadg\_ipx** transport is supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="b3c5e-131">las aplicaciones cliente de Windows de 16 bits que usan el transporte **\_ IPX ncadg** requieren que el archivo Nwipxspx.dll instalarse para ejecutarse en el subsistema wow.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-131">16-bit Windows client applications that use the **ncadg\_ipx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="b3c5e-132">Póngase en contacto con Novell para obtener este archivo.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-132">Contact Novell to obtain this file.</span></span>

<span data-ttu-id="b3c5e-133">Para obtener las direcciones de red y nodo, use la utilidad **ComCheck** de Novell o la API **IPXGetInternetAddress** definida por Novell.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-133">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="b3c5e-134">En Windows, también puede obtener estas direcciones con el comando **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="b3c5e-134">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

<span data-ttu-id="b3c5e-135">La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación IDL.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-135">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="b3c5e-136">El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-136">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="b3c5e-137">Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-137">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="b3c5e-138">Esta familia de protocolos no se admite en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-138">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b3c5e-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b3c5e-139">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="b3c5e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3c5e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c5e-141">**finales**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-141">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-142">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="b3c5e-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-143">**ncacn \_ en \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-143">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-144">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-144">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-145">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-145">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-146">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-146">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-147">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-147">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-148">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-148">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-149">**\_TCP NB \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-149">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-150">**NP de ncacn \_**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-150">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-151">**ncacn \_ redes virtuales \_ spp**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-151">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-152">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-152">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-153">**ncadg \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-153">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="b3c5e-154">enlace de cadenas</span><span class="sxs-lookup"><span data-stu-id="b3c5e-154">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 