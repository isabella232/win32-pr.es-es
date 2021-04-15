---
title: Detalles de implementación de DVC
description: Esta sección contiene información sobre cómo escribir un módulo de cliente de canal virtual dinámico (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676137"
---
# <a name="dvc-implementation-details"></a><span data-ttu-id="dd0d5-103">Detalles de implementación de DVC</span><span class="sxs-lookup"><span data-stu-id="dd0d5-103">DVC Implementation Details</span></span>

<span data-ttu-id="dd0d5-104">Esta sección contiene información sobre cómo escribir un módulo de cliente de canal virtual dinámico (DVC).</span><span class="sxs-lookup"><span data-stu-id="dd0d5-104">This section contains information about how to write a dynamic virtual channel (DVC) client module.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dd0d5-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="dd0d5-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="dd0d5-106">Escritura de un módulo DVC de cliente</span><span class="sxs-lookup"><span data-stu-id="dd0d5-106">Writing a Client DVC Module</span></span>](writing-a-client-dvc-component.md)
</dt> <dd>

<span data-ttu-id="dd0d5-107">Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="dd0d5-107">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="dd0d5-108">Registro del complemento DVC</span><span class="sxs-lookup"><span data-stu-id="dd0d5-108">DVC plug-in registration</span></span>](dvc-plug-in-registration.md)
</dt> <dd>

<span data-ttu-id="dd0d5-109">Describe la sintaxis de la entrada del complemento de canal virtual dinámico (DVC) del cliente Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="dd0d5-109">Describes syntax for the dynamic virtual channel (DVC) plug-in entry for the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="dd0d5-110">Inicio de un agente de escucha de DVC</span><span class="sxs-lookup"><span data-stu-id="dd0d5-110">Starting a DVC Listener</span></span>](starting-a-dvc-listener.md)
</dt> <dd>

<span data-ttu-id="dd0d5-111">Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y servidor de Conexión a Escritorio remoto (RDC), un agente de escucha de DVC debe estar en ejecución y en un estado de escucha.</span><span class="sxs-lookup"><span data-stu-id="dd0d5-111">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

</dd> <dt>

[<span data-ttu-id="dd0d5-112">Aceptación de una conexión</span><span class="sxs-lookup"><span data-stu-id="dd0d5-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> <dd>

<span data-ttu-id="dd0d5-113">En algún momento, el cliente del canal virtual dinámico (DVC) solicitará una conexión con el agente de escucha de DVC.</span><span class="sxs-lookup"><span data-stu-id="dd0d5-113">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span>

</dd> <dt>

[<span data-ttu-id="dd0d5-114">Escribir datos mediante un canal de DVC</span><span class="sxs-lookup"><span data-stu-id="dd0d5-114">Writing Data by Using a DVC Channel</span></span>](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

<span data-ttu-id="dd0d5-115">Escritorio remoto la escritura de datos del canal mediante el uso de un canal virtual dinámico (DVC) es simétrica tanto para el servidor host de sesión de escritorio remoto (host de sesión de RD) como para el cliente.</span><span class="sxs-lookup"><span data-stu-id="dd0d5-115">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span>

</dd> <dt>

[<span data-ttu-id="dd0d5-116">Pruebas y depuración</span><span class="sxs-lookup"><span data-stu-id="dd0d5-116">Testing and Debugging</span></span>](testing-and-debugging.md)
</dt> <dd>

<span data-ttu-id="dd0d5-117">Hay un agente de escucha de "Eco" implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y escuchando conexiones entrantes.</span><span class="sxs-lookup"><span data-stu-id="dd0d5-117">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span>

</dd> <dt>

[<span data-ttu-id="dd0d5-118">Ejemplo de complemento de cliente de DVC</span><span class="sxs-lookup"><span data-stu-id="dd0d5-118">DVC Client Plug-in Example</span></span>](dvc-client-plug-in-example.md)
</dt> <dd>

<span data-ttu-id="dd0d5-119">Código de ejemplo de C++ que muestra cómo crear un complemento de canal virtual dinámico (DVC) del cliente Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="dd0d5-119">C++ code sample that shows how to create a Remote Desktop Connection (RDC) client dynamic virtual channel (DVC) plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="dd0d5-120">Ejemplo del módulo de servidor DVC</span><span class="sxs-lookup"><span data-stu-id="dd0d5-120">DVC Server Module Example</span></span>](dvc-server-component-example.md)
</dt> <dd>

<span data-ttu-id="dd0d5-121">Código de ejemplo de C++ que muestra cómo crear el módulo de canal virtual dinámico (DVC) del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="dd0d5-121">C++ code sample that shows how to create the server-side dynamic virtual channel (DVC) module.</span></span>

</dd> </dl>

 

 




