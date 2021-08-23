---
title: Grupos de funciones de administración de redes
description: Las funciones de administración de red se pueden dividir en los siguientes grupos.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e49a8c45c59031a12653f5cb863fef320a33c93bc60cabdd4cd6fb4aece9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012513"
---
# <a name="network-management-function-groups"></a>Grupos de funciones de administración de redes

Las funciones de administración de red se pueden dividir en los siguientes grupos:

-   [Funciones de alerta](alert-functions.md)
-   [Funciones apiBuffer](apibuffer-functions.md)
-   [Funciones del servicio de directorio](directory-service-functions.md)
-   [Sistema de archivos distribuido (Dfs)](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Obtener funciones](get-functions.md)
-   [Funciones de grupo](group-functions.md)
-   [Funciones de grupo local](local-group-functions.md)
-   [Funciones de mensaje](message-functions.md)
-   [Funciones de NetFile](netfile-functions.md)
-   [Funciones de la utilidad remota](remote-utility-functions.md)
-   [Funciones de programación](schedule-functions.md)
-   [Funciones de servidor](server-functions.md)
-   [Funciones de transporte de servidor y estación de trabajo](server-and-workstation-transport-functions.md)
-   [Funciones de sesión](session-functions.md)
-   [Funciones de recurso compartido](share-functions.md)
-   [Funciones de estadísticas](/windows/desktop/NetShare/statistics-functions)
-   [Uso de las funciones](use-functions.md)
-   [Funciones de usuario](user-functions.md)
-   [Funciones modales de usuario](user-modal-functions.md)
-   [Funciones de usuario de estación de trabajo y estación de trabajo](workstation-and-workstation-user-functions.md)

Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de interfaz ADSI para lograr la misma funcionalidad que puede lograr mediante una llamada a determinadas funciones de administración de red. Para obtener más información, vea [Asignación de interfaces ADSI a las funciones de administración de red](mapping-adsi-interfaces-to-the-network-management-functions.md).

El sistema también proporciona un conjunto independiente de la red de funciones de red (funciones[de WNet)](/windows/desktop/WNet/wnet-functions)que permiten que las funciones de red funcionen en distintos productos de proveedores de red. Si la aplicación se puede convertir para usar una función de WNet, debe realizar la conversión. Hay motivos para realizar el cambio:

-   Las funciones de WNet son independientes de la red, mientras que las funciones de administración de red solo funcionan en redes de Microsoft.
-   Es posible que algunas de las funciones no se puedan usar en versiones futuras de los sistemas operativos de Microsoft si se han reemplazado. Microsoft no tiene previsto quitar funciones específicas a menos que haya disponible una funcionalidad equivalente o mejor.

 

 