---
title: Reflexión de mensajes
description: Reflexión de mensajes
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889041"
---
# <a name="message-reflection"></a>Reflexión de mensajes

Se recomienda encarecidamente que un contenedor ActiveX control admita la reflexión de mensajes. Esto dará como resultado una operación más eficaz para los controles con subclases. Si se admite la reflexión de mensajes, la propiedad ambiente MessageReflect debe ser compatible y tener un valor de **TRUE.** Si un contenedor no implementa la reflexión de mensajes, OLE CDK crea dos ventanas para cada control con subclases para proporcionar reflexión de mensajes en nombre del contenedor de controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 




