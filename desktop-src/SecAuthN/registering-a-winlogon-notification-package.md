---
description: La información acerca de los paquetes de notificación Winlogon se almacena en el registro. Las entradas del registro especifican el nombre del paquete de notificación, el nombre del archivo DLL que implementa el paquete y los nombres de las funciones que controlan los eventos de Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrar un paquete de notificación de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276686"
---
# <a name="registering-a-winlogon-notification-package"></a><span data-ttu-id="a9658-104">Registrar un paquete de notificación de Winlogon</span><span class="sxs-lookup"><span data-stu-id="a9658-104">Registering a Winlogon Notification Package</span></span>

<span data-ttu-id="a9658-105">La información acerca de los paquetes de notificación [*Winlogon*](../secgloss/w-gly.md) se almacena en el registro.</span><span class="sxs-lookup"><span data-stu-id="a9658-105">Information about [*Winlogon*](../secgloss/w-gly.md) notification packages is stored in the registry.</span></span> <span data-ttu-id="a9658-106">Las entradas del registro especifican el nombre del paquete de notificación, el nombre del archivo DLL que implementa el paquete y los nombres de las funciones que controlan los eventos de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="a9658-106">Registry entries specify the name of the notification package, the name of the DLL that implements the package, and the names of the functions that handle Winlogon events.</span></span>

<span data-ttu-id="a9658-107">Cuando se inicia Winlogon, comprueba el registro y carga los paquetes de notificación registrados.</span><span class="sxs-lookup"><span data-stu-id="a9658-107">When Winlogon starts, it checks the registry and loads any registered notification packages.</span></span> <span data-ttu-id="a9658-108">Cuando se produce un evento, Winlogon llama a la función de controlador de eventos designada para cada paquete.</span><span class="sxs-lookup"><span data-stu-id="a9658-108">When an event occurs, Winlogon calls the designated event handler function for each package.</span></span> <span data-ttu-id="a9658-109">Se pueden registrar varios paquetes de notificación de eventos en un sistema.</span><span class="sxs-lookup"><span data-stu-id="a9658-109">Multiple event notification packages may be registered on a system.</span></span>

<span data-ttu-id="a9658-110">Para registrar el paquete de notificación, cree una clave del registro denominada **Notify** como subclave de la siguiente clave del registro y agregue los valores detallados en [las entradas del registro](registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="a9658-110">To register your notification package, create a registry key named **Notify** as a subkey of the following registry key and add the values detailed in [Registry Entries](registry-entries.md).</span></span>

<span data-ttu-id="a9658-111">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**</span><span class="sxs-lookup"><span data-stu-id="a9658-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Winlogon**</span></span>

 

 
