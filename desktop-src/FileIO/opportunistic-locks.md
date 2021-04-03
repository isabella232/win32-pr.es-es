---
description: Un bloqueo oportunista (también denominado bloqueo oportunista) es un bloqueo colocado por un cliente en un archivo que reside en un servidor.
ms.assetid: b4c2f5f0-a29b-4598-a49b-da99e93d2991
title: Bloqueos oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faec833caae05bff247a7a3655885b1a967f3435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810448"
---
# <a name="opportunistic-locks"></a>Bloqueos oportunistas

Un bloqueo oportunista (también denominado bloqueo oportunista) es un bloqueo colocado por un cliente en un archivo que reside en un servidor. En la mayoría de los casos, un cliente solicita un bloqueo oportunista para que pueda almacenar en caché los datos localmente, lo que reduce el tráfico de red y mejora el tiempo de respuesta aparente. Los redirectores de red usan los bloqueos oportunistas en los clientes con servidores remotos, así como con las aplicaciones cliente en servidores locales.

Los bloqueos oportunistas coordinan el almacenamiento en caché de datos y la coherencia entre clientes y servidores y entre varios clientes. Los datos coherentes son los datos que son iguales en la red. En otras palabras, si los datos son coherentes, se sincronizan los datos del servidor y de todos los clientes.

Los bloqueos oportunistas no son comandos del cliente al servidor. Son solicitudes del cliente al servidor. Desde el punto de vista del cliente, son oportunistas. En otras palabras, el servidor concede estos bloqueos siempre que otros factores hagan posibles los bloqueos.

Cuando una aplicación local solicita acceso a un archivo remoto, la implementación de bloqueos oportunistas es transparente para la aplicación. El redirector de red y el servidor implicaban abrir y cerrar automáticamente los bloqueos oportunistas. Sin embargo, los bloqueos oportunistas también se pueden usar cuando una aplicación local solicita acceso a un archivo local y se debe delegar el acceso a otras aplicaciones y procesos para evitar daños en el archivo. En este caso, la aplicación local solicita directamente un bloqueo oportunista desde el sistema de archivos local y almacena el archivo en caché localmente. Cuando se usa de esta manera, el bloqueo oportunista es realmente un semáforo administrado por el servidor local y se usa principalmente con fines de coherencia de datos en la notificación de acceso a archivos y archivos.

Antes de usar bloqueos oportunistas en la aplicación, debe estar familiarizado con los modos de acceso y uso compartido de archivos descritos en [creación y apertura de archivos](creating-and-opening-files.md).

El número máximo de bloqueos oportunistas simultáneos que se pueden crear solo está limitado por la cantidad de memoria disponible.

Las aplicaciones locales no deben intentar solicitar bloqueos oportunistas desde servidores remotos. [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devolverá un error si se realiza un intento para hacerlo.

Los bloqueos oportunistas son de uso muy limitado para las aplicaciones. El único uso práctico es probar un redirector de red o un controlador de bloqueo oportunista del servidor. Normalmente, los sistemas de archivos implementan la compatibilidad con bloqueos oportunistas. Las aplicaciones suelen dejar la administración de bloqueos oportunistas en los controladores del sistema de archivos. Cualquier persona que implemente un sistema de archivos debe usar el [Kit del sistema de archivos instalables (IFS)](https://www.microsoft.com/whdc/devtools/ifskit/default.mspx). Cualquier persona que desarrolle un controlador de dispositivo que no sea un sistema de archivos instalable debe usar el [Kit de controladores de Windows (WDK)](https://www.microsoft.com/?ref=go).

Los bloqueos oportunistas y las operaciones asociadas son un superconjunto de la parte del bloqueo oportunista del Protocolo de sistema de archivos de Internet común (CIFS), un borrador de Internet. El protocolo CIFS es una versión mejorada del Protocolo de bloque de mensajes del servidor (SMB). Para obtener más información, vea [información general sobre el protocolo SMB de Microsoft y el protocolo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md). El borrador de Internet de CIFS identifica explícitamente que una implementación de CIFS puede implementar bloqueos oportunistas mediante la negación de concesión.

En los temas siguientes se identifican los bloqueos oportunistas.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                               | Descripción                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Almacenamiento en caché local](local-caching.md)<br/>                                                                       | El *almacenamiento en caché local* de los datos es una técnica que se usa para agilizar el acceso a la red a los archivos de datos. Implica almacenar datos en caché en los clientes en lugar de en servidores cuando sea posible.<br/>                                                                                                                           |
| [Coherencia de datos](data-coherency.md)<br/>                                                                     | Si los datos son coherentes, se sincronizan los datos del servidor y de todos los clientes. Un tipo de sistema de software que proporciona la coherencia de datos es un sistema de control de revisiones (RCS).<br/>                                                                                                              |
| [Cómo solicitar un bloqueo oportunista](how-to-request-an-opportunistic-lock.md)<br/>                         | Los bloqueos oportunistas se solicitan abriendo primero un archivo con permisos y marcas adecuadas para la aplicación que abre el archivo. Todos los archivos para los que se solicitarán bloqueos oportunistas se deben abrir para una operación superpuesta (asincrónica).<br/>                                |
| [Respuesta del servidor para abrir solicitudes en archivos bloqueados](server-response-to-open-requests-on-locked-files.md)<br/> | Puede minimizar el impacto que tiene la aplicación en otros clientes y el impacto que tienen en la aplicación al conceder tantos recursos compartidos como sea posible, solicitar el nivel de acceso mínimo necesario y usar el menos bloqueo oportunista intrusivo adecuado para su aplicación.<br/> |
| [Tipos de bloqueos oportunistas](types-of-opportunistic-locks.md)<br/>                                         | Describe los bloqueos oportunistas de nivel 1, nivel 2, Batch y Filter.<br/>                                                                                                                                                                                                                     |
| [Interrumpir bloqueos oportunistas](breaking-opportunistic-locks.md)<br/>                                         | Interrumpir un bloqueo oportunista es el proceso de degradar el bloqueo que un cliente tiene en un archivo para que otro cliente pueda abrir el archivo, con o sin un bloqueo oportunista.<br/>                                                                                                     |
| [Ejemplos de bloqueos oportunistas](opportunistic-lock-examples.md)<br/>                                           | Diagramas de vistas de tráfico de red para un bloqueo oportunista de nivel 1, un bloqueo oportunista de lotes y un bloqueo oportunista de filtro.<br/>                                                                                                                                                       |
| [Operaciones de bloqueo oportunista](opportunistic-lock-operations.md)<br/>                                       | Si una aplicación solicita bloqueos oportunistas, todos los archivos para los que solicita bloqueos deben abrirse para la entrada y salida superpuestas (asincrónicas) mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la marca de la **marca de archivo \_ \_ superpuesta** .<br/>                                   |



 

Para obtener más información sobre los bloqueos oportunistas, consulte el documento de borrador de Internet de CIFS. Las discrepancias entre este tema y el borrador de Internet de CIFS actual deben resolverse en favor del borrador de Internet de CIFS.

 

