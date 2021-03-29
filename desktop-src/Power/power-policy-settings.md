---
description: Describe la configuración de la Directiva de energía que constituye un plan de energía.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Configuración de la Directiva de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813787"
---
# <a name="power-policy-settings"></a>Configuración de la Directiva de energía

Los planes de energía y los esquemas constan de preferencias y configuraciones de directiva.

Un plan de energía consta de un grupo de preferencias de configuración de energía. Estas preferencias se componen de un valor de AC y DC para cada una de las configuraciones de energía. Cada plan de energía se identifica mediante un **GUID** único y un nombre descriptivo. Windows Vista tiene tres planes de energía predeterminados: economizador de energía, equilibrado y alto rendimiento. Estos planes se pueden personalizar y se pueden crear planes adicionales. Todos los planes de energía tienen un atributo de personalidad que indica el comportamiento de ahorro de energía general del plan.

En la tabla siguiente se muestran los tres personalidades del plan de energía. 

| Nombre para mostrar     | Descripción                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Economizador de energía      | Ofrece un rendimiento reducido que puede aumentar el ahorro de energía.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Equilibrada         | Equilibra automáticamente el rendimiento y el consumo de energía en función de la demanda. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Alto rendimiento | Ofrece un rendimiento máximo a costa de un mayor consumo energético.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> Los dispositivos que admiten el modo de [espera moderno](/windows-hardware/design/device-experiences/modern-standby) solo permiten el plan de energía **equilibrado** . El **modo de espera moderno** es la solución más reciente y más simplificada para la administración de la configuración de energía.

 

Cada equipo tiene un plan de energía único y activo. De forma predeterminada, los usuarios sin privilegios pueden acceder a la configuración de energía del sistema. Se puede controlar el acceso a toda la configuración de energía o a través de las ACL en la configuración de energía o a través de directiva de grupo. Las aplicaciones deben llamar a [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) para determinar si el usuario tiene acceso a la configuración de energía.

Cada configuración de energía se identifica mediante un **GUID** único e incluye un nombre descriptivo, una descripción, valores permitidos y valores predeterminados para AC y DC. La configuración de energía personalizada se puede crear con la función [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Planes de energía](power-schemes.md)
</dt> </dl>

 

 
