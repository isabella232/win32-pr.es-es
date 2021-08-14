---
title: Las llamadas remotas al protocolo RPC SAM están restringidas solo a los administradores locales
description: El protocolo RPC SAM está restringido. Esto significa que solo los miembros del grupo administrador local pueden realizar llamadas remotas a métodos de este protocolo. Active Directory comportamiento del controlador de dominio no se ven afectados.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee009e3f346c7e7a179a324ec68834999acd711934ab5c64a3cae1845372dbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211340"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Las llamadas remotas al protocolo RPC SAM están restringidas solo a los administradores locales

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

El protocolo RPC SAM está restringido. Esto significa que solo los miembros del grupo administrador local pueden realizar llamadas remotas a métodos de este protocolo. Active Directory comportamiento del controlador de dominio no se ven afectados.

## <a name="mitigations"></a>Mitigaciones

Asegúrese de que los usuarios adecuados están establecidos como administradores en el equipo. La ACL usada para la comprobación de acceso se puede configurar a través de la directiva de grupo.

 

 




