---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protección de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913373"
---
# <a name="depnx-protection"></a><span data-ttu-id="ebc42-103">Protección de DEP/NX</span><span class="sxs-lookup"><span data-stu-id="ebc42-103">DEP/NX Protection</span></span>

<span data-ttu-id="ebc42-104">A partir de Windows Internet Explorer 7 en Windows Vista, el elemento del panel de control de Internet incluye una opción **Habilitar protección de memoria** para ayudar a mitigar los ataques en línea.</span><span class="sxs-lookup"><span data-stu-id="ebc42-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="ebc42-105">Esta opción también se conoce como *prevención de ejecución de datos* (DEP) o *no ejecutar* (NX).</span><span class="sxs-lookup"><span data-stu-id="ebc42-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="ebc42-106">Cuando esta opción está habilitada, funciona con el procesador para ayudar a evitar ataques por desbordamiento del búfer al bloquear la ejecución del código de la memoria marcada como no ejecutable.</span><span class="sxs-lookup"><span data-stu-id="ebc42-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="ebc42-107">En Windows Internet Explorer 8 en el sistema operativo Windows Vista con Service Pack 1 (SP1) o una versión posterior, esta opción está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ebc42-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="ebc42-108">DEP/NX no protege contra todas las vulnerabilidades basadas en memoria.</span><span class="sxs-lookup"><span data-stu-id="ebc42-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="ebc42-109">Sin embargo, cuando se combina con otras tecnologías, como la selección aleatoria del diseño del espacio de direcciones (ASLR), ayuda a evitar vulnerabilidades de desbordamiento de búfer comunes en Windows Internet Explorer y en los complementos que se cargan.</span><span class="sxs-lookup"><span data-stu-id="ebc42-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="ebc42-110">No se requiere ninguna interacción del usuario adicional para proporcionar esta protección y no se introducen nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="ebc42-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebc42-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebc42-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc42-112">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="ebc42-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



