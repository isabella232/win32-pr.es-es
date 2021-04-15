---
title: ncacn_spx atributo)
description: La \_ palabra clave ncacn SPX identifica SPX como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665817"
---
# <a name="ncacn_spx-attribute"></a><span data-ttu-id="32550-105">\_atributo ncacn SPX</span><span class="sxs-lookup"><span data-stu-id="32550-105">ncacn\_spx attribute</span></span>

<span data-ttu-id="32550-106">La palabra clave **ncacn \_ SPX** identifica SPX como la familia de protocolos para el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="32550-106">The **ncacn\_spx** keyword identifies SPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="32550-107">Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="32550-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="32550-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32550-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32550-109">*Dirección de vínculo*</span><span class="sxs-lookup"><span data-stu-id="32550-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="32550-110">Especifica el servidor host.</span><span class="sxs-lookup"><span data-stu-id="32550-110">Specifies the host server.</span></span> <span data-ttu-id="32550-111">Puede ser una cadena de caracteres (el nombre del servidor) o un número hexadecimal de 20 dígitos que consta de la dirección de red del servidor host (8 dígitos) concatenada con la dirección del nodo (12 dígitos).</span><span class="sxs-lookup"><span data-stu-id="32550-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="32550-112">Vea la sección Comentarios para obtener instrucciones sobre cómo obtener la dirección de red y la dirección de nodo.</span><span class="sxs-lookup"><span data-stu-id="32550-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="32550-113">Una cadena **nula** especifica el equipo local.</span><span class="sxs-lookup"><span data-stu-id="32550-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="32550-114">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="32550-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="32550-115">Especifica un número de 16 bits opcional que representa la dirección del socket.</span><span class="sxs-lookup"><span data-stu-id="32550-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="32550-116">Los valores pueden oscilar entre 1 y 65.535.</span><span class="sxs-lookup"><span data-stu-id="32550-116">Values can range from 1 to 65,535.</span></span> <span data-ttu-id="32550-117">Cuando no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de Puerto* válido.</span><span class="sxs-lookup"><span data-stu-id="32550-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32550-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32550-118">Remarks</span></span>

<span data-ttu-id="32550-119">Cuando se usa el **transporte \_ SPX de ncacn** , el nombre del servidor es exactamente el mismo que el nombre de Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="32550-119">When you use the **ncacn\_spx** transport, the server name is exactly the same as the 32-bit Windows name.</span></span> <span data-ttu-id="32550-120">Sin embargo, puesto que los nombres se distribuyen mediante protocolos de Novell, deben cumplir las convenciones de nomenclatura de Novell.</span><span class="sxs-lookup"><span data-stu-id="32550-120">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="32550-121">Si un nombre de servidor no es un nombre de Novell válido, los servidores no podrán crear extremos con el transporte **\_ SPX de ncacn** .</span><span class="sxs-lookup"><span data-stu-id="32550-121">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** transport.</span></span> <span data-ttu-id="32550-122">La siguiente es una lista parcial de caracteres prohibidos en los nombres de servidor Novell:</span><span class="sxs-lookup"><span data-stu-id="32550-122">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="32550-123">" \* + .</span><span class="sxs-lookup"><span data-stu-id="32550-123">" \* + .</span></span> <span data-ttu-id="32550-124">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="32550-124">/ : ; < = > ?</span></span> <span data-ttu-id="32550-125">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="32550-125">\[ \] \\ \|</span></span>

<span data-ttu-id="32550-126">La versión de NWLink suministrada con el cliente 3,0 de MS no admite el transporte **ncacn \_ SPX** .</span><span class="sxs-lookup"><span data-stu-id="32550-126">The **ncacn\_spx** transport is not supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="32550-127">las aplicaciones cliente de Windows de 16 bits que usan el transporte **\_ SPX de ncacn** requieren que el archivo Nwipxspx.dll instalarse para ejecutarse en el subsistema wow.</span><span class="sxs-lookup"><span data-stu-id="32550-127">16-bit Windows client applications that use the **ncacn\_spx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="32550-128">Póngase en contacto con Novell para obtener este archivo.</span><span class="sxs-lookup"><span data-stu-id="32550-128">Contact Novell to obtain this file.</span></span>

> [!Note]  
> <span data-ttu-id="32550-129">Para obtener las direcciones de red y nodo, use la utilidad **ComCheck** de Novell o la API **IPXGetInternetAddress** definida por Novell.</span><span class="sxs-lookup"><span data-stu-id="32550-129">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="32550-130">En Windows, también puede obtener estas direcciones con el comando **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="32550-130">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

 

<span data-ttu-id="32550-131">La sintaxis de la cadena de puerto de transporte SPX, al igual que todas las cadenas de puerto, se define independientemente de la especificación IDL.</span><span class="sxs-lookup"><span data-stu-id="32550-131">The syntax of the SPX transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="32550-132">El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="32550-132">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="32550-133">Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="32550-133">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="32550-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="32550-134">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="32550-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="32550-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32550-136">**finales**</span><span class="sxs-lookup"><span data-stu-id="32550-136">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="32550-137">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="32550-137">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="32550-138">**ncacn \_ en \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="32550-138">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="32550-139">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="32550-139">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="32550-140">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="32550-140">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="32550-141">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="32550-141">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="32550-142">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="32550-142">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="32550-143">**\_TCP NB \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="32550-143">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="32550-144">**NP de ncacn \_**</span><span class="sxs-lookup"><span data-stu-id="32550-144">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="32550-145">**ncacn \_ redes virtuales \_ spp**</span><span class="sxs-lookup"><span data-stu-id="32550-145">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="32550-146">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="32550-146">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="32550-147">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="32550-147">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="32550-148">**ncadg \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="32550-148">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="32550-149">enlace de cadenas</span><span class="sxs-lookup"><span data-stu-id="32550-149">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 