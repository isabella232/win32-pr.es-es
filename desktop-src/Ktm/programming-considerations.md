---
description: 'Más información sobre: consideraciones de programación para escribir administradores de recursos'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Consideraciones de programación para escribir administradores de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687703"
---
# <a name="programming-considerations-for-writing-resource-managers"></a><span data-ttu-id="343e3-103">Consideraciones de programación para escribir administradores de recursos</span><span class="sxs-lookup"><span data-stu-id="343e3-103">Programming Considerations For Writing Resource Managers</span></span>

<span data-ttu-id="343e3-104">Al usar la API del administrador de transacciones de kernel para agregar compatibilidad con transacciones a las aplicaciones, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="343e3-104">When using the Kernel Transaction Manager API to add transaction support to your applications, consider the following:</span></span>

-   <span data-ttu-id="343e3-105">Al escribir su propio administrador de recursos, debe tener un buen conocimiento práctico de los protocolos y las técnicas de administración de transacciones.</span><span class="sxs-lookup"><span data-stu-id="343e3-105">When you are writing your own resource manager, you should have a good, working knowledge of transaction management techniques and protocols.</span></span>
-   <span data-ttu-id="343e3-106">Si no escribe los administradores de recursos correctamente, puede dañar sus propios datos con operaciones de recuperación que se administran de forma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="343e3-106">If you do not write resource managers correctly, you can corrupt your own data with improperly handled recovery operations.</span></span> <span data-ttu-id="343e3-107">También puede anclar el final del registro de transacciones y rellenar el sistema de archivos con registros de transacciones.</span><span class="sxs-lookup"><span data-stu-id="343e3-107">You can also pin the tail of transaction log and fill up your file system with transaction logs.</span></span>
-   <span data-ttu-id="343e3-108">Si la Directiva de tamaño del registro no está configurada para evitar que el registro aumente de tamaño, el administrador de recursos no detendrá las transacciones.</span><span class="sxs-lookup"><span data-stu-id="343e3-108">If your log size policy is not set to prevent the log from increasing in size, your resource manager will not stop transactions.</span></span> <span data-ttu-id="343e3-109">El administrador de recursos debe detener la actualización del sistema para que no desborda los recursos del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="343e3-109">Your resource manager must stop updating the system so it does not overrun the file system resources.</span></span>
-   <span data-ttu-id="343e3-110">Los administradores de recursos deben utilizar listas de control de acceso (ACL) para controlar el acceso a los archivos de registro. de lo contrario, es posible que se produzcan ataques de denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="343e3-110">Resource managers should use access control lists (ACLs) to control access to the log files; otherwise, denial of service attacks are possible.</span></span>
-   <span data-ttu-id="343e3-111">Cualquier participante de Resource Manager o de transacción que almacene los datos en caché debe darse de alta para las notificaciones previas a la preparación.</span><span class="sxs-lookup"><span data-stu-id="343e3-111">Any resource manager or transaction participant that caches data must enlist for pre-prepare notifications.</span></span> <span data-ttu-id="343e3-112">Cuando se recibe una notificación previa a la preparación, debe vaciar todos los datos para que los administradores de recursos de nivel inferior puedan inscribirse antes de la fase de preparación.</span><span class="sxs-lookup"><span data-stu-id="343e3-112">When a pre-prepare notification is received, you must flush all your data, so that any downstream resource managers can enlist before the prepare phase.</span></span> <span data-ttu-id="343e3-113">Cualquier trabajo adicional en esa transacción no se debe almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="343e3-113">Any further work in that transaction must not be cached.</span></span>
-   <span data-ttu-id="343e3-114">No cierre un identificador de inscripción mientras la transacción todavía esté activa; Esto hará que se revierta la transacción.</span><span class="sxs-lookup"><span data-stu-id="343e3-114">Do not close an enlistment handle while the transaction is still active; this will cause the transaction to be rolled back.</span></span>

 

 



