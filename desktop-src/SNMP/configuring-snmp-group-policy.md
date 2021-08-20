---
title: Configuración de snmp directiva de grupo
description: Si usa el complemento Microsoft Management Console (MMC) para directiva de grupo para administrar la configuración de directivas basada en el Registro que se aplica a SNMP, puede que exista una o varias de las subclaves siguientes.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e17bc3b1bac886a19791f57903920a11062072a81577a0a78ab01d461709ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009663"
---
# <a name="configuring-snmp-group-policy"></a>Configuración de snmp directiva de grupo

Si usa el complemento Microsoft Management Console (MMC) para directiva de grupo para administrar la configuración de directivas basada en el Registro que se aplica a SNMP, puede que exista una o varias de las subclaves siguientes.

**HKEY \_ Parámetros \_ SNMP** \\  \\  \\  \\  \\ **validCommuniities** de directivas DE SOFTWARE DE MÁQUINA LOCAL

**HKEY \_ Directivas \_ DE** SOFTWARE DE MÁQUINA LOCAL \\  \\  \\ **Parámetros SNMP** \\  \\ **AllowedManagers**

**HKEY \_ Parámetros \_ snmp de directivas** DE SOFTWARE \\  \\ **DE** MÁQUINA LOCAL \\  \\  \\ **TrapConfiguration**

Normalmente, solo los miembros del grupo local Administradores pueden acceder a las siguientes subclaves del Registro que almacenan datos de configuración para el servicio SNMP:

**HKEY \_ Parámetros \_ SNMP** \\  \\  \\  \\  \\  \\ **validCommuniities** del sistema LOCAL MACHINE CurrentControlSet Services

**HKEY \_ Parámetros \_ SNMP** \\  \\  \\  \\  \\  \\ **allowedManagers** de CurrentControlSet Services del sistema LOCAL MACHINE

Para obtener más información sobre la configuración de directivas basada en el Registro, vea [Acerca de directiva de grupo](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 