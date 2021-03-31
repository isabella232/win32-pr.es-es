---
title: Acerca de SNMP
description: SNMP utiliza una arquitectura distribuida que consta de administradores y agentes.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078196"
---
# <a name="about-snmp"></a>Acerca de SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

SNMP utiliza una arquitectura distribuida que consta de administradores y agentes. Un agente es una aplicación SNMP que responde a las consultas de las aplicaciones del administrador SNMP. El agente SNMP es responsable de recuperar y actualizar la información de administración local en función de las solicitudes del administrador de SNMP. El agente también notifica a los administradores registrados cuando se producen eventos o capturas significativos. Un administrador es una aplicación SNMP que genera consultas a las aplicaciones del agente SNMP y recibe capturas de aplicaciones del agente SNMP.

En los equipos que ejecutan Microsoft Windows XP/Windows 2000/Windows NT, el agente SNMP se implementa mediante el servicio SNMP (SNMP.EXE). Normalmente, el administrador SNMP es una aplicación de consola de administración SNMP de terceros. No es necesario que la aplicación de consola de administración se ejecute en el mismo host que el agente SNMP. Para usar la información que proporciona el servicio SNMP de Microsoft, necesita al menos una aplicación de consola de administración SNMP. El sistema incluye bibliotecas que admiten aplicaciones de consola de administración de SNMP, pero no incluye una aplicación de consola de administración de SNMP en este momento.

 

 