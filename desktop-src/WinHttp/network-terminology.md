---
description: Al desarrollar una aplicación que usa los servicios HTTP de Microsoft Windows (WinHTTP), es importante comprender los conceptos y la terminología siguientes relacionados con las redes en general y el protocolo HTTP en particular.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Terminología de red (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8173b921957a95ebde7f00034c31b2f016b78ab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706608"
---
# <a name="network-terminology-winhttp"></a>Terminología de red (WinHTTP)

Al desarrollar una aplicación que usa los servicios HTTP de Microsoft Windows (WinHTTP), es importante comprender los conceptos y la terminología siguientes relacionados con las redes en general y el protocolo HTTP en particular.

-   [Transacciones HTTP](#http-transactions)
-   [Servidores proxy](#proxy-servers)
-   [Modos sincrónicos y asincrónicos](#synchronous-and-asynchronous-modes)
-   [Autenticación](#authentication)

## <a name="http-transactions"></a>Transacciones HTTP

Al trabajar con transacciones HTTP, intercambia información con otro equipo en otra parte de una red. La información intercambiada puede ser un archivo que contiene texto o multimedia, o puede ser el resultado de una consulta de base de datos. Una parte de la información intercambiada a través de una red se denomina *recurso*. Normalmente, el equipo que envía un recurso es el servidor y el equipo que recibe ese recurso es un cliente. Sin embargo, también es posible que un cliente publique datos en un servidor. A veces, una transacción HTTP implica un servidor de nivel intermedio. Un servidor de nivel intermedio recopila varios recursos de otros servidores, compila la información en un recurso y envía ese recurso al cliente.

El proceso de obtención de un recurso mediante el protocolo HTTP requiere que se intercambien una serie de mensajes entre el cliente y el servidor. El cliente inicia la transacción mediante el envío de un mensaje que solicita un recurso. Este mensaje se denomina solicitud HTTP o, a veces, solo una solicitud. Una solicitud HTTP consta de los siguientes componentes.

-   Método, identificador uniforme de recursos (URI), número de versión del Protocolo
-   Encabezados
-   Cuerpo de entidad

Cuando un servidor recibe una solicitud, responde mediante el envío de un mensaje de vuelta al cliente. El mensaje enviado por el servidor se denomina respuesta HTTP. Una respuesta HTTP consta de los siguientes componentes.

-   Número de versión del Protocolo, código de estado, texto de estado
-   Encabezados
-   Cuerpo de entidad

La respuesta indica que la solicitud no se puede procesar o proporciona la información solicitada. En función del tipo de solicitud, puede tratarse de información sobre un recurso, como su tamaño y tipo, o puede ser parte o todo el recurso. La parte de una respuesta que incluye algunos o todos los recursos solicitados se denomina "datos de respuesta" o "cuerpo de entidad" y la respuesta no se completa hasta que se reciben todos los datos de respuesta.

Para obtener información detallada sobre las transacciones HTTP y el protocolo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), protocolo de transferencia de hipertexto (http/1.1).

## <a name="proxy-servers"></a>Servidores proxy

Aunque el servidor de destino recibe finalmente una solicitud enviada por un cliente, en ocasiones la transacción pasa a través de un servidor proxy. Un proxy intercepta la solicitud e incluso puede modificar la solicitud antes de enviarla al servidor. Cuando el servidor responde, la respuesta también pasa a través del proxy antes de que se reenvíe al cliente. El proxy puede modificar los encabezados de esta respuesta.

Al interceptar y traducir las transacciones de red, un proxy puede:

-   Proteja el cliente mediante la supervisión de transacciones potencialmente peligrosas.
-   Habilitar al cliente para que se comunique mediante protocolos que es posible que no haya implementado el software cliente.
-   Actúe como puerta de enlace entre una red privada y una red pública.

La API WinHTTP incluye una herramienta de configuración de proxy que permite proporcionar a WinHTTP información relacionada con cualquier servidor proxy que intercepte las transacciones HTTP. Para obtener información sobre el uso de la herramienta de configuración de proxy, vea [ProxyCfg.exe, una herramienta de configuración de proxy](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Modos sincrónicos y asincrónicos

Hay dos modelos de programación para obtener recursos a través de una red mediante WinHTTP: los modelos sincrónicos y asincrónicos. En un modelo sincrónico, una llamada a una función o método no finaliza hasta que se completa la operación solicitada o hasta que se produce un error. Por ejemplo, cuando la aplicación solicita un recurso mediante WinHTTP sincrónicamente, no continúa con el paso siguiente hasta que se hayan recibido los datos solicitados.

Un modelo asincrónico, por otro lado, permite que una aplicación realice otras tareas mientras espera a que se recupere el recurso. Si se llama a otra función o método WinHTTP y una operación anterior no ha finalizado, la función devuelve un error. Al usar WinHTTP de forma asincrónica, los eventos del modelo de objetos componentes (COM) y la devolución de llamada están disponibles para notificar a una aplicación de progreso en una operación HTTP.

## <a name="authentication"></a>Autenticación

La autenticación es el proceso por el que un proxy HTTP o un servidor HTTP valida la información de inicio de sesión de un usuario antes de permitir el acceso a los recursos. Se usan varios esquemas de autenticación en Internet. Normalmente, el nombre y la contraseña de un usuario se comparan con una lista autorizada y, si el sistema detecta una coincidencia, se concede el acceso a la extensión especificada en la lista de permisos para el usuario.

Las funciones WinHTTP admiten la autenticación de servidor y proxy para las sesiones HTTP. WinHTTP admite los siguientes esquemas de autenticación: básico, implícito (consulte [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)), [autenticación NTLM](../com/ntlmssp.md), Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md)y Microsoft Passport 1,4. Para obtener información detallada sobre la autenticación, así como un ejemplo del uso de la autenticación en una aplicación Microsoft Visual C++, consulte [autenticación en WinHTTP](authentication-in-winhttp.md).

Para obtener información sobre las consideraciones de seguridad relacionadas con la autenticación básica y de Passport, vea [consideraciones de seguridad de WinHTTP](winhttp-security-considerations.md).

 

 
