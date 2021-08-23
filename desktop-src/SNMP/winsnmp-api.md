---
title: WinSNMP API
description: Las versiones 1.1a y 2.0 de la interfaz de programación de aplicaciones snmp de Microsoft Windows SNMP (API winSNMP) permiten desarrollar aplicaciones de administración de red basadas en SNMP que se ejecutan en el entorno Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38f6205b8d5ad2315be877f62f0f81f17b5737e557d5db2683163ff26edf62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142988"
---
# <a name="winsnmp-api"></a>WinSNMP API

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Las versiones 1.1a y 2.0 de la interfaz de programación de aplicaciones snmp de Microsoft Windows SNMP (API winSNMP) permiten desarrollar aplicaciones de administración de red basadas en SNMP que se ejecutan en el entorno Windows. El Protocolo simple de administración de redes (SNMP) es un protocolo de solicitud-respuesta que transfiere información de administración entre entidades de protocolo.

WinSNMP se ha desarrollado conjuntamente con la cooperación, la entrada y el soporte técnico de varias empresas, asociaciones e individuos.

La primera parte de esta información general proporciona información sobre el anexo WinSNMP 2.0, las versiones SNMP y una lista de las solicitudes de comentarios (RFC) pertinentes. También se describe el modelo WinSNMP y los componentes y características de la implementación de Microsoft WinSNMP. También proporciona información sobre los conceptos de comunicación y administración de datos que debe programar en el entorno de WinSNMP.

La segunda sección describe las funciones de WinSNMP y las siguientes tareas de programación relacionadas con WinSNMP:

-   [Apertura y cierre de una aplicación WinSNMP](opening-and-closing-a-winsnmp-application.md)
-   [Apertura y cierre de una sesión de WinSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Administración de capturas y notificaciones](managing-traps-and-notifications.md)
-   [Trabajar con listas de enlaces de variables](working-with-variable-binding-lists.md)
-   [Trabajar con unidades de datos de protocolo](working-with-protocol-data-units.md)
-   [Envío de mensajes SNMP](sending-snmp-messages.md)
-   [Recepción de mensajes SNMP](receiving-snmp-messages.md)
-   [Administración de identificadores de objeto](managing-object-identifiers.md)
-   [Liberar descriptores winSNMP](freeing-winsnmp-descriptors.md)
-   [Establecimiento del modo de traducción de entidades y contexto](setting-the-entity-and-context-translation-mode.md)
-   [Administración de la directiva de retransmisión](managing-the-retransmission-policy.md)
-   [Escritura de aplicaciones WinSNMP con varios subprocesos](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registro de una aplicación de agente SNMP](registering-an-snmp-agent-application.md)

Debe estar familiarizado con los conceptos básicos de SNMP y Windows programación antes de leer esta introducción. Para obtener más información sobre SNMP, vea [Protocolo](simple-network-management-protocol-snmp-.md) simple de administración de redes y las solicitudes de comentarios (RFC) pertinentes publicadas por el Grupo de tareas de ingeniería de Internet (IETF).

 

 