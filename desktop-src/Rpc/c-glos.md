---
title: C (RPC)
description: Palabras a partir de C en el Glosario de llamada a procedimiento remoto (RPC).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: da1ee843-c33e-42a1-bcaf-6cdb4834e70b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15eb37af87fd36dd31f3e9e106904b4ce734c15
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995868"
---
# <a name="c-rpc"></a><span data-ttu-id="38724-103">C (RPC)</span><span class="sxs-lookup"><span data-stu-id="38724-103">C (RPC)</span></span>

<span data-ttu-id="38724-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [o](o-glos.md) [p](p-glos.md) [Q](q.md) [R](r-glos.md) [s](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="38724-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="38724-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Servicio de directorio de celdas (CDS)**</span><span class="sxs-lookup"><span data-stu-id="38724-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Cell Directory Service (CDS)**</span></span>
</dt> <dd>

<span data-ttu-id="38724-106">Nombre: proveedor de servicios para el entorno informático distribuido de Open Software Foundation.</span><span class="sxs-lookup"><span data-stu-id="38724-106">Name-service provider for the Open Software Foundation's Distributed Computing Environment.</span></span>

</dd> <dt>

<span data-ttu-id="38724-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**código auxiliar de cliente**</span><span class="sxs-lookup"><span data-stu-id="38724-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**client stub**</span></span>
</dt> <dd>

<span data-ttu-id="38724-108">Código fuente del lenguaje C generado por MIDL.</span><span class="sxs-lookup"><span data-stu-id="38724-108">MIDL-generated C-language source code.</span></span> <span data-ttu-id="38724-109">Contiene todas las funciones necesarias para que la aplicación cliente realice llamadas a procedimientos remotos mediante el modelo de una llamada de función tradicional en una aplicación independiente.</span><span class="sxs-lookup"><span data-stu-id="38724-109">It contains all the functions necessary for the client application to make remote procedure calls using the model of a traditional function call in a standalone application.</span></span> <span data-ttu-id="38724-110">El código auxiliar de cliente es responsable de calcular las referencias de los parámetros de entrada y de calcular las referencias de los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="38724-110">The client stub is responsible for marshaling input parameters and unmarshaling output parameters.</span></span> <span data-ttu-id="38724-111">Vea también [*código auxiliar de servidor*](s-glos.md)y [*código auxiliar de proxy*](p-glos.md).</span><span class="sxs-lookup"><span data-stu-id="38724-111">See also [*server stub*](s-glos.md), [*proxy stub*](p-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="38724-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**matriz compatible**</span><span class="sxs-lookup"><span data-stu-id="38724-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**conformant array**</span></span>
</dt> <dd>

<span data-ttu-id="38724-113">Matriz cuyo tamaño se determina en tiempo de ejecución por otro parámetro, campo de estructura o expresión.</span><span class="sxs-lookup"><span data-stu-id="38724-113">Array whose size is determined at run time by another parameter, structure field, or expression.</span></span>

</dd> <dt>

<span data-ttu-id="38724-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**orientado a la conexión**</span><span class="sxs-lookup"><span data-stu-id="38724-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**connection-oriented**</span></span>
</dt> <dd>

<span data-ttu-id="38724-115">Protocolo de comunicaciones o transporte que proporciona un circuito virtual a través del cual los paquetes de datos se reciben en el mismo orden en que se transmitiron.</span><span class="sxs-lookup"><span data-stu-id="38724-115">Communications protocol or transport that provides a virtual circuit through which data packets are received in the same order as they were transmitted.</span></span> <span data-ttu-id="38724-116">Si se produce un error en la conexión entre equipos, se notifica a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38724-116">If the connection between computers fails, the application is notified.</span></span> <span data-ttu-id="38724-117">[*TCP*](t-glos.md) y [*SPX*](s-glos.md) son ejemplos de protocolos orientados a la conexión.</span><span class="sxs-lookup"><span data-stu-id="38724-117">[*TCP*](t-glos.md) and [*SPX*](s-glos.md) are examples of connection-oriented protocols.</span></span> <span data-ttu-id="38724-118">Vea también [*datagrama*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="38724-118">See also [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="38724-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**sin conexión**</span><span class="sxs-lookup"><span data-stu-id="38724-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**connectionless**</span></span>
</dt> <dd>

<span data-ttu-id="38724-120">Vea [*Datagram*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="38724-120">See [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="38724-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**detención de contexto**</span><span class="sxs-lookup"><span data-stu-id="38724-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**context rundown**</span></span>
</dt> <dd>

<span data-ttu-id="38724-122">Notificación de servidor que es el resultado de una terminación inesperada del enlace entre las aplicaciones cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="38724-122">Server notification that results from an unexpected termination of the binding between client and server applications.</span></span>

</dd> </dl>

 

 




