---
description: Un AppContainer se implementa agregando nueva información al token de proceso, cambiando SeAccessCheck () para que todos los objetos de la lista de control de acceso (ACL) heredados y no modificados bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada, y vuelva a crear los objetos de ACL que deben estar disponibles para AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementar un AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912429"
---
# <a name="implementing-an-appcontainer"></a>Implementar un AppContainer

Un AppContainer se implementa agregando nueva información al token de proceso, cambiando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos los objetos de la lista de control de acceso (ACL) heredados y no modificados bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada, y vuelva a crear los objetos de ACL que deben estar disponibles para AppContainers.

## <a name="the-process"></a>El proceso

Comience agregando nueva información para el token de proceso. A continuación, cambie **SeAccessCheck ()** para que todas las ACL heredadas y sin modificar bloqueen de forma predeterminada las solicitudes de acceso de los procesos de AppContainer. Por último, vuelva a crear los recursos de la ACL que deben estar disponibles para AppContainers

El SID del AppContainer es un identificador único persistente para el appcontainer. Los SID de capacidad conceden acceso a grupos de recursos a grupos de AppContainers. Un AppContainerNumber es un **valor DWORD** transitorio que se usa para distinguir entre AppContainers. Sin embargo, no debe usarse como una identidad para el AppContainer.

Para permitir que un único AppContainer tenga acceso a un recurso, agregue su AppContainerSID a la ACL para ese recurso.

Para permitir que varias AppContainers específicas tengan acceso a un recurso, agregue todos sus AppContainerSIDs a la ACL para ese recurso.

Para administrar grupos de permisos, cree un SID de funcionalidad (un GUID) y coloque ese SID de capacidad en todos los recursos que se van a conceder. A continuación, agregue el SID de capacidad al token de proceso.

Para permitir que todos los AppContainers tengan acceso a un recurso, agregue el SID **todos los paquetes de aplicación** a la ACL para ese recurso. Esto actúa como un carácter comodín.

Tanto AppContainerSID como CapabilitySID admiten las máscaras de acceso en entradas de Access Control (ACE). Establezca según corresponda.

 

 
