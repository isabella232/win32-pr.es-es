---
description: El perfil de virtualización de recursos proporciona los medios por los que un cliente puede detectar los recursos virtuales compatibles con el sistema de virtualización.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Servicio de administración de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593af3c440ad15add50445a3b05f41d44c8c396a1334635aeaf141838e82e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746225"
---
# <a name="resource-management-service"></a>Servicio de administración de recursos

El perfil de virtualización de recursos proporciona los medios por los que un cliente puede detectar los recursos virtuales compatibles con el sistema de virtualización. También se describe la capacidad (o el número de asignaciones) que se admite para cada tipo de recurso virtual. En la ilustración siguiente se muestra el perfil de virtualización de recursos.

![perfil de virtualización de recursos](images/resourcemanagement.png)

El perfil de virtualización de recursos define dos clases diferentes de recursos virtuales:

-   Recurso compartido: representa los recursos del host que son o son capaces de compartirse entre varias máquinas virtuales. [**Msvm \_ El**](msvm-processor.md) procesador es un ejemplo de un recurso compartido.
-   Recurso sintético: representa los recursos virtuales que no tienen ningún recurso de host correspondiente. [**Msvm \_ EmulatedEthernetPort es**](msvm-emulatedethernetport.md) un ejemplo de un recurso sintético.

El grupo de recursos se usa para recopilar una clase de recursos de host para que se pueda detectar fácilmente, mientras que sus funcionalidades y configuración se pueden describir en una ubicación central. No hay ningún límite en lo básico o avanzado que puede ser una implementación del recurso recopilado.

Desde el grupo de recursos, el cliente puede acceder a las funcionalidades de asignación (AC) asociadas. Esta clase describe las funcionalidades del recurso descritas por este grupo de recursos. Por ejemplo, puede indicar si [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) representado por este grupo de recursos admite redes LAN virtuales (VLAN) o filtros.

El perfil de CA define los medios por los que un cliente puede detectar el intervalo válido de y la configuración predeterminada para un recurso virtual determinado. Un objeto ac está asociado a cada grupo de recursos. Cuatro objetos de datos de configuración de asignación de recursos (RASD) están asociados al objeto ac para describir los valores mínimo, máximo, predeterminado e incremental para la asignación del recurso especificado. Juntas, estas clases describen la gama general de funcionalidades admitidas. La instancia de [**\_ Msvm AllocationCapabilities**](msvm-allocationcapabilities.md) proporciona un punto delimitador para el conjunto de instancias de [**\_ ResourceAllocationSettingData de Msvm**](msvm-resourceallocationsettingdata.md) que especifican el intervalo predeterminado y válido de configuración para un recurso virtual. La clase de [**asociación Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) proporciona el vínculo entre la instancia de AC y la configuración mínima, máxima, incremental y predeterminada de un recurso compatible con la plataforma de virtualización.

 

 



