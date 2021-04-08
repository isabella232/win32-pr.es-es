---
title: Grupos de funciones de administración de red
description: Las funciones de administración de red se pueden dividir en los siguientes grupos.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bce5c0fb3dd70facb0ebbbb2479b968d428c49e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077922"
---
# <a name="network-management-function-groups"></a>Grupos de funciones de administración de red

Las funciones de administración de red se pueden dividir en los siguientes grupos:

-   [Funciones de alerta](alert-functions.md)
-   [Funciones de ApiBuffer](apibuffer-functions.md)
-   [Funciones del servicio de directorio](directory-service-functions.md)
-   [Funciones de Sistema de archivos distribuido (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Funciones Get](get-functions.md)
-   [Funciones de grupo](group-functions.md)
-   [Funciones de grupo local](local-group-functions.md)
-   [Funciones de mensaje](message-functions.md)
-   [Funciones de NetFile](netfile-functions.md)
-   [Funciones de utilidad remota](remote-utility-functions.md)
-   [Funciones de programación](schedule-functions.md)
-   [Funciones de servidor](server-functions.md)
-   [Funciones de transporte de servidor y estación de trabajo](server-and-workstation-transport-functions.md)
-   [Funciones de sesión](session-functions.md)
-   [Funciones de uso compartido](share-functions.md)
-   [Funciones de estadísticas](/windows/desktop/NetShare/statistics-functions)
-   [Uso de las funciones](use-functions.md)
-   [Funciones de usuario](user-functions.md)
-   [Funciones modales de usuario](user-modal-functions.md)
-   [Funciones de usuario de estación de trabajo y estación de trabajo](workstation-and-workstation-user-functions.md)

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz ADSI para lograr la misma funcionalidad que puede lograr mediante una llamada a determinadas funciones de administración de red. Para obtener más información, consulte [asignación de interfaces ADSI a las funciones de administración de redes](mapping-adsi-interfaces-to-the-network-management-functions.md).

El sistema también proporciona un conjunto independiente de la red de funciones de red ([funciones de WNet](/windows/desktop/WNet/wnet-functions)) que permiten a las funciones de red trabajar en productos de distintos proveedores de red. Si la aplicación se puede convertir para usar una función de WNet, debe realizar la conversión. Hay motivos para hacer el cambio:

-   Las funciones de WNet son independientes de la red, mientras que las funciones de administración de red solo funcionan en redes de Microsoft.
-   Es posible que algunas de las funciones no se admitan en futuras versiones de los sistemas operativos de Microsoft si se han sustituido. Microsoft no planea quitar funciones específicas a menos que esté disponible una funcionalidad equivalente o mejor.

 

 