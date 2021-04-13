---
title: Tipo de inicio de BITS
description: El tipo de inicio de BITS se retrasa el inicio automático. Antes de Windows Vista, el tipo de inicio de BITS es manual. Cuando se crea un trabajo de BITS, el tipo de inicio cambia a automático. El tipo de inicio vuelve a ser manual cuando todos los trabajos se completan o se cancelan.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1ce1dcd2f939237142a0afd44e49b4b63df419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418389"
---
# <a name="bits-startup-type"></a><span data-ttu-id="48782-106">Tipo de inicio de BITS</span><span class="sxs-lookup"><span data-stu-id="48782-106">BITS Startup Type</span></span>

<span data-ttu-id="48782-107">El **tipo de inicio** de bits es el inicio automático retrasado (si hay trabajos de bits activos) o el inicio de la demanda (si no hay ningún trabajo activo).</span><span class="sxs-lookup"><span data-stu-id="48782-107">The **Startup Type** for BITS is delayed auto-start (if there are active BITS jobs) or demand start (if there are no active jobs).</span></span> <span data-ttu-id="48782-108">Las versiones de Windows anteriores a la actualización de noviembre usaban solo el tipo de inicio de inicio automático retrasado; las versiones anteriores a vista usaban el tipo de inicio manual.</span><span class="sxs-lookup"><span data-stu-id="48782-108">Versions of Windows prior to the November Update used only the delayed auto-start startup type; versions prior to Vista used the manual startup type.</span></span>

<span data-ttu-id="48782-109">No debe establecer el **tipo de inicio** en deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="48782-109">You should not set the **Startup Type** to Disabled.</span></span> <span data-ttu-id="48782-110">Deshabilitar BITS puede interrumpir las aplicaciones que dependen de BITS para transferir archivos.</span><span class="sxs-lookup"><span data-stu-id="48782-110">Disabling BITS may break applications that rely on BITS to transfer files.</span></span>

 

 




