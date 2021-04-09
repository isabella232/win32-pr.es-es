---
title: Las llamadas remotas al protocolo RPC de SAM están restringidas solo a los administradores locales
description: El protocolo RPC de SAM está restringido. Esto significa que solo los miembros del grupo de administradores locales pueden realizar llamadas remotas en métodos en este protocolo. Active Directory comportamiento del controlador de dominio no se ve afectado.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148861"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Las llamadas remotas al protocolo RPC de SAM están restringidas solo a los administradores locales

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

El protocolo RPC de SAM está restringido. Esto significa que solo los miembros del grupo de administradores locales pueden realizar llamadas remotas en métodos en este protocolo. Active Directory comportamiento del controlador de dominio no se ve afectado.

## <a name="mitigations"></a>Mitigaciones

Asegúrese de que los usuarios adecuados estén configurados como administradores en el equipo. La ACL utilizada para la comprobación de acceso se puede configurar mediante la Directiva de grupo.

 

 




