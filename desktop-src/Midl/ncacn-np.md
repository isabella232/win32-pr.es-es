---
title: ncacn_np atributo)
description: La \_ palabra clave ncacn NP identifica las canalizaciones con nombre como la familia de protocolos para el punto de conexión.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791200"
---
# <a name="ncacn_np-attribute"></a><span data-ttu-id="a60d0-104">\_atributo ncacn NP</span><span class="sxs-lookup"><span data-stu-id="a60d0-104">ncacn\_np attribute</span></span>

<span data-ttu-id="a60d0-105">La palabra clave **ncacn \_ NP** identifica las canalizaciones con nombre como la familia de protocolos para el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="a60d0-105">The **ncacn\_np** keyword identifies named pipes as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a><span data-ttu-id="a60d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a60d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a60d0-107">*nombre del servidor*</span><span class="sxs-lookup"><span data-stu-id="a60d0-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a60d0-108">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a60d0-108">Optional.</span></span> <span data-ttu-id="a60d0-109">Especifica el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="a60d0-109">Specifies the name of the server.</span></span> <span data-ttu-id="a60d0-110">Los caracteres de barra diagonal inversa son opcionales.</span><span class="sxs-lookup"><span data-stu-id="a60d0-110">Backslash characters are optional.</span></span>

</dd> <dt>

<span data-ttu-id="a60d0-111">*nombre de canalización*</span><span class="sxs-lookup"><span data-stu-id="a60d0-111">*pipe-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a60d0-112">Especifica un nombre de canalización válido.</span><span class="sxs-lookup"><span data-stu-id="a60d0-112">Specifies a valid pipe name.</span></span> <span data-ttu-id="a60d0-113">Un nombre de canalización válido es una cadena que contiene identificadores separados por caracteres de barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="a60d0-113">A valid pipe name is a string containing identifiers separated by backslash characters.</span></span> <span data-ttu-id="a60d0-114">El primer identificador debe ser una [**canalización**](pipe.md).</span><span class="sxs-lookup"><span data-stu-id="a60d0-114">The first identifier must be [**pipe**](pipe.md).</span></span> <span data-ttu-id="a60d0-115">Cada identificador debe estar separado por dos caracteres de barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="a60d0-115">Each identifier must be separated by two backslash characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a60d0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a60d0-116">Remarks</span></span>

<span data-ttu-id="a60d0-117">Un servidor crea una instancia de una canalización con nombre que, a continuación, está disponible para cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="a60d0-117">A server creates an instance of a named pipe that is then available to any client.</span></span> <span data-ttu-id="a60d0-118">Cuando un cliente intenta conectarse, la instancia existente se asocia con ese cliente.</span><span class="sxs-lookup"><span data-stu-id="a60d0-118">When a client attempts to connect, the existing instance is associated with that client.</span></span> <span data-ttu-id="a60d0-119">Antes de que otro cliente pueda conectarse, el servidor debe crear otra instancia de la canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="a60d0-119">Before another client can connect, the server must create another instance of the named pipe.</span></span> <span data-ttu-id="a60d0-120">Si un cliente intenta enlazarse al servidor antes de que se cree la nueva instancia, la llamada de enlace, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), puede generar un error con el mensaje de error RPC \_ S \_ Server \_ Too \_ busy.</span><span class="sxs-lookup"><span data-stu-id="a60d0-120">If a client tries to bind to the server before the new instance is created, the binding call, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), may fail with the error message RPC\_S\_SERVER\_TOO\_BUSY.</span></span> <span data-ttu-id="a60d0-121">Por lo tanto, debe asegurarse de que la aplicación cliente controla el caso en el que el servidor está demasiado ocupado para aceptar una conexión.</span><span class="sxs-lookup"><span data-stu-id="a60d0-121">Therefore, you need to make sure that your client application handles the case where the server is too busy to accept a connection.</span></span> <span data-ttu-id="a60d0-122">El cliente debe volver a intentarlo automáticamente, preguntar al usuario sobre una acción o producir un error.</span><span class="sxs-lookup"><span data-stu-id="a60d0-122">The client should automatically retry, prompt the user for a course of action, or fail gracefully.</span></span>

<span data-ttu-id="a60d0-123">La sintaxis de la cadena de puerto de la canalización con nombre, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL.</span><span class="sxs-lookup"><span data-stu-id="a60d0-123">The syntax of the named-pipe port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="a60d0-124">El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="a60d0-124">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="a60d0-125">Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="a60d0-125">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="a60d0-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a60d0-126">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="a60d0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a60d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60d0-128">**finales**</span><span class="sxs-lookup"><span data-stu-id="a60d0-128">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="a60d0-129">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="a60d0-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a60d0-130">**ncacn \_ en \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="a60d0-130">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="a60d0-131">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="a60d0-131">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="a60d0-132">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="a60d0-132">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="a60d0-133">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="a60d0-133">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="a60d0-134">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="a60d0-134">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="a60d0-135">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="a60d0-135">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="a60d0-136">**\_TCP NB \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="a60d0-136">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="a60d0-137">**ncacn \_ redes virtuales \_ spp**</span><span class="sxs-lookup"><span data-stu-id="a60d0-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="a60d0-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="a60d0-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="a60d0-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="a60d0-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="a60d0-140">**ncadg \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="a60d0-140">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="a60d0-141">**enlace de cadenas**</span><span class="sxs-lookup"><span data-stu-id="a60d0-141">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 