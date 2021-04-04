---
title: Registro de puntos de conexión
description: El registro del programa de servidor en la asignación de extremo del equipo host del servidor permite a los programas cliente determinar qué punto de conexión (normalmente un puerto TCP/IP o una canalización con nombre) está escuchando el programa de servidor.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- RPC llamada a procedimiento remoto, tareas, registrar extremos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772864"
---
# <a name="registering-endpoints"></a><span data-ttu-id="78e64-104">Registro de puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="78e64-104">Registering Endpoints</span></span>

<span data-ttu-id="78e64-105">El registro del programa de servidor en la asignación de extremo del equipo host del servidor permite a los programas cliente determinar qué punto de conexión (normalmente un puerto TCP/IP o una canalización con nombre) está escuchando el programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="78e64-105">Registering the server program in the endpoint map of the server host computer enables client programs to determine which endpoint (usually a TCP/IP port or a named pipe) the server program is listening to.</span></span> <span data-ttu-id="78e64-106">Para registrarse en la asignación de punto de conexión del sistema host del servidor, un programa de servidor llama a la función [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , tal como se muestra en el siguiente fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="78e64-106">To register itself in the server host system's endpoint map, a server program calls the [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) function as shown in the following code fragment:</span></span>


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



<span data-ttu-id="78e64-107">El primer parámetro de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) es la estructura que representa la interfaz.</span><span class="sxs-lookup"><span data-stu-id="78e64-107">The first parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is the structure that represents the interface.</span></span> <span data-ttu-id="78e64-108">Puede encontrarlo en el archivo de encabezado que el compilador MIDL generó a partir del archivo MIDL para esta aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="78e64-108">You can find it in the header file that the MIDL compiler generated from your MIDL file for this distributed application.</span></span> <span data-ttu-id="78e64-109">Vea [desarrollar la interfaz](developing-the-interface.md).</span><span class="sxs-lookup"><span data-stu-id="78e64-109">See [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="78e64-110">A continuación, **RpcEpRegister** necesita que la aplicación pase un conjunto de identificadores de enlace que se almacenan en un vector de enlace.</span><span class="sxs-lookup"><span data-stu-id="78e64-110">Next, **RpcEpRegister** needs your application to pass a set of binding handles that are stored in a binding vector.</span></span>

<span data-ttu-id="78e64-111">Además de registrar los nombres de interfaz, la aplicación de servidor también puede registrar UUID de objeto en la asignación de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="78e64-111">In addition to registering interface names, your server application can also register object UUIDs in the endpoint map.</span></span> <span data-ttu-id="78e64-112">En este ejemplo, no hay ningún UUID de objeto para registrar, por lo que el tercer parámetro de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="78e64-112">In this example, there are no object UUIDs to register, so the third parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is set to **NULL**.</span></span>

<span data-ttu-id="78e64-113">El último parámetro es una cadena de comentario.</span><span class="sxs-lookup"><span data-stu-id="78e64-113">The last parameter is a comment string.</span></span> <span data-ttu-id="78e64-114">Aunque la biblioteca en tiempo de ejecución de RPC no usa esta cadena, se recomienda establecer la cadena, ya que mejora la capacidad de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="78e64-114">Although the RPC run-time library does not use this string, setting the string is recommended, as it improves manageability of the system.</span></span> <span data-ttu-id="78e64-115">Un administrador del sistema puede usar la cadena para detectar qué puertos usan las aplicaciones, que se pueden usar para determinar qué puertos se van a administrar mediante firewalls.</span><span class="sxs-lookup"><span data-stu-id="78e64-115">A system administrator can use the string to detect which ports are used by which applications, which can then be used to determine which ports to be managed by firewalls.</span></span>

 

 




