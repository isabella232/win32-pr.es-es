---
title: Comprobaciones de kernel para controladores no firmados por WHQL
description: En el caso de los dispositivos que limpian Windows 10 y donde el arranque seguro está activado (tenga en cuenta que esto es estándar para todos los dispositivos nuevos desde el lanzamiento de Windows 8,0), todos los controladores nuevos deben estar firmados por WHQL/Sysdev en lugar de simplemente usar certificados con firma cruzada.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418985"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a><span data-ttu-id="b6538-103">Comprobaciones de kernel para controladores no firmados por WHQL</span><span class="sxs-lookup"><span data-stu-id="b6538-103">Kernel checks for non-WHQL signed drivers</span></span>

<span data-ttu-id="b6538-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b6538-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b6538-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b6538-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b6538-106">En el caso de los dispositivos que limpian Windows 10 y donde el arranque seguro está activado (tenga en cuenta que esto es estándar para todos los dispositivos nuevos desde el lanzamiento de Windows 8,0), todos los controladores nuevos deben estar firmados por WHQL/Sysdev en lugar de simplemente usar certificados con firma cruzada.</span><span class="sxs-lookup"><span data-stu-id="b6538-106">For devices that clean install Windows 10, and where Secure Boot is on (note that this is standard for all new devices since the release of Windows 8.0), all new drivers must be signed by WHQL/Sysdev rather than just use cross-signed certificates.</span></span> <span data-ttu-id="b6538-107">Los dispositivos que se actualizan y los casos en los que los controladores se han firmado con un certificado cruzado antes de que esta directiva entrara en vigor se excluyen de esta directiva para garantizar la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="b6538-107">Devices that are upgraded and cases where drivers have been signed with a cross-cert before this policy went into effect are excluded from this policy to ensure backwards compatibility.</span></span> <span data-ttu-id="b6538-108">Esta Directiva se anunció el 2015 de abril, pero se aplicará con la edición de aniversario de Windows, publicada en agosto de 2016.</span><span class="sxs-lookup"><span data-stu-id="b6538-108">This policy was announced April 2015, however it will be enforced with the Windows Anniversary Edition, released August 2016.</span></span>

<span data-ttu-id="b6538-109">En los casos en los que un controlador no está firmado correctamente, se emitirá como una notificación de PCA de que los controladores se bloquean cuando no supera los requisitos de firma.</span><span class="sxs-lookup"><span data-stu-id="b6538-109">In cases where a driver is not signed correctly, it will manifest as a PCA notification that the driver(s) is blocked when it doesn’t pass signature requirements.</span></span> <span data-ttu-id="b6538-110">Esto evita que una experiencia de usuario desconectada posterior del controlador se bloquee en el kernel de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="b6538-110">This prevents a later disconnected user experience of the driver being blocked in kernel transparently.</span></span>

<span data-ttu-id="b6538-111">Para obtener más información, consulte [esta entrada de blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), que anuncia el cambio de firma del controlador.</span><span class="sxs-lookup"><span data-stu-id="b6538-111">For more information, please refer to [this blog post](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), which announces the driver signing change.</span></span>

 

 




