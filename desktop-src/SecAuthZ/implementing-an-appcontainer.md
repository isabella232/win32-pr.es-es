---
description: AppContainer se implementa agregando nueva información al token de proceso, cambiando SeAccessCheck() para que todos los objetos heredados de lista de control de acceso (ACL) sin modificar bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada y vuelvan a usar los objetos ACL que deben estar disponibles para AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementación de un elemento AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d50c0a5aa9f80755084886554a533fe1c82a6791840a9ff4ea4fdcf1476fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670805"
---
# <a name="implementing-an-appcontainer"></a>Implementación de un elemento AppContainer

AppContainer se implementa agregando nueva información al token de proceso, cambiando [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos los objetos heredados de lista de control de acceso (ACL) sin modificar bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada y vuelvan a usar los objetos ACL que deben estar disponibles para AppContainers.

## <a name="the-process"></a>El proceso

Comience agregando nueva información para el token de proceso. A continuación, cambie **SeAccessCheck()** para que todas las ACL heredadas y sin modificar bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada. Por último, re-ACL resources that should be available to AppContainers (Recursos de acl de nuevo que deben estar disponibles para AppContainers)

El SID de AppContainer es un identificador único persistente para appcontainer. Los SID de funcionalidad conceden acceso a grupos de recursos a grupos de AppContainers. AppContainerNumber es un **DWORD** transitorio que se usa para distinguir entre AppContainers. Sin embargo, no debe usarse como identidad para AppContainer.

Para permitir que un único AppContainer acceda a un recurso, agregue su AppContainerSID a la ACL de ese recurso.

Para permitir que varios AppContainers específicos accedan a un recurso, agregue todos sus SSID de AppContainer a la ACL de ese recurso.

Para administrar grupos de permisos, cree un SID de funcionalidad (un GUID) y coloque ese SID de funcionalidad en todos los recursos que se concederán. A continuación, agregue el SID de funcionalidad al token de proceso.

Para permitir que todos los AppContainers accedan a un recurso, agregue el SID **ALL APPLICATION PACKAGES** a la ACL de ese recurso. Esto actúa como un carácter comodín.

Tanto AppContainerSID como CapabilitySID admiten máscaras de acceso en Access Control entradas (ACE). Establezca según corresponda.

 

 
