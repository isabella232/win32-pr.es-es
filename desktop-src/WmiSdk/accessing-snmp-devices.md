---
description: Permite que las aplicaciones cliente accedan a la información de SNMP a través de WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Acceso a dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241473"
---
# <a name="accessing-snmp-devices"></a>Acceso a dispositivos SNMP

El proveedor del Protocolo simple de administración de redes (SNMP) permite a las aplicaciones cliente acceder a la información de SNMP a través de WMI. El [proveedor SNMP actúa](snmp-provider.md) como puerta de enlace a sistemas y dispositivos que usan SNMP para la administración. Solo el equipo de administración o supervisión debe ejecutar WMI porque puede leer desde cualquier dispositivo habilitado para SNMP.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Las variables de objeto de base de información de administración (MIB) de SNMP se pueden leer y escribir en , y las capturas de SNMP se pueden asignar automáticamente a eventos WMI, que se pueden definir para cualquier operación arbitraria de creación, eliminación o actualización de datos más allá de las capturas definidas por MIB. Esta característica de funciones WMI como una extensión de las funcionalidades estándar de SNMP. Para obtener más información, vea [Monitoring Events](monitoring-events.md).

Las herramientas descritas en los temas siguientes están diseñadas para su uso por parte de Windows scripting y programadores de C/C++. Se recomienda estar familiarizado con WMI, SNMPv1 y SNMPv2C, así como un conocimiento práctico de los conceptos de administración de redes y redes.

Para obtener más información sobre el uso de WMI con SNMP, vea [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

 



