---
description: Un proveedor de red es un archivo DLL que permite al Windows operativo interactuar con otros tipos de redes, como Asín. Es un cliente del controlador Windows WNet.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API del proveedor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173418"
---
# <a name="network-provider-api"></a>API del proveedor de red

Un proveedor de red es un archivo DLL que permite al Windows operativo interactuar con otros tipos de redes, como Asín. Es un cliente del controlador Windows WNet. Un proveedor de red implementa acciones específicas de la red, como realizar una conexión, y expone una interfaz común para Windows. Esta interfaz se denomina API de proveedor de red y consta de funciones implementadas por el proveedor de red. Puede crear un archivo DLL de proveedor de red para admitir nuevos protocolos de red.

Dado que cada red expone una interfaz común a través de su proveedor, Windows puede interactuar con varios tipos de redes sin conocer los detalles de implementación específicos de la red.

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

 

 
