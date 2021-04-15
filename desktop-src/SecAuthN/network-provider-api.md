---
description: Un proveedor de red es un archivo DLL que permite al sistema operativo Windows interactuar con otros tipos de redes, como Novell. Es un cliente del controlador Windows WNet.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API de proveedor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648559"
---
# <a name="network-provider-api"></a>API de proveedor de red

Un proveedor de red es un archivo DLL que permite al sistema operativo Windows interactuar con otros tipos de redes, como Novell. Es un cliente del controlador Windows WNet. Un proveedor de red implementa acciones específicas de la red, como establecer una conexión y expone una interfaz común a Windows. Esta interfaz se denomina API de proveedor de red y consta de funciones implementadas por el proveedor de red. Puede crear un archivo DLL de proveedor de red para admitir nuevos protocolos de red.

Dado que cada red expone una interfaz común a través de su proveedor, Windows puede interactuar con varios tipos de redes sin conocer los detalles de la implementación específica de la red.

El [*enrutador de proveedor múltiple*](../secgloss/m-gly.md) (MPR) controla la comunicación con todos los diversos proveedores de red del sistema y presenta una red integrada al usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores de red](network-providers.md)
</dt> <dt>

[Administrador de credenciales](credential-manager.md)
</dt> <dt>

[Enrutador de varios proveedores](multiple-provider-router.md)
</dt> <dt>

[Funciones implementadas por los proveedores de red](functions-implemented-by-network-providers.md)
</dt> <dt>

[API de administración de credenciales](credential-management-api.md)
</dt> <dt>

[API de notificación de conexión](connection-notification-api.md)
</dt> </dl>

 

 
