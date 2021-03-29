---
title: ncacn_vns_spp atributo)
description: La \_ \_ palabra clave ncacn redes virtuales spp identifica Banyan Vines spp como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790708"
---
# <a name="ncacn_vns_spp-attribute"></a><span data-ttu-id="f0c58-105">\_atributo ncacn redes virtuales \_ spp</span><span class="sxs-lookup"><span data-stu-id="f0c58-105">ncacn\_vns\_spp attribute</span></span>

<span data-ttu-id="f0c58-106">La palabra clave **ncacn \_ redes virtuales \_ spp** identifica Banyan Vines spp como la familia de protocolos para el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="f0c58-106">The **ncacn\_vns\_spp** keyword identifies Banyan Vines SPP as the protocol family for the endpoint.</span></span> <span data-ttu-id="f0c58-107">Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="f0c58-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a><span data-ttu-id="f0c58-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0c58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c58-109">*nombre del servidor*</span><span class="sxs-lookup"><span data-stu-id="f0c58-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c58-110">Especifica el nombre de StreetTalk del servidor.</span><span class="sxs-lookup"><span data-stu-id="f0c58-110">Specifies the StreetTalk name of the server.</span></span> <span data-ttu-id="f0c58-111">El nombre tiene el formato item@group @organization .</span><span class="sxs-lookup"><span data-stu-id="f0c58-111">The name is of the form item@group@organization.</span></span> <span data-ttu-id="f0c58-112">El elemento puede tener una longitud de hasta 31 caracteres y el grupo y la organización pueden tener un máximo de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f0c58-112">The item can be up to 31 characters long and the group and organization can be up to 15 characters.</span></span>

</dd> <dt>

<span data-ttu-id="f0c58-113">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="f0c58-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c58-114">Especifica un puerto de Banyan Vines SPP.</span><span class="sxs-lookup"><span data-stu-id="f0c58-114">Specifies a Banyan Vines SPP port.</span></span> <span data-ttu-id="f0c58-115">El intervalo válido para los puntos de conexión estáticos es 250 – 511.</span><span class="sxs-lookup"><span data-stu-id="f0c58-115">The valid range for static endpoints is 250– 511.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0c58-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0c58-116">Remarks</span></span>

<span data-ttu-id="f0c58-117">Para usar el protocolo de transporte **ncacn \_ redes virtuales \_ spp** en aplicaciones distribuidas que se ejecutan en Windows 2000, debe instalarse el software de Banyan cliente de empresa adecuado.</span><span class="sxs-lookup"><span data-stu-id="f0c58-117">In order to use the **ncacn\_vns\_spp** transport protocol in distributed applications running on Windows 2000, the appropriate Banyan Enterprise Client software must be installed.</span></span> <span data-ttu-id="f0c58-118">Después de la instalación, abra el **Panel de control**, elija **configuración y agregar** y, a continuación, seleccione **servicio \| Banyan \| RPC Services para Banyan**.</span><span class="sxs-lookup"><span data-stu-id="f0c58-118">After installation, open **Control Panel**, choose **Configuration and Add**, then select **Service \| Banyan \| RPC services for Banyan**.</span></span> <span data-ttu-id="f0c58-119">La compatibilidad con clientes de 16 bits requiere el software de Vines adecuado.</span><span class="sxs-lookup"><span data-stu-id="f0c58-119">Support for 16-bit clients requires appropriate Vines software.</span></span> <span data-ttu-id="f0c58-120">Para obtener más información sobre el producto de Cliente de empresa de Banyan y el software de 16 bits Vines, póngase en contacto con Banyan.</span><span class="sxs-lookup"><span data-stu-id="f0c58-120">For more information about Banyan's Enterprise Client product and 16-bit Vines software, contact Banyan.</span></span>

<span data-ttu-id="f0c58-121">La sintaxis de la cadena de puerto de transporte de Banyan Vines SPP, como todas las cadenas de puerto, se define independientemente de la especificación de IDL.</span><span class="sxs-lookup"><span data-stu-id="f0c58-121">The syntax of the Banyan Vines SPP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="f0c58-122">El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="f0c58-122">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="f0c58-123">Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="f0c58-123">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="f0c58-124">Esta familia de protocolos no es compatible con Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0c58-124">This protocol family is not supported in Windows XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f0c58-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f0c58-125">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="f0c58-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c58-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c58-127">**finales**</span><span class="sxs-lookup"><span data-stu-id="f0c58-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="f0c58-128">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="f0c58-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f0c58-129">**ncacn \_ en \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="f0c58-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="f0c58-130">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="f0c58-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="f0c58-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="f0c58-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="f0c58-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="f0c58-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="f0c58-133">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="f0c58-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="f0c58-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="f0c58-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="f0c58-135">**\_TCP NB \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="f0c58-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="f0c58-136">**NP de ncacn \_**</span><span class="sxs-lookup"><span data-stu-id="f0c58-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="f0c58-137">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="f0c58-137">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="f0c58-138">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="f0c58-138">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="f0c58-139">**ncadg \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="f0c58-139">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="f0c58-140">enlace de cadenas</span><span class="sxs-lookup"><span data-stu-id="f0c58-140">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 