---
description: Con un contexto orientado a la conexión, el autor de la llamada de la función es responsable de dar formato a los mensajes. El autor de la llamada se basa en el paquete de seguridad para autenticar las conexiones y garantizar la integridad de determinadas partes del mensaje.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Contextos de Connection-Oriented
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155900"
---
# <a name="connection-oriented-contexts"></a>Contextos de Connection-Oriented

Con un [*contexto*](/windows/desktop/SecGloss/c-gly)orientado a la conexión, el autor de la llamada de la función es responsable de dar formato a los mensajes. El autor de la llamada se basa en el [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) para autenticar las conexiones y garantizar la integridad de determinadas partes del mensaje.

La mayoría de las opciones de contexto están disponibles para los contextos orientados a la conexión. Estas opciones incluyen la autenticación mutua, la detección de reproducción y la detección de secuencias, tal como se describe en [requisitos de contexto](context-requirements.md).

Un paquete de seguridad establece la \_ marca de conexión de la marca SECPKG \_ para indicar que admite la semántica orientada a la conexión.

 

 
