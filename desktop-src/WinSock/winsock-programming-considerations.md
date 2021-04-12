---
description: Windows Sockets 2 amplía la funcionalidad de Windows Sockets 1,1 en varias áreas. En la tabla siguiente se resumen algunos de los principales cambios en las características.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Consideraciones sobre la programación de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaee2cd04f03afe050ca539190b51e66c0abff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155248"
---
# <a name="winsock-programming-considerations"></a>Consideraciones sobre la programación de Winsock

Windows Sockets 2 amplía la funcionalidad de Windows Sockets 1,1 en varias áreas. En la tabla siguiente se resumen algunos de los principales cambios en las características.



| Características                                                                                                           | Descripción                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Arquitectura de Windows Sockets 2](windows-sockets-2-architecture-2.md)                                             | Una descripción de la arquitectura de Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Identificadores de socket](socket-handles-2.md)                                                                             | Un identificador de socket puede ser opcionalmente un identificador de archivo en Windows Sockets 2. Es posible usar identificadores de socket con las funciones de e/s de archivo estándar de Windows.                                                                                                                                           |
| [Acceso simultáneo a varios protocolos de transporte](simultaneous-access-to-multiple-transport-protocols-2.md)   | Permite que una aplicación use la conocida interfaz de socket para obtener acceso simultáneo a varios protocolos de transporte instalados.                                                                                                                                                        |
| [Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)                                 | Incluye un conjunto estandarizado de funciones para consultar y trabajar con los cientos de dominios de resolución de nombres que existen actualmente (por ejemplo, DNS, SAP y X. 500).                                                                                                                                  |
| [Multidifusión y Multipoint independientes del Protocolo](protocol-independent-multicast-and-multipoint-2.md)               | Las aplicaciones detectan qué tipo de capacidades Multipoint o multidifusión proporciona un transporte y utilizan estos recursos de forma genérica.                                                                                                                                                     |
| [E/s superpuestas](overlapped-i-o-and-event-objects-2.md)                                                           | Incorpora el paradigma superpuesto para la e/s de sockets siguiendo el modelo establecido en entornos Windows.                                                                                                                                                                                   |
| [E/s de dispersión y recopilación](scatter-gather-i-o-2.md)                                                                     | Incorpora funcionalidades de dispersión y recopilación con el paradigma superpuesto para la e/s de socket, siguiendo el modelo establecido en entornos Windows.                                                                                                                                                 |
| [Calidad de servicio](flow-specification-quality-of-service-2.md) (QoS)                                            | Establece convenciones que las aplicaciones usan para negociar los niveles de servicio necesarios para parámetros como el ancho de banda y la latencia. Otras mejoras relacionadas con QoS incluyen mecanismos para las extensiones de calidad de servicio específicas de la red.                                                         |
| [Mecanismo de extensión específico del proveedor](provider-specific-extension-mechanism-2.md)                               | La función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permite a los proveedores de servicios ofrecer extensiones de características específicas del proveedor.                                                                                                                                                                           |
| [Sockets compartidos](shared-sockets-2.md)                                                                             | La función [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) se introduce para permitir el uso compartido de sockets entre los procesos.                                                                                                                                                                       |
| [Configuración y desmontaje de la conexión](connection-setup-and-teardown-2.md)                                               | Una aplicación puede obtener información del llamador como el identificador del autor de la llamada y la calidad del servicio antes de decidir si aceptar una solicitud de conexión entrante. También es posible (para los protocolos que lo admiten) intercambiar datos de usuario entre los extremos en el momento de la destrucción de la conexión. |
| [Cierre estable, opciones de permanencia y cierre de socket](graceful-shutdown-linger-options-and-socket-closure-2.md) | Una aplicación tiene varias opciones para cerrar una conexión de socket (secuencia de cierre).                                                                                                                                                                                                  |
| [Datos fuera de banda independientes del Protocolo](protocol-independent-out-of-band-data-2.md)                               | La abstracción de sockets de secuencia incluye la noción de datos fuera de banda (OOB).                                                                                                                                                                                                                   |
| [Funciones de depuración y seguimiento](debug-and-trace-facilities-2.md)                                                     | Windows Sockets 2 es compatible con una versión especial del32.dll Ws2 \_ y un archivo dll de depuración/seguimiento independiente.                                                                                                                                                                                      |
| [Problemas de compatibilidad de Windows Sockets](windows-sockets-compatibility-issues-2.md)                                 | Windows Sockets 2 sigue admitiendo todas las llamadas a funciones y semánticas de Windows Sockets 1,1, a excepción de las que se ocupan de los pseudo bloqueos.                                                                                                                                              |
| [Control de errores de Winsock](handling-winsock-errors.md)                                                             | Cómo una aplicación puede recuperar y controlar los errores de Winsock.                                                                                                                                                                                                                             |



 

 

 



