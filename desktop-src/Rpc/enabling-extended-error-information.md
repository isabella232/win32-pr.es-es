---
title: Habilitar información de error extendida
description: Habilitar la información de error extendida para la llamada a procedimiento remoto (RPC).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269033"
---
# <a name="enabling-extended-error-information"></a><span data-ttu-id="f1c40-103">Habilitar información de error extendida</span><span class="sxs-lookup"><span data-stu-id="f1c40-103">Enabling Extended Error Information</span></span>

<span data-ttu-id="f1c40-104">Para habilitar la información de error extendida, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="f1c40-104">To enable extended error information, take the following steps:</span></span>

<span data-ttu-id="f1c40-105">Abra la Directiva del equipo local mediante la interfaz gpedit. msc.</span><span class="sxs-lookup"><span data-stu-id="f1c40-105">Open the local machine policy using the gpedit.msc interface.</span></span>

<span data-ttu-id="f1c40-106">Vaya a la Directiva que se encuentra en configuración del equipo/Plantillas administrativas/sistema/llamada a procedimiento remoto/compatibilidad con la solución de problemas de RPC/propagación de la información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="f1c40-106">Navigate to the policy located at Computer Configuration/Administrative Templates/System/Remote Procedure Call/Rpc Troubleshooting Support/Propagation of extended error information</span></span>

<span data-ttu-id="f1c40-107">Habilite la Directiva y establezca la **propagación del campo de información de error extendida** en "activado".</span><span class="sxs-lookup"><span data-stu-id="f1c40-107">Enable the policy, and set the field **Propagation of extended error information** to "On".</span></span>

<span data-ttu-id="f1c40-108">Este proceso convierte la propagación de la información de error extendida en para todos los procesos del equipo.</span><span class="sxs-lookup"><span data-stu-id="f1c40-108">This process turns the propagation of extended error information on for all processes on the machine.</span></span>

<span data-ttu-id="f1c40-109">Para habilitar la información de error extendida solo para determinados procesos de un equipo, o para deshabilitarlo solo en determinados procesos del equipo, use las opciones **desactivado con excepciones** o **con excepciones** .</span><span class="sxs-lookup"><span data-stu-id="f1c40-109">To enable extended error information for only certain processes on a computer, or to disable it for only certain processes on the computer, use the **Off with exceptions** or **On with exceptions** options.</span></span> <span data-ttu-id="f1c40-110">Ambas opciones usan las **excepciones de información de errores extendidos** de campo para especificar los procesos que tienen la configuración predeterminada y los procesos que tienen la misma configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f1c40-110">Both options use the field **Extended Error Information Exceptions** to specify which processes have the default setting, and which processes have the opposite of the default setting.</span></span> <span data-ttu-id="f1c40-111">**Excepciones de información de error extendida** contiene una lista de nombres de proceso.</span><span class="sxs-lookup"><span data-stu-id="f1c40-111">**Extended Error Information Exceptions** contains a list of process names.</span></span>

<span data-ttu-id="f1c40-112">Si la línea de comandos de un proceso comienza con una cadena que se encuentra en las **excepciones de información de error extendida**, el proceso recibirá la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f1c40-112">If the command line of a process starts with a string that is in the **Extended Error Information Exceptions**, the process will receive the opposite of the default setting.</span></span> <span data-ttu-id="f1c40-113">Por ejemplo, si desea que todo el proceso del equipo propague información extendida de errores, excepto para LSASS y el proceso llamado **servidor seguro**, establezca la **propagación de la información de errores extendida** en **activado con excepciones** y especifique en el campo **excepciones de información de error extendida** la siguiente cadena: LSASS "servidor seguro".</span><span class="sxs-lookup"><span data-stu-id="f1c40-113">For example, if you want all the process on your computer to propagate extended error information, except for lsass and the process called **Secure Server**, set the **Propagation of extended error information** to **On with exceptions**, and specify in the **Extended Error Information Exceptions** field the following string: lsass "Secure Server".</span></span>

<span data-ttu-id="f1c40-114">Las cadenas se pueden incluir entre comillas dobles, pero es opcional si no hay ningún espacio en la cadena.</span><span class="sxs-lookup"><span data-stu-id="f1c40-114">Strings can be enclosed with double quotes, but doing so is optional if there are no spaces in the string.</span></span> <span data-ttu-id="f1c40-115">Además, se puede especificar el principio de la línea de comandos del proceso.</span><span class="sxs-lookup"><span data-stu-id="f1c40-115">Also, the beginning of the process command line can be specified.</span></span> <span data-ttu-id="f1c40-116">Por ejemplo, si se especifica **OFF con excepciones** en el campo **propagación de información de error extendida** , y en el campo **excepciones de información de error extendida** se especifica lo siguiente: Win.</span><span class="sxs-lookup"><span data-stu-id="f1c40-116">For example, if **Off with exceptions** is specified in the **Propagation of extended error information** field, and in the **Extended Error Information Exceptions** field the following is specified: win.</span></span>

<span data-ttu-id="f1c40-117">Cada proceso que comienza por "Win" propaga información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="f1c40-117">Each process that begins with "win" propagates extended error information.</span></span> <span data-ttu-id="f1c40-118">En muchos equipos, por ejemplo, estos procesos se winlogon.exe y WINWORD.EXE.</span><span class="sxs-lookup"><span data-stu-id="f1c40-118">On many computers, for example, those processes would be winlogon.exe and WINWORD.EXE.</span></span>

 

 




