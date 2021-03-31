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
# <a name="message-reflection"></a>Reflexión de mensajes

Se recomienda encarecidamente que un contenedor de controles ActiveX admita la reflexión de mensajes. Esto dará lugar a una operación más eficaz para los controles de subclases. Si se admite la reflexión de mensajes, se debe admitir la propiedad de ambiente MessageReflect y tener un valor de **true**. Si un contenedor no implementa la reflexión de mensajes, el CDK de OLE crea dos ventanas para cada control de subclase, para proporcionar la reflexión de mensajes en nombre en el contenedor de control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 




