---
title: Reflexión de mensajes
description: Reflexión de mensajes
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9191e0e189f8653518aaabb3c31785cde960538b0828d56669096ebf1d63f1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048053"
---
# <a name="message-reflection"></a>Reflexión de mensajes

Se recomienda encarecidamente que un contenedor ActiveX control admita la reflexión de mensajes. Esto dará como resultado un funcionamiento más eficaz para los controles con subclases. Si se admite la reflexión de mensajes, la propiedad ambiente MessageReflect debe ser compatible y tener un valor **de TRUE.** Si un contenedor no implementa la reflexión de mensajes, OLE CDK crea dos ventanas para cada control con subclases para proporcionar reflexión de mensajes en nombre del contenedor de controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 




