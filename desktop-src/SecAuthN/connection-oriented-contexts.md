---
description: Con un contexto orientado a la conexión, el autor de la llamada de la función es responsable de dar formato a los mensajes. El autor de la llamada se basa en el paquete de seguridad para autenticar las conexiones y garantizar la integridad de partes específicas del mensaje.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Connection-Oriented contextos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b889b948f41916e3e741311ea4289c4214cdc256084af7bb455265dd69a7d00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141168"
---
# <a name="connection-oriented-contexts"></a>Connection-Oriented contextos

Con un contexto orientado a la [*conexión,*](/windows/desktop/SecGloss/c-gly)el autor de la llamada de la función es responsable de dar formato a los mensajes. El autor de la llamada se basa en el paquete [*de seguridad para*](/windows/desktop/SecGloss/s-gly) autenticar las conexiones y garantizar la integridad de partes específicas del mensaje.

La mayoría de las opciones de contexto están disponibles para los contextos orientados a la conexión. Estas opciones incluyen la autenticación mutua, la detección de reproducción y la detección de secuencias, como se describe en [Requisitos de contexto](context-requirements.md).

Un paquete de seguridad establece la marca SECPKG FLAG CONNECTION para indicar que admite la semántica orientada \_ \_ a la conexión.

 

 
