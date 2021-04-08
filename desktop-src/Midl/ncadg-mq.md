---
title: ncadg_mq atributo)
description: La \_ palabra clave ncadg MQ identifica Microsoft Message Queuing Services (MSMQ) como protocolo de transporte para el extremo. Este protocolo está obsoleto y no debe usarse en aplicaciones nuevas.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq el atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995171"
---
# <a name="ncadg_mq-attribute"></a><span data-ttu-id="9613e-105">\_atributo MQ ncadg</span><span class="sxs-lookup"><span data-stu-id="9613e-105">ncadg\_mq attribute</span></span>

<span data-ttu-id="9613e-106">La palabra clave **ncadg \_ mq** identifica Microsoft Message QUEUING Services (MSMQ) como protocolo de transporte para el extremo.</span><span class="sxs-lookup"><span data-stu-id="9613e-106">The **ncadg\_mq** keyword identifies Microsoft Message Queuing Services (MSMQ) as the transport protocol for the endpoint.</span></span> <span data-ttu-id="9613e-107">Este protocolo está obsoleto y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="9613e-107">This protocol is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a><span data-ttu-id="9613e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9613e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9613e-109">*nombre del servidor*</span><span class="sxs-lookup"><span data-stu-id="9613e-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9613e-110">Especifica el nombre del servidor, o host, del equipo.</span><span class="sxs-lookup"><span data-stu-id="9613e-110">Specifies the name of the server, or host, computer.</span></span> <span data-ttu-id="9613e-111">El nombre es una cadena de caracteres y puede ser un nombre de dominio completo.</span><span class="sxs-lookup"><span data-stu-id="9613e-111">The name is a character string and may be a fully qualified domain name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9613e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9613e-112">Remarks</span></span>

<span data-ttu-id="9613e-113">Para usar el protocolo de **transporte \_ MQ de ncadg** , los componentes de MSMQ deben estar completamente instalados y los sistemas de servidor y cliente deben ser accesibles a través de los protocolos MQ.</span><span class="sxs-lookup"><span data-stu-id="9613e-113">In order to use the **ncadg\_mq** transport protocol, the MSMQ components must be fully installed and the client and server systems must be reachable through the MQ protocols.</span></span>

<span data-ttu-id="9613e-114">El **Protocolo \_ MQ ncadg** no admite puntos de conexión dinámicos ni llamadas de [**difusión**](broadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="9613e-114">The **ncadg\_mq** protocol does not support dynamic endpoints or [**broadcast**](broadcast.md) calls.</span></span> <span data-ttu-id="9613e-115">Al igual que con otros protocolos de datagrama, **ncadg \_ MQ** no admite las devoluciones de llamada; se producirá un error en todas las funciones que utilicen el atributo [**callback**](callback.md) .</span><span class="sxs-lookup"><span data-stu-id="9613e-115">As with other datagram protocols, **ncadg\_mq** does not support callbacks; any functions using the [**callback**](callback.md) attribute will fail.</span></span>

> [!Note]  
> <span data-ttu-id="9613e-116">Esta familia de protocolos no se admite en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9613e-116">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9613e-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9613e-117">Examples</span></span>

<span data-ttu-id="9613e-118">La sintaxis del protocolo Message-Queue se define independientemente de la especificación IDL.</span><span class="sxs-lookup"><span data-stu-id="9613e-118">The syntax of the message-queue protocol is defined independently of the IDL specification.</span></span> <span data-ttu-id="9613e-119">El compilador MIDL realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del extremo sea correcta.</span><span class="sxs-lookup"><span data-stu-id="9613e-119">The MIDL compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="9613e-120">Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="9613e-120">Some errors may be reported at run time rather than during compilation.</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="9613e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9613e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9613e-122">**amplia**</span><span class="sxs-lookup"><span data-stu-id="9613e-122">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="9613e-123">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="9613e-123">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="9613e-124">**finales**</span><span class="sxs-lookup"><span data-stu-id="9613e-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="9613e-125">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="9613e-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9613e-126">**Mensaje**</span><span class="sxs-lookup"><span data-stu-id="9613e-126">**message**</span></span>](message.md)
</dt> <dt>

[<span data-ttu-id="9613e-127">Message Queue Server de RPC</span><span class="sxs-lookup"><span data-stu-id="9613e-127">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="9613e-128">Enlace de cadenas</span><span class="sxs-lookup"><span data-stu-id="9613e-128">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 