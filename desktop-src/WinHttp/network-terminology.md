---
description: Al desarrollar una aplicación que usa los servicios HTTP de Microsoft Windows (WinHTTP), es importante comprender los siguientes conceptos y terminología relacionados con las redes en general y el protocolo HTTP en particular.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Terminología de red (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8173b921957a95ebde7f00034c31b2f016b78ab5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068323"
---
# <a name="network-terminology-winhttp"></a>Terminología de red (WinHTTP)

Al desarrollar una aplicación que usa los servicios HTTP de Microsoft Windows (WinHTTP), es importante comprender los siguientes conceptos y terminología relacionados con las redes en general y el protocolo HTTP en particular.

-   [Transacciones HTTP](#http-transactions)
-   [Servidores proxy](#proxy-servers)
-   [Modos sincrónicos y asincrónicos](#synchronous-and-asynchronous-modes)
-   [Autenticación](#authentication)

## <a name="http-transactions"></a>Transacciones HTTP

Cuando se trabaja con transacciones HTTP, se intercambia información con otro equipo en otra parte de una red. La información intercambiada puede ser un archivo que contiene texto o multimedia, o bien pueden ser los resultados de una consulta de base de datos. Una parte de la información intercambiada a través de una red se denomina *recurso*. Normalmente, el equipo que envía un recurso es el servidor y el equipo que recibe ese recurso es un cliente. Sin embargo, también es posible que un cliente publique datos en un servidor. A veces, una transacción HTTP implica un servidor de nivel intermedio. Un servidor de nivel intermedio recopila varios recursos de otros servidores, compila la información en un recurso y envía ese recurso al cliente.

El proceso de obtención de un recurso mediante el protocolo HTTP requiere que se intercamba una serie de mensajes entre el cliente y el servidor. El cliente comienza la transacción enviando un mensaje que solicita un recurso. Este mensaje se denomina solicitud HTTP o, a veces, solo una solicitud. Una solicitud HTTP consta de los siguientes componentes.

-   Método, identificador uniforme de recursos (URI), número de versión del protocolo
-   encabezados
-   Cuerpo de la entidad

Cuando un servidor recibe una solicitud, responde enviando un mensaje de vuelta al cliente. El mensaje enviado por el servidor se denomina respuesta HTTP. Una respuesta HTTP consta de los siguientes componentes.

-   Número de versión del protocolo, código de estado, texto de estado
-   encabezados
-   Cuerpo de la entidad

La respuesta indica que no se puede procesar la solicitud o proporciona la información solicitada. Dependiendo del tipo de solicitud, puede ser información sobre un recurso, como su tamaño y tipo, o puede ser parte o todo el recurso en sí. La parte de una respuesta que incluye algunos o todos los recursos solicitados se denomina "datos de respuesta" o "cuerpo de la entidad", y la respuesta no se completa hasta que se reciben todos los datos de respuesta.

Para obtener información detallada sobre las transacciones HTTP y el protocolo HTTP, vea [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), Protocolo de transferencia de hipertexto : HTTP/1.1.

## <a name="proxy-servers"></a>Servidores proxy

Aunque el servidor de destino recibe finalmente una solicitud enviada por un cliente, a veces la transacción pasa primero a través de un servidor proxy. Un proxy intercepta la solicitud e incluso puede modificarla antes de enviarla al servidor. Cuando el servidor responde, la respuesta también pasa a través del proxy antes de que se reenvía al cliente. El proxy puede modificar los encabezados en esta respuesta.

Al interceptar y traducir transacciones de red, un proxy puede:

-   Proteja el cliente mediante la supervisión de transacciones potencialmente peligrosas.
-   Permitir que el cliente se comunique mediante protocolos que podrían no ser implementados por el software cliente.
-   Actuar como puerta de enlace entre una red privada y una red pública.

La API WinHTTP incluye una herramienta de configuración de proxy que le permite proporcionar a WinHTTP información sobre los servidores proxy que interceptan las transacciones HTTP. Para obtener información sobre el uso de la herramienta de configuración de proxy, [ veaProxyCfg.exe, una herramienta de configuración de proxy](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Modos sincrónicos y asincrónicos

Hay dos modelos de programación para obtener recursos a través de una red mediante WinHTTP: los modelos sincrónicos y asincrónicos. En un modelo sincrónico, una llamada a una función o método no finaliza hasta que se completa la operación solicitada o hasta que se produce un error. Por ejemplo, cuando la aplicación solicita un recurso mediante WinHTTP sincrónicamente, no continúa con el paso siguiente hasta que se reciben los datos solicitados.

Por otro lado, un modelo asincrónico permite a una aplicación realizar otras tareas mientras espera a que se recupere el recurso. Si se llama a otra función o método WinHTTP y no ha finalizado una operación anterior, la función devuelve un error. Cuando se usa WinHTTP de forma asincrónica, los eventos y la devolución de llamada del Modelo de objetos componentes (COM) están disponibles para notificar a una aplicación el progreso en una operación HTTP.

## <a name="authentication"></a>Authentication

La autenticación es el proceso por el que un servidor HTTP o proxy HTTP valida la información de inicio de sesión de un usuario antes de que permita el acceso a los recursos. En Internet se usan varios esquemas de autenticación. Normalmente, el nombre y la contraseña de un usuario se comparan con una lista autorizada y, si el sistema detecta una coincidencia, se concede acceso en la medida especificada en la lista de permisos para el usuario.

Las funciones WinHTTP admiten la autenticación de servidor y proxy para sesiones HTTP. WinHTTP admite los siguientes esquemas de autenticación: Básico, Implícita (consulte [RFC 2617),](https://www.ietf.org/rfc/rfc2617.txt)Autenticación [NTLM,](../com/ntlmssp.md)Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md)y Microsoft Passport 1.4. Para obtener información detallada sobre la autenticación, así como un ejemplo del uso de la autenticación en una aplicación Microsoft Visual C++, vea [Autenticación en WinHTTP](authentication-in-winhttp.md).

Para obtener información sobre las consideraciones de seguridad relacionadas con la autenticación Básica y Passport, vea [Consideraciones de seguridad de WinHTTP.](winhttp-security-considerations.md)

 

 
