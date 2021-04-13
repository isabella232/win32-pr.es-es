---
title: Funciones de mensaje (administración de red)
description: Las funciones de mensajes de administración de red envían mensajes y mantienen los alias de los mensajes. A continuación se enumeran las funciones de mensaje.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421837"
---
# <a name="message-functions-network-management"></a>Funciones de mensaje (administración de red)

\[No se admiten las funciones de mensaje en Windows Vista porque no se admiten los servicios de mensajería y alertas.\]

Las funciones de mensajes de administración de red envían mensajes y mantienen los alias de los mensajes. A continuación se enumeran las funciones de mensaje.

**Windows Server 2003:** Los servicios de alerta y mensajería están deshabilitados de forma predeterminada. Debe volver a habilitar los servicios antes de llamar a las [funciones de alerta](alert-functions.md) de administración de redes o a las funciones de mensajes de administración de redes.



| Función                                               | Descripción                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envía un mensaje a un alias de mensaje registrado.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra un alias de mensaje en la tabla de nombres de mensaje.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Elimina un alias de mensaje de la tabla de nombres de mensaje.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Enumera todos los alias de mensajes almacenados en la tabla de nombres de mensaje.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Devuelve información sobre un alias de mensaje determinado en la tabla de nombres de mensaje. |



 

Un *mensaje* es un búfer de datos de texto que se envía a un usuario o aplicación en la red. Para recibir un mensaje, un usuario o una aplicación debe registrar un alias de mensaje en la tabla de nombres de mensajes de un equipo. Los siguientes alias se registran de forma predeterminada: "usuario", "equipo", "dominio" o " \* " (el dominio actual del equipo). El alias "dominio" especifica el conjunto de equipos que tienen el mismo nombre de dominio definido como su dominio o como su grupo de trabajo y escuchan difusiones en la misma subred. En el caso de NetBIOS a través de TCP/IP, la especificación del alias "dominio" también puede realizarse entre subredes si el nombre de dominio se resuelve mediante un servidor de nombres, o si se reenvían difusiones de datagramas NetBIOS a través de enrutadores. Por lo tanto, los mensajes enviados a un dominio no tienen una entrega garantizada a todos los miembros del dominio. También es posible que algunos miembros del dominio reciban el mensaje varias veces si tienen varios transportes instalados que admitan NetBIOS.

También puede registrar un alias de mensaje mediante una llamada a la función [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) . Una *tabla de nombres de mensajes* contiene una lista de alias de mensajes registrados (usuarios y aplicaciones) permitidos para recibir mensajes. Los alias registrados en la tabla de nombres de mensaje no distinguen mayúsculas de minúsculas.

El servicio Messenger debe estar en ejecución en el equipo receptor para mostrar un mensaje emergente cuando se reciba el mensaje. Además, el servicio estación de trabajo debe estar en ejecución en el equipo local. NetBIOS es el mecanismo de transporte que se usa entre el remitente y el receptor.

Las funciones de mensaje están disponibles en dos niveles de información:

-   [**Información de mensajes \_ \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**Información de mensaje \_ \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

El nivel de información de **msg \_ info \_ 1** solo existe por compatibilidad. El servicio Messenger no reenvía nombres ni permite que se reenvíen los nombres.

 

 




