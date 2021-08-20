---
description: Describe la configuración de la directiva de energía que forma un esquema de energía.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Power Policy Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f8c0dbd4c7f2a27b6e6b96528c689c6609c175eded58a1de625af71e965f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674315"
---
# <a name="power-policy-settings"></a>Power Policy Configuración

Los planes y esquemas de energía constan de preferencias y configuración de directivas.

Un plan de energía consta de un grupo de preferencias de configuración de energía. Estas preferencias constan de un valor de AC y DC para cada una de las configuraciones de energía. Cada plan de energía se identifica a través de un **GUID** único, así como un nombre descriptivo. Windows Vista tiene tres planes de energía predeterminados: Ahorro de energía, Equilibrado y Alto rendimiento. Estos planes se pueden personalizar y se pueden crear planes adicionales. Todos los planes de energía tienen un atributo de personalidad que indica el comportamiento general del ahorro de energía del plan.

En la tabla siguiente se muestran las tres personalidades del plan de energía. 

| Nombre para mostrar     | Descripción                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Ahorro de energía      | Ofrece un rendimiento reducido, lo que puede aumentar el ahorro de energía.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Equilibrada         | Equilibra automáticamente el rendimiento y el consumo de energía según la demanda. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Alto rendimiento | Ofrece un rendimiento máximo a costa de un mayor consumo de energía.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> Los dispositivos que [admiten el modo de](/windows-hardware/design/device-experiences/modern-standby) espera moderna solo permiten el plan **de** energía equilibrada. **El modo de espera** moderno es la solución más reciente y simplificada para la administración de la configuración de energía.

 

Cada equipo tiene un único plan de energía activo. De forma predeterminada, los usuarios sin requisitos pueden acceder a la configuración de energía del sistema. El acceso a la configuración de energía total o individual se puede controlar a través de acl en la configuración de energía o a través de directiva de grupo. Las aplicaciones deben [**llamar a PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) para determinar si el usuario tiene acceso a la configuración de energía.

Cada configuración de energía se identifica mediante un **GUID** único e incluye un nombre descriptivo, una descripción, valores permitidos y valores predeterminados para AC y DC. La configuración de energía personalizada se puede crear mediante la [**función PowerCreateSetting.**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquemas de energía](power-schemes.md)
</dt> </dl>

 

 
