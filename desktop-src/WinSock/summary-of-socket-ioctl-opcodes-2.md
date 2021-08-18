---
description: Algunos de los códigos de operación ioctl de socket para Windows Sockets 2 se resumen en la tabla siguiente.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Resumen de los códigos de operación de Ioctl de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f0d6163e4ef36598dad56dd4d81201bdda3c2a3b1bb0473a0ef9ffb4675b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559665"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Resumen de los códigos de operación de Ioctl de socket

Algunos de los códigos de operación ioctl de socket para Windows Sockets 2 se resumen en la tabla siguiente. Encontrará información más detallada en la referencia de Winsock sobre las ICTL de [**Winsock**](winsock-ioctls.md) y la [**función WSPIoctl.**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) Hay otros códigos de operación ioCTL específicos del protocolo nuevos que se pueden encontrar en el anexo específico del protocolo.

Hay disponible una lista completa [**de ICTL de Winsock**](winsock-ioctls.md) en la referencia de Winsock.



| Código de operación                                                      | Tipo de entrada                               | Tipo de salida                                 | Significado                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Unsigned long                            | <Not used>                            | Habilita o deshabilita el modo de no bloqueo en el socket.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Unsigned long                               | Determina la cantidad de datos que se pueden leer de forma atómica desde el socket.                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | Determina si se han leído o no todos los datos de OOB.                                                                                                                                                              |
| IDENTIFICADOR DE ASOCIADO DE SIO \_ \_                                      | Api complementaria dependiente                  | <Not used>                            | Asocia el socket al identificador especificado de una interfaz complementaria.                                                                                                                                          |
| SIO \_ ENABLE \_ CIRCULAR \_ QUEUEING                             | <Not used>                         | <Not used>                            | Habilita la cola circular.                                                                                                                                                                                          |
| SIO \_ FIND \_ ROUTE                                            | [**sockaddr (estructura)**](sockaddr-2.md) | <Not used>                            | Solicita la ruta a la dirección especificada que se va a detectar.                                                                                                                                                      |
| SIO \_ FLUSH                                                  | <Not used>                         | <Not used>                            | Descarta el contenido actual de la cola de envío.                                                                                                                                                                    |
| SIO \_ GET \_ BROADCAST \_ ADDRESS                                | <Not used>                         | [**sockaddr (estructura)**](sockaddr-2.md)    | Recupera la dirección de difusión específica del protocolo que se usará en [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)).                                                                                                                  |
| SIO \_ GET \_ QOS                                               | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Recupera las especificaciones de flujo actuales para el socket.                                                                                                                                                              |
| SIO \_ GET \_ GROUP \_ QOS                                        | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Reservado.                                                                                                                                                                                                          |
| SIO \_ MULTIPOINT \_ LOOPBACK                                   | BOOL                                     | <Not used>                            | Controla si los datos enviados en una sesión de varios puntos también los recibirá el mismo socket en el host local.                                                                                                     |
| ÁMBITO DE \_ MULTIDIFUSIÓN DE SIO \_                                       | int                                      | <Not used>                            | Especifica el ámbito sobre el que se producirán las transmisiones de multidifusión.                                                                                                                                                 |
| SIO \_ SET \_ QOS                                               | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Establece nuevas especificaciones de flujo para el socket.                                                                                                                                                                |
| SIO \_ SET \_ GROUP \_ QOS                                        | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Reservado.                                                                                                                                                                                                          |
| IDENTIFICADOR DE TRADUCCIÓN DE SIO \_ \_                                      | int                                      | Companion-API dependiente                     | Obtiene un identificador correspondiente para los *sockets* que es válido en el contexto de una interfaz complementaria.                                                                                                               |
| CONSULTA DE INTERFAZ \_ DE ENRUTAMIENTO \_ DE \_ SIO                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | Obtiene la dirección de la interfaz local que se debe usar para enviar a la dirección especificada.                                                                                                                   |
| CAMBIO DE LA INTERFAZ \_ DE ENRUTAMIENTO \_ DE \_ SIO                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | Solicita la notificación de cambios en la información notificada a través de SIO \_ ROUTING INTERFACE QUERY para la dirección \_ \_ especificada.                                                                                         |
| [**CONSULTA DE LISTA \_ DE \_ DIRECCIONES DE \_ SIO**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**DIRECCIÓN DE \_ SOCKET**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Obtiene una lista de direcciones de transporte local de la familia de protocolos del socket a la que se puede enlazar la aplicación. La lista de direcciones varía en función de la familia de direcciones y algunas direcciones se excluyen de la lista. |
| CAMBIO EN LA \_ LISTA DE DIRECCIONES DE \_ \_ SIO                                  | <Not used>                         | <Not used>                            | Solicita la notificación de cambios en la información notificada a través de SIO \_ ADDRESS \_ LIST \_ QUERY                                                                                                                         |
| IDENTIFICADOR DE DESTINO \_ \_ DE PNP DE CONSULTA DE \_ \_ SIO                             | <Not used>                         | Zócalo                                      | Obtiene el descriptor de socket del siguiente proveedor de la cadena de la que depende el socket actual con respecto a PnP.                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
