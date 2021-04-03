---
title: Interfaces de servidor de publicidad
description: El lado del servidor de una aplicación que usa identificadores automáticos debe llamar a la función RpcNsBindingExport para que la información de enlace del servidor esté disponible para los clientes.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075769"
---
# <a name="advertising-server-interfaces"></a><span data-ttu-id="5d021-103">Interfaces de servidor de publicidad</span><span class="sxs-lookup"><span data-stu-id="5d021-103">Advertising Server Interfaces</span></span>

<span data-ttu-id="5d021-104">El lado del servidor de una aplicación que usa identificadores automáticos debe llamar a la función [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) para que la información de enlace del servidor esté disponible para los clientes.</span><span class="sxs-lookup"><span data-stu-id="5d021-104">The server side of an application that uses automatic handles must call the function [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) to make binding information about the server available to clients.</span></span> <span data-ttu-id="5d021-105">Los identificadores de enlace automáticos requieren un servicio de nombres que se ejecute en un servidor al que pueda acceder el cliente.</span><span class="sxs-lookup"><span data-stu-id="5d021-105">Automatic binding handles require a name service running on a server that is accessible to the client.</span></span> <span data-ttu-id="5d021-106">La implementación de Microsoft del servicio de nombres, localizador de Microsoft, administra los identificadores automáticos.</span><span class="sxs-lookup"><span data-stu-id="5d021-106">The Microsoft implementation of the name service, Microsoft Locator, manages automatic handles.</span></span> <span data-ttu-id="5d021-107">Las aplicaciones de servidor que usan identificadores de enlace implícitos y explícitos también pueden anunciar su presencia en la base de datos del servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5d021-107">Server applications that use implicit and explicit binding handles can also advertise their presence in the name service database.</span></span>

<span data-ttu-id="5d021-108">Normalmente, el servidor llama a las siguientes funciones en tiempo de ejecución:</span><span class="sxs-lookup"><span data-stu-id="5d021-108">Typically, the server calls the following run-time functions:</span></span>

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

<span data-ttu-id="5d021-109">Las llamadas a las dos primeras funciones de este fragmento de código son similares al [ejemplo Hello, World](tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="5d021-109">The calls to the first two functions in this code fragment are similar to the [Hello, World example](tutorial.md).</span></span> <span data-ttu-id="5d021-110">Estas funciones realizan información sobre el enlace disponible para el cliente.</span><span class="sxs-lookup"><span data-stu-id="5d021-110">These functions make information about the binding available to the client.</span></span> <span data-ttu-id="5d021-111">Las llamadas a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) y [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) colocan la información en la base de datos del servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5d021-111">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) put the information in the name service database.</span></span> <span data-ttu-id="5d021-112">La llamada a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) rellena el vector de enlace con identificadores de enlace válidos antes de que los identificadores se exporten al servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5d021-112">The call to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) fills the binding vector with valid binding handles before the handles are exported to the name service.</span></span> <span data-ttu-id="5d021-113">Una vez que el programa de servidor exporta los identificadores a la base de datos, el cliente (o los códigos auxiliares de cliente) puede llamar a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) y [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obtener esta información.</span><span class="sxs-lookup"><span data-stu-id="5d021-113">After the server program exports the handles to the database, the client (or client stubs) can call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) and [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) to obtain this information.</span></span> <span data-ttu-id="5d021-114">Para obtener más información, consulte [búsqueda de sistemas host de servidor](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="5d021-114">For details, see [Finding Server Host Systems](finding-server-host-systems.md).</span></span>

<span data-ttu-id="5d021-115">Las llamadas a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) y [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) y sus estructuras de datos asociadas tienen un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="5d021-115">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) and their associated data structures look similar to the following:</span></span>

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

<span data-ttu-id="5d021-116">Tenga en cuenta que el parámetro [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* es un puntero a un puntero a un [**\_ \_ Vector de enlace RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span><span class="sxs-lookup"><span data-stu-id="5d021-116">Note that the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parameter *pBindingVector* is a pointer to a pointer to [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span></span> <span data-ttu-id="5d021-117">Recuerde también que cada llamada a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) debe ir seguida de una llamada a [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span><span class="sxs-lookup"><span data-stu-id="5d021-117">Also remember that each call to [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) must be followed by a call to [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span></span>

<span data-ttu-id="5d021-118">Para quitar la interfaz exportada de la base de datos del servicio de nombres, el servidor llama a [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="5d021-118">To remove the exported interface from the name service database, the server calls [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) as shown:</span></span>

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

<span data-ttu-id="5d021-119">La función [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) solo debe usarse cuando el servicio se quita permanentemente.</span><span class="sxs-lookup"><span data-stu-id="5d021-119">The [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) function should be used only when the service is being permanently removed.</span></span> <span data-ttu-id="5d021-120">No debe usarse cuando el servicio está deshabilitado temporalmente, como cuando se apaga el servidor para el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5d021-120">It should not be used when the service is temporarily disabled, such as when the server is shut down for maintenance.</span></span> <span data-ttu-id="5d021-121">Un programa de servidor puede registrarse en la base de datos del servicio de nombres, pero no estar disponible porque el servidor está sin conexión temporalmente.</span><span class="sxs-lookup"><span data-stu-id="5d021-121">A server program can register itself with the name service database, yet be unavailable because the server is temporarily offline.</span></span> <span data-ttu-id="5d021-122">La aplicación cliente debe contener el código de control de excepciones para esta condición.</span><span class="sxs-lookup"><span data-stu-id="5d021-122">The client application should contain exception-handling code for such a condition.</span></span>

<span data-ttu-id="5d021-123">Para obtener más información sobre el contenido y el formato de la base de datos del servicio de nombres, vea [la base de datos del servicio de nombres RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="5d021-123">For more information on the content and format of the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="5d021-124">Las aplicaciones pueden utilizar el servicio Active Directory si los programas cliente y servidor se ejecutan en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5d021-124">Applications can utilize the Active Directory service if both the client and server programs are running under Windows 2000.</span></span> <span data-ttu-id="5d021-125">Los equipos que ejecutan los programas de cliente y servidor de deben ser miembros de un dominio de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5d021-125">The computers running the client and server programs must both be members of a Windows 2000 domain.</span></span>

<span data-ttu-id="5d021-126">Para anunciar su presencia mediante el servicio Active Directory, el programa de servidor debe ejecutarse en el contexto de seguridad de un administrador de dominio.</span><span class="sxs-lookup"><span data-stu-id="5d021-126">To advertise its presence using the Active Directory service, the server program should run in the security context of a domain administrator.</span></span> <span data-ttu-id="5d021-127">Si se ejecuta en el contexto de los usuarios del dominio, un administrador de dominio debe modificar la lista de control de acceso (ACL) en el contenedor de servicios RPC.</span><span class="sxs-lookup"><span data-stu-id="5d021-127">If it is running in the context of domain users, a domain administrator must modify the access control list (ACL) on the RPC Services container.</span></span> <span data-ttu-id="5d021-128">Para obtener más información, consulte la documentación de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d021-128">For more information, see the Active Directory documentation.</span></span>

 

 




