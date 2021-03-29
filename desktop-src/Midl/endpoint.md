---
title: atributo de extremo
description: El atributo \ Endpoint \ especifica un puerto o puertos conocidos (puntos de conexión de comunicación) en los que los servidores de la interfaz escuchan las llamadas.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- atributo de extremo MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904525"
---
# <a name="endpoint-attribute"></a><span data-ttu-id="47e9b-104">atributo de extremo</span><span class="sxs-lookup"><span data-stu-id="47e9b-104">endpoint attribute</span></span>

<span data-ttu-id="47e9b-105">El atributo de **\[ extremo \]** especifica un puerto o puertos conocidos (puntos de conexión de comunicación) en los que los servidores de la interfaz escuchan las llamadas.</span><span class="sxs-lookup"><span data-stu-id="47e9b-105">The **\[endpoint\]** attribute specifies a well-known port or ports (communication endpoints) on which servers of the interface listen for calls.</span></span>

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a><span data-ttu-id="47e9b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47e9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e9b-107">*Protocolo: secuencia*</span><span class="sxs-lookup"><span data-stu-id="47e9b-107">*protocol-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="47e9b-108">Especifica una cadena de caracteres que representa una combinación válida de un protocolo RPC (como "ncacn"), un protocolo de transporte (por ejemplo, "TCP") y un protocolo de red (como "IP").</span><span class="sxs-lookup"><span data-stu-id="47e9b-108">Specifies a character string that represents a valid combination of an RPC protocol (such as "ncacn"), a transport protocol (such as "tcp"), and a network protocol (such as "ip").</span></span> <span data-ttu-id="47e9b-109">Para obtener una lista de secuencias de protocolo válidas, vea [constantes de secuencia de protocolos](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="47e9b-109">For a list of valid protocol sequences, see [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

</dd> <dt>

<span data-ttu-id="47e9b-110">*Puerto de extremo*</span><span class="sxs-lookup"><span data-stu-id="47e9b-110">*endpoint-port*</span></span> 
</dt> <dd>

<span data-ttu-id="47e9b-111">Especifica una cadena que representa la designación del extremo para la familia de protocolos especificada.</span><span class="sxs-lookup"><span data-stu-id="47e9b-111">Specifies a string that represents the endpoint designation for the specified protocol family.</span></span> <span data-ttu-id="47e9b-112">La sintaxis de la cadena de puerto es específica de cada secuencia de protocolos.</span><span class="sxs-lookup"><span data-stu-id="47e9b-112">The syntax of the port string is specific to each protocol sequence.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47e9b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47e9b-113">Remarks</span></span>

<span data-ttu-id="47e9b-114">El atributo de **\[ extremo \]** especifica una familia de transporte como el protocolo orientado a la conexión TCP/IP, un protocolo orientado a la conexión NetBIOS o el protocolo orientado a la conexión de canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="47e9b-114">The **\[endpoint\]** attribute specifies a transport family such as the TCP/IP connection-oriented protocol, a NetBIOS connection-oriented protocol, or the named-pipe connection-oriented protocol.</span></span> <span data-ttu-id="47e9b-115">El uso del atributo de **\[ punto de conexión \]** es coherente con otros métodos para agregar un punto de conexión y no proporciona servicios adicionales o especiales para el punto de conexión; simplemente proporciona un acceso directo para llamar a la API.</span><span class="sxs-lookup"><span data-stu-id="47e9b-115">Use of the **\[endpoint\]** attribute is consistent with other methods for adding an endpoint, and does not provide additional or special services for the endpoint; it simply provides a shortcut for calling the API.</span></span>

> [!Note]  
> <span data-ttu-id="47e9b-116">Especificar un extremo en. La definición de la interfaz IDL no restringe el acceso a la interfaz al punto de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="47e9b-116">Specifying an endpoint in the .IDL interface definition does not restrict access to the interface to the specified endpoint.</span></span> <span data-ttu-id="47e9b-117">Agregar un punto de conexión a. La definición de la interfaz IDL permite llamar a la interfaz a través de cualquier punto de conexión de ese proceso y permite usar el punto de conexión para llamar a otras interfaces en ese proceso.</span><span class="sxs-lookup"><span data-stu-id="47e9b-117">Adding an endpoint to the .IDL interface definition allows the interface to be called through any endpoint in that process, and allows the endpoint to be used to call other interfaces in that process.</span></span>

 

<span data-ttu-id="47e9b-118">El valor de la *secuencia de protocolos* determina los valores válidos para el *Puerto del extremo*.</span><span class="sxs-lookup"><span data-stu-id="47e9b-118">The *protocol-sequence* value determines the valid values for the *endpoint-port*.</span></span> <span data-ttu-id="47e9b-119">El compilador MIDL comprueba únicamente la sintaxis general de la entrada del *Puerto de extremo* .</span><span class="sxs-lookup"><span data-stu-id="47e9b-119">The MIDL compiler checks only general syntax for the *endpoint-port* entry.</span></span> <span data-ttu-id="47e9b-120">Las bibliotecas en tiempo de ejecución informan de los errores de especificación de puerto.</span><span class="sxs-lookup"><span data-stu-id="47e9b-120">Port specification errors are reported by the run-time libraries.</span></span> <span data-ttu-id="47e9b-121">Para obtener información sobre los valores permitidos para cada secuencia de protocolo, vea las [constantes de secuencia de protocolo](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="47e9b-121">For information about the allowed values for each protocol sequence, see the [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

<span data-ttu-id="47e9b-122">Las siguientes secuencias de protocolo especificadas por DCE no son compatibles con el compilador MIDL proporcionado con Microsoft RPC: **ncacn \_ OSI \_ DNA** y **ncadg \_ DDS**.</span><span class="sxs-lookup"><span data-stu-id="47e9b-122">The following protocol sequences specified by DCE are not supported by the MIDL compiler provided with Microsoft RPC: **ncacn\_osi\_dna** and **ncadg\_dds**.</span></span>

<span data-ttu-id="47e9b-123">Asegúrese de que ha comillas correctamente los caracteres de barra diagonal inversa en los extremos.</span><span class="sxs-lookup"><span data-stu-id="47e9b-123">Make sure that you correctly quote backslash characters in endpoints.</span></span> <span data-ttu-id="47e9b-124">Este error suele producirse cuando el punto de conexión es una canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="47e9b-124">This error commonly occurs when the endpoint is a named pipe.</span></span>

<span data-ttu-id="47e9b-125">La información del punto de conexión especificada en el archivo IDL se usa en las funciones de tiempo de ejecución de RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) y [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span><span class="sxs-lookup"><span data-stu-id="47e9b-125">Endpoint information specified in the IDL file is used by the RPC run-time functions [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) and [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span></span>

## <a name="examples"></a><span data-ttu-id="47e9b-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="47e9b-126">Examples</span></span>

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a><span data-ttu-id="47e9b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="47e9b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e9b-128">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="47e9b-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="47e9b-129">**RpcServerUseAllProtseqsIf**</span><span class="sxs-lookup"><span data-stu-id="47e9b-129">**RpcServerUseAllProtseqsIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[<span data-ttu-id="47e9b-130">**RpcServerUseProtseqIf**</span><span class="sxs-lookup"><span data-stu-id="47e9b-130">**RpcServerUseProtseqIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 