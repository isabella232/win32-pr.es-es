---
title: Reflexión de mensajes
description: Reflexión de mensajes
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075043"
---
# <a name="message-reflection"></a><span data-ttu-id="4eff8-103">Reflexión de mensajes</span><span class="sxs-lookup"><span data-stu-id="4eff8-103">Message Reflection</span></span>

<span data-ttu-id="4eff8-104">Se recomienda encarecidamente que un contenedor de controles ActiveX admita la reflexión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4eff8-104">It is strongly recommended that an ActiveX control container supports message reflection.</span></span> <span data-ttu-id="4eff8-105">Esto dará lugar a una operación más eficaz para los controles de subclases.</span><span class="sxs-lookup"><span data-stu-id="4eff8-105">This will result in more efficient operation for subclassed controls.</span></span> <span data-ttu-id="4eff8-106">Si se admite la reflexión de mensajes, se debe admitir la propiedad de ambiente MessageReflect y tener un valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="4eff8-106">If message reflection is supported, the MessageReflect ambient property must be supported and have a value of **TRUE**.</span></span> <span data-ttu-id="4eff8-107">Si un contenedor no implementa la reflexión de mensajes, el CDK de OLE crea dos ventanas para cada control de subclase, para proporcionar la reflexión de mensajes en nombre en el contenedor de control.</span><span class="sxs-lookup"><span data-stu-id="4eff8-107">If a container does not implement message reflection, then the OLE CDK creates two windows for every subclassed control, to provide message reflection on behalf on the control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eff8-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4eff8-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eff8-109">Contenedores</span><span class="sxs-lookup"><span data-stu-id="4eff8-109">Containers</span></span>](containers.md)
</dt> </dl>

 

 




