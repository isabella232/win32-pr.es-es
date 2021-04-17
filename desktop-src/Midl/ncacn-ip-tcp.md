---
title: ncacn_ip_tcp atributo)
description: La \_ \_ palabra clave TCP de IP de NCACN identifica TCP/IP como la familia de protocolos para el extremo.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651371"
---
# <a name="ncacn_ip_tcp-attribute"></a><span data-ttu-id="ca6d3-104">\_atributo TCP de IP de ncacn \_</span><span class="sxs-lookup"><span data-stu-id="ca6d3-104">ncacn\_ip\_tcp attribute</span></span>

<span data-ttu-id="ca6d3-105">La palabra clave **\_ \_ TCP de IP de ncacn** identifica TCP/IP como la familia de protocolos para el extremo.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-105">The **ncacn\_ip\_tcp** keyword identifies TCP/IP as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="ca6d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca6d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca6d3-107">*nombre del servidor*</span><span class="sxs-lookup"><span data-stu-id="ca6d3-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ca6d3-108">Especifica el nombre o la dirección de Internet del servidor, o host, del equipo.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-108">Specifies the name or Internet address for the server, or host, computer.</span></span> <span data-ttu-id="ca6d3-109">El nombre es una cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-109">The name is a character string.</span></span> <span data-ttu-id="ca6d3-110">La dirección de Internet es una notación de dirección de Internet común.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-110">The Internet address is a common Internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d3-111">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="ca6d3-111">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ca6d3-112">Especifica un número de 16 bits opcional.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-112">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="ca6d3-113">Los valores de menos de 1024 suelen estar reservados.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-113">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="ca6d3-114">Si no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de Puerto* válido.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-114">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca6d3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca6d3-115">Remarks</span></span>

<span data-ttu-id="ca6d3-116">La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación IDL.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-116">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="ca6d3-117">El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-117">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="ca6d3-118">Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="ca6d3-118">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="ca6d3-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ca6d3-119">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a><span data-ttu-id="ca6d3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca6d3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca6d3-121">**finales**</span><span class="sxs-lookup"><span data-stu-id="ca6d3-121">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="ca6d3-122">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="ca6d3-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ca6d3-123">**\_TCP NB \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="ca6d3-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="ca6d3-124">**NP de ncacn \_**</span><span class="sxs-lookup"><span data-stu-id="ca6d3-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="ca6d3-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="ca6d3-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="ca6d3-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="ca6d3-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="ca6d3-127">**enlace de cadenas**</span><span class="sxs-lookup"><span data-stu-id="ca6d3-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 