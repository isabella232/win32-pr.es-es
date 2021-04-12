---
title: Configuración de directiva de grupo SNMP
description: Si usa el complemento Microsoft Management Console (MMC) para directiva de grupo para administrar la configuración de directivas basada en el registro que se aplica a SNMP, pueden existir una o varias de las subclaves siguientes.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149510"
---
# <a name="configuring-snmp-group-policy"></a>Configuración de directiva de grupo SNMP

Si usa el complemento Microsoft Management Console (MMC) para directiva de grupo para administrar la configuración de directivas basada en el registro que se aplica a SNMP, pueden existir una o varias de las subclaves siguientes.

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\  \\ **parámetros** SNMP \\ **ValidCommunities**

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\  \\ **parámetros** SNMP \\ **PermittedManagers**

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\  \\ **parámetros** SNMP \\ **TrapConfiguration**

Normalmente, solo los miembros del grupo local administradores pueden tener acceso a las subclaves del registro siguientes que almacenan los datos de configuración para el servicio SNMP:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Parámetros** \\  SNMP de System CurrentControlSet Services del equipo local ValidCommunities

**HKEY \_ \_** \\  \\  \\  \\  \\ **Parámetros** \\  SNMP de System CurrentControlSet Services del equipo local PermittedManagers

Para obtener más información acerca de la configuración de directivas basada en el registro, consulte [acerca de directiva de grupo](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 