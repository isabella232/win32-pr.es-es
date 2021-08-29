---
title: Acerca de SNMP
description: SNMP usa una arquitectura distribuida que consta de administradores y agentes.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, Acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9b43fe4c6b297f0a6973be425239453bb2f03f551f217f4baf7ed0c55099b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009913"
---
# <a name="about-snmp"></a>Acerca de SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

SNMP usa una arquitectura distribuida que consta de administradores y agentes. Un agente es una aplicación SNMP que responde a las consultas de las aplicaciones del administrador SNMP. El agente SNMP es responsable de recuperar y actualizar la información de administración local en función de las solicitudes del administrador snmp. El agente también notifica a los administradores registrados cuando se producen eventos o capturas significativos. Un administrador es una aplicación SNMP que genera consultas a las aplicaciones del agente SNMP y recibe capturas de las aplicaciones del agente SNMP.

En equipos que ejecutan Microsoft Windows XP/Windows 2000/Windows NT, el agente SNMP se implementa mediante el servicio SNMP (SNMP.EXE). El administrador SNMP suele ser una aplicación de consola de administración SNMP de terceros. La aplicación de consola de administración no necesita ejecutarse en el mismo host que el agente SNMP. Para usar la información que proporciona el servicio SNMP de Microsoft, necesita al menos una aplicación de consola de administración de SNMP. El sistema incluye bibliotecas que admiten aplicaciones de consola de administración SNMP, pero no incluye una aplicación de consola de administración SNMP en este momento.

 

 