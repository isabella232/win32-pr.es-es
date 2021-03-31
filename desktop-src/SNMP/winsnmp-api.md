---
title: API WinSNMP
description: Las versiones 1.1 a y 2,0 de la interfaz de programación de aplicaciones (API WinSNMP) de Microsoft Windows SNMP permiten desarrollar aplicaciones de administración de red basadas en SNMP que se ejecutan en el entorno de Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078087"
---
# <a name="winsnmp-api"></a>API WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Las versiones 1.1 a y 2,0 de la interfaz de programación de aplicaciones (API WinSNMP) de Microsoft Windows SNMP permiten desarrollar aplicaciones de administración de red basadas en SNMP que se ejecutan en el entorno de Windows. El Protocolo simple de administración de redes (SNMP) es un protocolo de solicitud-respuesta que transfiere información de administración entre las entidades del protocolo.

WinSNMP se ha desarrollado conjuntamente con la cooperación, la entrada y el soporte técnico de varias empresas, asociaciones y usuarios.

En la primera parte de esta información general se proporciona información sobre el anexo WinSNMP 2,0, las versiones de SNMP y una lista de las solicitudes de comentarios (RFC) pertinentes. También se describe el modelo WinSNMP y los componentes y características de la implementación de Microsoft WinSNMP. También proporciona información sobre la administración de datos y los conceptos de comunicaciones que debe programar en el entorno WinSNMP.

En la segunda sección se describen las funciones WinSNMP y las siguientes tareas de programación WinSNMP relacionadas:

-   [Abrir y cerrar una aplicación WinSNMP](opening-and-closing-a-winsnmp-application.md)
-   [Abrir y cerrar una sesión WinSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Administración de capturas y notificaciones](managing-traps-and-notifications.md)
-   [Trabajar con listas de enlaces de variables](working-with-variable-binding-lists.md)
-   [Trabajar con unidades de datos de protocolo](working-with-protocol-data-units.md)
-   [Envío de mensajes SNMP](sending-snmp-messages.md)
-   [Recepción de mensajes SNMP](receiving-snmp-messages.md)
-   [Administrar identificadores de objeto](managing-object-identifiers.md)
-   [Liberación de descriptores WinSNMP](freeing-winsnmp-descriptors.md)
-   [Establecer el modo de traducción de entidad y contexto](setting-the-entity-and-context-translation-mode.md)
-   [Administrar la Directiva de retransmisión](managing-the-retransmission-policy.md)
-   [Escribir aplicaciones WinSNMP con varios subprocesos](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registro de una aplicación de agente SNMP](registering-an-snmp-agent-application.md)

Antes de leer esta información general, debe estar familiarizado con los conceptos básicos de la programación de SNMP y Windows. Para obtener más información acerca de SNMP, consulte [Protocolo simple de administración de redes](simple-network-management-protocol-snmp-.md) y las solicitudes de comentarios (RFC) relevantes publicadas por Internet Engineering Task Force (IETF).

 

 