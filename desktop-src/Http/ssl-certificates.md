---
title: Certificados SSL
description: Capa de sockets seguros (SSL) se ha convertido en un estándar para proteger las conexiones a Internet y se usa para evitar la interceptación en la red. El protocolo SSL permite que un cliente y un servidor se autentiquen entre sí y negocien los algoritmos de cifrado.
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15e4e6f2b0fe9e3bb058ba506f8a36728540443
ms.sourcegitcommit: be2b23d847b9717224c5f31816594c8abda388a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "105685686"
---
# <a name="ssl-certificates"></a>Certificados SSL

Capa de sockets seguros (SSL), también conocido como seguridad de la capa de transporte (TLS), se ha convertido en un estándar para proteger las conexiones a Internet y se usa para evitar la interceptación en la red. El protocolo SSL/TLS permite que un cliente y un servidor se autentiquen entre sí y negocien los algoritmos de cifrado.

SSL utiliza una clave de cifrado y un algoritmo de cifrado para proteger la conexión HTTP. Las claves de cifrado están contenidas en certificados SSL utilizados por el cliente y el servidor. Normalmente, el certificado es un documento X. 509 ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)). El servidor proporciona el certificado SSL para la sesión y lo envía al cliente en la fase de protocolo de enlace. El cliente envía su certificado al servidor sólo si el servidor envía una solicitud al cliente para un certificado. Por lo tanto, el cliente siempre autentica el servidor, pero el servidor tiene la opción de autenticar el cliente.

Los certificados de servidor deben almacenarse en el almacenamiento persistente local de la API del servidor HTTP, para su uso cada vez que se cree una conexión segura. Cada entrada del almacén de certificados también contiene la dirección IP y el puerto del servidor, el hash del certificado (usado para firmar los mensajes) y el identificador de la aplicación. El identificador de la aplicación se usa para identificar la aplicación que posee el certificado.

Los administradores del sistema pueden almacenar la información del certificado de servidor SSL con las API de configuración. Una herramienta administrativa llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) y especifica el valor HttpServiceConfigSSLCertInfo para el parámetro de configuración del servicio para establecer la información de un certificado SSL. Solo se puede configurar un certificado de servidor para cada par de puerto y dirección IP del equipo. La API del servidor HTTP también proporciona funciones de [**consulta**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) y [**eliminación**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) para obtener acceso a los certificados existentes o eliminarlos.

 

 




