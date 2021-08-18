---
title: Funciones de mensaje (administración de redes)
description: Las funciones de mensajes de administración de red envían mensajes y mantienen alias de mensaje. Las funciones de mensaje se enumeran a continuación.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b30f88b3cbe0742b3bd06f2200475aaeb0d96d0c37bff9189efd1127ddc7d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912054"
---
# <a name="message-functions-network-management"></a>Funciones de mensaje (administración de redes)

\[Las funciones de mensaje no se admiten a Windows Vista porque no se admiten los servicios de alerta y mensajería.\]

Las funciones de mensajes de administración de red envían mensajes y mantienen alias de mensaje. Las funciones de mensaje se enumeran a continuación.

**Windows Server 2003:** Los servicios de alerta y mensajería están deshabilitados de forma predeterminada. Debe volver a habilitar los servicios antes de llamar a las funciones de alerta de administración de [red](alert-functions.md) o a las funciones de mensaje de administración de red.



| Función                                               | Descripción                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envía un mensaje a un alias de mensaje registrado.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra un alias de mensaje en la tabla de nombres de mensaje.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Elimina un alias de mensaje de la tabla de nombres de mensaje.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Enumera todos los alias de mensaje almacenados en la tabla de nombres de mensaje.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Devuelve información sobre un alias de mensaje determinado en la tabla de nombres de mensaje. |



 

Un *mensaje* es un búfer de datos de texto enviados a un usuario o aplicación en la red. Para recibir un mensaje, un usuario o aplicación debe registrar un alias de mensaje en la tabla de nombres de mensaje de un equipo. Los siguientes alias se registran de forma predeterminada: "user", "machine", "domain" o " \* " (el dominio actual del equipo). El alias "dominio" especifica el conjunto de equipos que tienen el mismo nombre de dominio definido como dominio o grupo de trabajo y escuchan difusión en la misma subred. Para NetBIOS a través de TCP/IP, la especificación del alias "dominio" también puede realizarse correctamente entre subredes si un servidor de nombres resuelve el nombre de dominio o si las difusiones de datagramas NetBIOS se reenvía entre enrutadores. Por lo tanto, los mensajes enviados a un dominio no tienen una entrega garantizada a todos los miembros del dominio. También es posible que algunos miembros del dominio reciban el mensaje varias veces si tienen varios transportes instalados que admiten NetBIOS.

También puede registrar un alias de mensaje llamando a la [**función NetMessageNameAdd.**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) Una *tabla de nombres de mensaje* contiene una lista de alias de mensaje registrados (usuarios y aplicaciones) permitidos para recibir mensajes. Los alias registrados en la tabla de nombres de mensaje no tienen en cuenta mayúsculas de minúsculas.

El servicio de mensajería debe ejecutarse en el equipo receptor para mostrar un mensaje emergente cuando se recibe el mensaje. Además, el servicio workstation debe ejecutarse en el equipo local. NetBIOS es el mecanismo de transporte que se usa entre el remitente y el receptor.

Las funciones de mensaje están disponibles en dos niveles de información:

-   [**MSG \_ INFO \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**MSG \_ INFO \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

El **nivel de información MSG INFO \_ \_ 1** solo existe por compatibilidad. El servicio de mensajería no reenvía nombres ni permite que los nombres se reenvía a él.

 

 




