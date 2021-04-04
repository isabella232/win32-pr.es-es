---
description: La \_ exclusión mutua MSIExecute se establece solo al procesar la tabla InstallExecuteSequence, la tabla AdminExecuteSequence o la tabla AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute exclusión mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909173"
---
# <a name="_msiexecute-mutex"></a><span data-ttu-id="92af3-103">\_Exclusión mutua MSIExecute</span><span class="sxs-lookup"><span data-stu-id="92af3-103">\_MSIExecute Mutex</span></span>

<span data-ttu-id="92af3-104">La \_ exclusión mutua MSIExecute se establece solo al procesar la tabla [InstallExecuteSequence](installexecutesequence-table.md), la tabla [AdminExecuteSequence](adminexecutesequence-table.md)o la tabla [AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="92af3-104">The \_MSIExecute Mutex is set only while processing the [InstallExecuteSequence table](installexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

<span data-ttu-id="92af3-105">Dado que no se pueden ejecutar dos instalaciones en el mismo proceso, un intento de llamar a la interfaz de programación de aplicaciones (API) del instalador devuelve la instalación de ERROR \_ \_ que ya se \_ está ejecutando (1618) en dos casos:</span><span class="sxs-lookup"><span data-stu-id="92af3-105">Because two installations cannot be run in the same process, an attempt to call the installer's application programming interface (API) returns ERROR\_INSTALL\_ALREADY\_RUNNING (1618) in two cases:</span></span>

-   <span data-ttu-id="92af3-106">Mientras \_ se establece la exclusión mutua MSIExecute.</span><span class="sxs-lookup"><span data-stu-id="92af3-106">While the \_MSIExecute Mutex is set.</span></span>
-   <span data-ttu-id="92af3-107">Mientras el proceso actual está procesando la [tabla InstallUISequence](installuisequence-table.md) o la [tabla AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="92af3-107">While the current process is processing the [InstallUISequence table](installuisequence-table.md) or [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="92af3-108">Consulte los mensajes de [registro de eventos](event-logging.md) para obtener información sobre la aplicación que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="92af3-108">See the [Event Logging](event-logging.md) messages for information about what application is being installed.</span></span>

<span data-ttu-id="92af3-109">En los casos en los que no resulta práctico devolver un \_ error en la instalación de un error \_ \_ , se puede recuperar el estado actual del servicio de Windows Installer antes de intentar iniciar la instalación mediante la función [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) .</span><span class="sxs-lookup"><span data-stu-id="92af3-109">In cases where it is impractical to return an ERROR\_INSTALL\_ALREADY\_RUNNING error, you can retrieve the current status of the Windows Installer service before attempting to start the installation by using the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function.</span></span> <span data-ttu-id="92af3-110">El servicio Windows Installer se está ejecutando actualmente si el valor del miembro **dwControlsAccepted** de la estructura [**de \_ \_ proceso de estado de servicio**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) devuelto es el **\_ \_ cierre del servicio Accept**.</span><span class="sxs-lookup"><span data-stu-id="92af3-110">The Windows Installer service is currently running if the value of the **dwControlsAccepted** member of the returned [**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) structure is **SERVICE\_ACCEPT\_SHUTDOWN**.</span></span>

<span data-ttu-id="92af3-111">**Windows Installer 2,0:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="92af3-111">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="92af3-112">El uso de la función [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) para recuperar el estado actual del servicio Windows Installer requiere Windows Installer versión 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="92af3-112">The use of the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function to retrieve the current status of the Windows Installer service requires Windows Installer version 3.0 or greater.</span></span>

 

 
