---
title: Pruebas y depuración
description: Hay un 0034; echo \ 0034; agente de escucha implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y escuchando conexiones entrantes.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676118"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="82e9f-103">Pruebas y depuración</span><span class="sxs-lookup"><span data-stu-id="82e9f-103">Testing and Debugging</span></span>

<span data-ttu-id="82e9f-104">Hay un agente de escucha de "Eco" implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y escuchando conexiones entrantes.</span><span class="sxs-lookup"><span data-stu-id="82e9f-104">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span> <span data-ttu-id="82e9f-105">Al escribir el lado del servidor de un módulo de canal virtual dinámico (DVC), como una prueba rápida, puede abrir un punto de conexión denominado "ECHO".</span><span class="sxs-lookup"><span data-stu-id="82e9f-105">When you are writing the server side of a dynamic virtual channel (DVC) module, as a quick test you can open an endpoint named "ECHO".</span></span> <span data-ttu-id="82e9f-106">Cualquier escritura en un canal del que se crean instancias desde este punto de conexión dará como resultado la recepción de los mismos datos.</span><span class="sxs-lookup"><span data-stu-id="82e9f-106">Any write to a channel that is instantiated from this endpoint will result in the receipt of the same data.</span></span>

<span data-ttu-id="82e9f-107">Puede usar esta técnica para probar una implementación de entrada/salida (e/s) del módulo de servidor, para medir el tiempo de respuesta de un complemento de cliente Conexión a Escritorio remoto (RDC) o para medir el retraso de red para el cliente Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="82e9f-107">You can use this technique to test an input/output (I/O) implementation of the server-side module, to measure the response time for a Remote Desktop Connection (RDC) client plug-in, or to measure the network delay for the Remote Desktop Connection (RDC) client.</span></span> <span data-ttu-id="82e9f-108">No hay ninguna limitación en la cantidad de datos que se pueden enviar a través de este canal.</span><span class="sxs-lookup"><span data-stu-id="82e9f-108">There is no limitation on the amount of data that can be sent over this channel.</span></span>

 

 




