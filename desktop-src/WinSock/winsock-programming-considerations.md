---
description: Windows Sockets 2 amplía la funcionalidad de Windows Sockets 1.1 en varias áreas. En la tabla siguiente se resumen algunos de los principales cambios de características.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Consideraciones de programación de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8451601f92f0fbf7b85532fc5a63479fe2bec26adc1984c74fc1cd7d750a04aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739864"
---
# <a name="winsock-programming-considerations"></a>Consideraciones de programación de Winsock

Windows Sockets 2 amplía la funcionalidad de Windows Sockets 1.1 en varias áreas. En la tabla siguiente se resumen algunos de los principales cambios de características.



| Características                                                                                                           | Descripción                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Arquitectura de sockets 2](windows-sockets-2-architecture-2.md)                                             | Descripción de la arquitectura Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Identificadores de socket](socket-handles-2.md)                                                                             | Opcionalmente, un identificador de socket puede ser un identificador de archivo Windows Sockets 2. Es posible usar identificadores de socket con funciones Windows de E/S de archivos estándar.                                                                                                                                           |
| [Acceso simultáneo a varios protocolos de transporte](simultaneous-access-to-multiple-transport-protocols-2.md)   | Permite que una aplicación use la conocida interfaz de socket para lograr el acceso simultáneo a varios protocolos de transporte instalados.                                                                                                                                                        |
| [Resolución de nombres independiente del protocolo](protocol-independent-name-resolution-2.md)                                 | Incluye un conjunto estandarizado de funciones para consultar y trabajar con los infinidad de dominios de resolución de nombres que existen actualmente (por ejemplo, DNS, SAP y X.500).                                                                                                                                  |
| [Multipunto y multipunto independientes del protocolo](protocol-independent-multicast-and-multipoint-2.md)               | Las aplicaciones detectan qué tipo de funcionalidades multipunto o multidifusión proporciona un transporte y usan estas instalaciones de forma genérica.                                                                                                                                                     |
| [E/S superpuesta](overlapped-i-o-and-event-objects-2.md)                                                           | Incorpora el paradigma superpuesto para la E/S de socket siguiendo el modelo establecido en Windows entornos.                                                                                                                                                                                   |
| [E/S de dispersión/recopilación](scatter-gather-i-o-2.md)                                                                     | Incorpora funcionalidades de dispersión y recopilación con el paradigma superpuesto para la E/S de socket, siguiendo el modelo establecido en Windows entornos.                                                                                                                                                 |
| [Calidad de servicio](flow-specification-quality-of-service-2.md) (QoS)                                            | Establece convenciones que las aplicaciones usan para negociar los niveles de servicio necesarios para parámetros como el ancho de banda y la latencia. Otras mejoras relacionadas con QoS incluyen mecanismos para extensiones de calidad de servicio específicas de la red.                                                         |
| [Mecanismo de extensión específico del proveedor](provider-specific-extension-mechanism-2.md)                               | La [**función WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permite a los proveedores de servicios ofrecer extensiones de características específicas del proveedor.                                                                                                                                                                           |
| [Sockets compartidos](shared-sockets-2.md)                                                                             | La [**función WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) se introdujo para habilitar el uso compartido de sockets entre procesos.                                                                                                                                                                       |
| [Configuración y desmontaje de la conexión](connection-setup-and-teardown-2.md)                                               | Una aplicación puede obtener información del autor de la llamada, como el identificador del autor de la llamada y la calidad del servicio antes de decidir si se acepta una solicitud de conexión entrante. También es posible (para los protocolos que lo admiten) intercambiar datos de usuario entre los puntos de conexión en el momento de la desmontaje de la conexión. |
| [Cierre estable, opciones de Linger y cierre de socket](graceful-shutdown-linger-options-and-socket-closure-2.md) | Una aplicación tiene varias opciones para apagar una conexión de socket (secuencia de apagado).                                                                                                                                                                                                  |
| [Datos fuera de banda independientes del protocolo](protocol-independent-out-of-band-data-2.md)                               | La abstracción del socket de flujo incluye la noción de datos fuera de banda (OOB).                                                                                                                                                                                                                   |
| [Instalaciones de depuración y seguimiento](debug-and-trace-facilities-2.md)                                                     | Windows Sockets 2 admite una versión especialmente ideada de la32.dll Ws2 y un archivo \_ DLL de depuración o seguimiento independiente.                                                                                                                                                                                      |
| [Windows Problemas de compatibilidad de sockets](windows-sockets-compatibility-issues-2.md)                                 | Windows Sockets 2 sigue siendo compatible con todas las semánticas de Windows Sockets 1.1 y las llamadas de función, excepto las que se enfrentan al pseudobloqueo.                                                                                                                                              |
| [Control de errores de Winsock](handling-winsock-errors.md)                                                             | Cómo una aplicación puede recuperar y controlar los errores de Winsock.                                                                                                                                                                                                                             |



 

 

 



