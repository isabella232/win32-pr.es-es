---
description: Un proveedor de red es un archivo DLL que permite al Windows operativo interactuar con otros tipos de redes, como Después. Es un cliente del controlador Windows WNet.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API del proveedor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359104da668ee3dbe63efa538b58f224f93f52575ed20992fced0e10517fe5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921331"
---
# <a name="network-provider-api"></a>API del proveedor de red

Un proveedor de red es un archivo DLL que permite al Windows operativo interactuar con otros tipos de redes, como Después. Es un cliente del controlador Windows WNet. Un proveedor de red implementa acciones específicas de la red, como realizar una conexión, y expone una interfaz común para Windows. Esta interfaz se denomina API de proveedor de red y consta de funciones implementadas por el proveedor de red. Puede crear un archivo DLL de proveedor de red para admitir nuevos protocolos de red.

Dado que cada red expone una interfaz común a través de su proveedor, Windows puede interactuar con varios tipos de redes sin conocer sus detalles de implementación específicos de la red.

El [*enrutador de varios*](../secgloss/m-gly.md) proveedores (MPR) controla la comunicación con todos los distintos proveedores de red del sistema y presenta una red integrada al usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores de red](network-providers.md)
</dt> <dt>

[Administrador de credenciales](credential-manager.md)
</dt> <dt>

[Enrutador de varios proveedores](multiple-provider-router.md)
</dt> <dt>

[Funciones implementadas por proveedores de red](functions-implemented-by-network-providers.md)
</dt> <dt>

[Credenciales API de Administración](credential-management-api.md)
</dt> <dt>

[Conexión API de notificación](connection-notification-api.md)
</dt> </dl>

 

 
