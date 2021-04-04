---
description: El perfil de virtualización de recursos proporciona los medios por los que un cliente puede detectar los recursos virtuales que admite el sistema de virtualización.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Servicio de administración de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c405cac60df719195466da6ea0c7aadb7bf0d765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083267"
---
# <a name="resource-management-service"></a>Servicio de administración de recursos

El perfil de virtualización de recursos proporciona los medios por los que un cliente puede detectar los recursos virtuales que admite el sistema de virtualización. También describe la capacidad, o el número de asignaciones, que se admite para cada tipo de recurso virtual. En la ilustración siguiente se muestra el perfil de virtualización de recursos.

![Perfil de virtualización de recursos](images/resourcemanagement.png)

En el perfil de virtualización de recursos se definen dos clases diferentes de recursos virtuales:

-   Recurso compartido: representa los recursos del host que se pueden compartir entre varias máquinas virtuales. [**MSVM \_ El procesador**](msvm-processor.md) es un ejemplo de un recurso compartido.
-   Recurso sintético: representa los recursos virtuales que no tienen un recurso de host correspondiente. [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) es un ejemplo de un recurso sintético.

El grupo de recursos de servidor se utiliza para recopilar una clase de recursos de host para que se pueda detectar fácilmente mientras sus capacidades y configuraciones se pueden describir en una ubicación central. No hay ningún límite en la forma en que puede ser básica o avanzada una implementación del recurso recopilado.

En el grupo de recursos, el cliente puede tener acceso a las capacidades de asignación asociadas (AC). Esta clase describe las capacidades del recurso descrito por este grupo de recursos. Por ejemplo, puede indicar si el [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) representado por este grupo de recursos es compatible con LAN virtuales (VLAN) o filtros.

El perfil AC define los medios por los que un cliente puede detectar el intervalo válido y la configuración predeterminada de un recurso virtual determinado. Un objeto AC está asociado a cada grupo de recursos. Cuatro objetos de datos de configuración de asignación de recursos (RASD) se asocian con el objeto AC para describir los valores mínimo, máximo, predeterminado e incremental para la asignación del recurso especificado. Juntas, estas clases describen el intervalo general de las capacidades admitidas. La instancia de [**MSVM \_ AllocationCapabilities**](msvm-allocationcapabilities.md) proporciona un punto de anclaje para el conjunto de instancias de [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que especifican el intervalo de valores predeterminado y válido para un recurso virtual. La clase de asociación [**MSVM \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) proporciona el vínculo entre la instancia de AC y la configuración mínima, máxima, incremental y predeterminada para un recurso admitido por la plataforma de virtualización.

 

 



