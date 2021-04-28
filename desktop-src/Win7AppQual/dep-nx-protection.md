---
description: Protección de DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protección de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088573"
---
# <a name="depnx-protection"></a><span data-ttu-id="cf083-103">Protección de DEP/NX</span><span class="sxs-lookup"><span data-stu-id="cf083-103">DEP/NX Protection</span></span>

<span data-ttu-id="cf083-104">A partir de Windows Internet Explorer 7 en Windows Vista,  el elemento del panel de control de Internet incluye una opción Habilitar la protección de memoria para ayudar a mitigar los ataques en línea.</span><span class="sxs-lookup"><span data-stu-id="cf083-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="cf083-105">Esta opción también se conoce como *Prevención de ejecución* de datos (DEP) o *No-Execute* (NX).</span><span class="sxs-lookup"><span data-stu-id="cf083-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="cf083-106">Cuando esta opción está habilitada, funciona con el procesador para ayudar a evitar ataques de desbordamiento de búfer bloqueando la ejecución de código desde la memoria marcada como no ejecutable.</span><span class="sxs-lookup"><span data-stu-id="cf083-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="cf083-107">En Windows Internet Explorer 8 en Windows Vista con el sistema operativo Service Pack 1 (SP1) o una versión posterior, esta opción está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cf083-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="cf083-108">DEP/NX no protege contra todas las vulnerabilidades basadas en memoria.</span><span class="sxs-lookup"><span data-stu-id="cf083-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="cf083-109">Pero cuando se combina con otras tecnologías como la selección aleatoria del diseño del espacio de direcciones (ASLR), ayuda a evitar vulnerabilidades comunes de desbordamiento de búfer en Windows Internet Explorer y los complementos que carga.</span><span class="sxs-lookup"><span data-stu-id="cf083-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="cf083-110">No se requiere ninguna interacción adicional del usuario para proporcionar esta protección y no se introducen nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="cf083-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf083-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf083-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf083-112">Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="cf083-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



