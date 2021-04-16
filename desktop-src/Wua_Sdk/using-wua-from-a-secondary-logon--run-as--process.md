---
description: Las actualizaciones que requieren la interacción del usuario no se pueden instalar con aplicaciones del agente de Windows Update (WUA) si las aplicaciones de WUA se ejecutan en el contexto del servicio de inicio de sesión secundario.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Usar WUA desde un proceso de inicio de sesión secundario (ejecutar como)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696565"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a><span data-ttu-id="aced2-103">Usar WUA desde un proceso de inicio de sesión secundario (ejecutar como)</span><span class="sxs-lookup"><span data-stu-id="aced2-103">Using WUA from a Secondary Logon (Run As) Process</span></span>

<span data-ttu-id="aced2-104">Las actualizaciones que requieren la interacción del usuario no se pueden instalar con aplicaciones del agente de Windows Update (WUA) si las aplicaciones de WUA se ejecutan en el contexto del servicio de inicio de sesión secundario.</span><span class="sxs-lookup"><span data-stu-id="aced2-104">Updates that require user interaction cannot be installed by Windows Update Agent (WUA) applications if the WUA applications are running in the context of the Secondary Logon service.</span></span>

<span data-ttu-id="aced2-105">Si el proceso que llama a WUA se está ejecutando en el contexto del servicio runas o del servicio de inicio de sesión secundario, se produce un error al intentar instalar una actualización que requiere la interacción del usuario y se devuelve el error de **usuario de Wu \_ E \_ no \_ interactivo \_** .</span><span class="sxs-lookup"><span data-stu-id="aced2-105">If the process that is calling WUA is running in the context of the RunAs service or the Secondary Logon service, an attempt to install an update that requires user interaction fails and returns the **WU\_E\_NO\_INTERACTIVE\_USER** error.</span></span>

<span data-ttu-id="aced2-106">En Microsoft Windows, puede ejecutar programas como un usuario que difiere del usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="aced2-106">In Microsoft Windows, you can run programs as a user who differs from the user who is currently logged on.</span></span> <span data-ttu-id="aced2-107">Para ello, el servicio de inicio de sesión secundario debe estar en ejecución.</span><span class="sxs-lookup"><span data-stu-id="aced2-107">To do this the Secondary Logon service must be running.</span></span>

 

 



