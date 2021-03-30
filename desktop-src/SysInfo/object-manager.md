---
description: Un objeto consta de un encabezado estándar y atributos específicos del objeto. Dado que todos los objetos tienen la misma estructura, hay un único administrador de objetos en Windows que mantiene todos los objetos.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Administrador de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002457"
---
# <a name="object-manager"></a><span data-ttu-id="60ad2-104">Administrador de objetos</span><span class="sxs-lookup"><span data-stu-id="60ad2-104">Object Manager</span></span>

<span data-ttu-id="60ad2-105">Un objeto consta de un encabezado estándar y atributos específicos del objeto.</span><span class="sxs-lookup"><span data-stu-id="60ad2-105">An object consists of a standard header and object-specific attributes.</span></span> <span data-ttu-id="60ad2-106">Dado que todos los objetos tienen la misma estructura, hay un único administrador de objetos en Windows que mantiene todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="60ad2-106">Because all objects have the same structure, there is a single object manager in Windows that maintains all objects.</span></span>

<span data-ttu-id="60ad2-107">El encabezado del objeto incluye elementos como el nombre del objeto, de modo que otros procesos puedan hacer referencia al objeto por nombre, y un descriptor de seguridad, para que el administrador de objetos pueda controlar qué procesos tienen acceso al recurso del sistema.</span><span class="sxs-lookup"><span data-stu-id="60ad2-107">The object header includes items such as the object name, so that other processes can reference the object by name, and a security descriptor, so that the object manager can control which processes access the system resource.</span></span>

<span data-ttu-id="60ad2-108">Entre las tareas que realiza el administrador de objetos se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="60ad2-108">The tasks that the object manager performs include the following:</span></span>

-   <span data-ttu-id="60ad2-109">Creación de objetos</span><span class="sxs-lookup"><span data-stu-id="60ad2-109">Creating objects</span></span>
-   <span data-ttu-id="60ad2-110">Comprobar que un proceso tiene el derecho a usar el objeto</span><span class="sxs-lookup"><span data-stu-id="60ad2-110">Verifying that a process has the right to use the object</span></span>
-   <span data-ttu-id="60ad2-111">Crear identificadores de objeto y devolverlos al autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="60ad2-111">Creating object handles and returning them to the caller</span></span>
-   <span data-ttu-id="60ad2-112">Mantenimiento de cuotas de recursos</span><span class="sxs-lookup"><span data-stu-id="60ad2-112">Maintaining resource quotas</span></span>
-   <span data-ttu-id="60ad2-113">Crear identificadores duplicados</span><span class="sxs-lookup"><span data-stu-id="60ad2-113">Creating duplicate handles</span></span>
-   <span data-ttu-id="60ad2-114">Controladores de cierre de objetos</span><span class="sxs-lookup"><span data-stu-id="60ad2-114">Closing handles to objects</span></span>

 

 



