---
description: Permite a las aplicaciones cliente obtener acceso a información de SNMP a través de WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Acceso a dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697845"
---
# <a name="accessing-snmp-devices"></a>Acceso a dispositivos SNMP

El proveedor del Protocolo simple de administración de redes (SNMP) permite a las aplicaciones cliente obtener acceso a información de SNMP a través de WMI. El [proveedor SNMP](snmp-provider.md) actúa como puerta de enlace a los sistemas y dispositivos que utilizan SNMP para la administración. Solo el equipo de administración o supervisión debe ejecutar WMI porque puede leer desde cualquier dispositivo habilitado para SNMP.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Las variables de objeto de la base de información de administración de SNMP (MIB) se pueden leer y escribir en, y las capturas de SNMP se pueden asignar automáticamente a eventos de WMI, que se pueden definir para cualquier operación arbitraria de creación, eliminación o actualización a los datos más allá de las capturas definidas por MIB. Esta característica de WMI funciona como una extensión de las funcionalidades SNMP estándar. Para obtener más información, consulte [supervisión de eventos](monitoring-events.md).

Las herramientas que se describen en los temas siguientes están diseñadas para que las usen los programadores de Windows Scripting y C/C++. Se recomienda estar familiarizado con WMI, SNMPv1 y SNMPv2C, y el conocimiento práctico de los conceptos de administración de redes y redes.

Para obtener más información acerca del uso de WMI con SNMP, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

 



