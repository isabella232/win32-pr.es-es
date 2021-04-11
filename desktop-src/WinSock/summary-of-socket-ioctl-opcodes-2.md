---
description: En la tabla siguiente se resumen algunos de los códigos de operaciones de IOCTL de socket para Windows Sockets 2.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Resumen de códigos de fin de ioctl de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2243457ddbb7e0bb59f14357cf61d2e771c6a7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156009"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Resumen de códigos de fin de ioctl de socket

En la tabla siguiente se resumen algunos de los códigos de operaciones de IOCTL de socket para Windows Sockets 2. Hay información más detallada en la referencia de Winsock en el [**ioctl de Winsock**](winsock-ioctls.md) y la función [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) . Existen otros códigos de error de IOCTL específicos del protocolo que se pueden encontrar en el anexo específico del protocolo.

Puede encontrar una lista completa de los [**ioctl de Winsock**](winsock-ioctls.md) en la referencia de Winsock.



| Código de operación                                                      | Tipo de entrada                               | Tipo de salida                                 | Significado                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Unsigned Long                            | <Not used>                            | Habilita o deshabilita el modo de no bloqueo en el socket.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Unsigned Long                               | Determina la cantidad de datos que se pueden leer de forma atómica desde el socket.                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | Determina si se han leído o no todos los datos OOB.                                                                                                                                                              |
| SIO \_ ( \_ identificador asociado)                                      | Dependiente de la API complementaria                  | <Not used>                            | Asocia el socket con el identificador especificado de una interfaz complementaria.                                                                                                                                          |
| SIO \_ habilitar \_ la \_ puesta en cola circular                             | <Not used>                         | <Not used>                            | Habilita la puesta en cola circular.                                                                                                                                                                                          |
| SIO \_ Buscar \_ ruta                                            | estructura [**sockaddr**](sockaddr-2.md) | <Not used>                            | Solicita la ruta a la dirección especificada que se va a detectar.                                                                                                                                                      |
| \_vaciado de SiO                                                  | <Not used>                         | <Not used>                            | Descarta el contenido actual de la cola de envío.                                                                                                                                                                    |
| SIO \_ obtener \_ dirección de difusión \_                                | <Not used>                         | estructura [**sockaddr**](sockaddr-2.md)    | Recupera la dirección de difusión específica del protocolo que se va a usar en [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)).                                                                                                                  |
| SIO \_ obtener \_ QoS                                               | <Not used>                         | [**SERVICIOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Recupera las especificaciones de flujo actuales para el socket.                                                                                                                                                              |
| SIO \_ obtener \_ QoS de grupo \_                                        | <Not used>                         | [**SERVICIOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Reservado.                                                                                                                                                                                                          |
| \_bucle invertido de Multipoint de SiO \_                                   | BOOL                                     | <Not used>                            | Controla si los datos enviados en una sesión de Multipoint también se recibirán en el mismo socket del host local.                                                                                                     |
| \_ámbito de multidifusión de SiO \_                                       | int                                      | <Not used>                            | Especifica el ámbito en el que se realizarán las transmisiones de multidifusión.                                                                                                                                                 |
| SIO \_ set \_ QoS                                               | [**SERVICIOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Establece nuevas especificaciones de flujo para el socket.                                                                                                                                                                |
| SIO \_ establecer \_ QoS de grupo \_                                        | [**SERVICIOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Reservado.                                                                                                                                                                                                          |
| \_cuadro de traducción de SiO \_                                      | int                                      | Complemento dependiente de la API                     | Obtiene un identificador correspondiente para socket *s* que es válido en el contexto de una interfaz complementaria.                                                                                                               |
| SIO \_ \_ consulta de interfaz de enrutamiento \_                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | Obtiene la dirección de la interfaz local que se debe usar para enviar a la dirección especificada.                                                                                                                   |
| SIO \_ cambio de la interfaz de enrutamiento \_ \_                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | Solicita la notificación de cambios en la información notificada a través de \_ \_ \_ la consulta de interfaz de enrutamiento de SiO para la dirección especificada.                                                                                         |
| [**\_solicitud de \_ lista de direcciones de SiO \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**Dirección de SOCKET \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación. La lista de direcciones varía en función de la familia de direcciones y algunas direcciones se excluyen de la lista. |
| cambio de la lista de direcciones de SIO \_ \_ \_                                  | <Not used>                         | <Not used>                            | Solicita la notificación de cambios en la información notificada a través de la consulta de la lista de direcciones de SIO \_ \_ \_                                                                                                                         |
| \_identificador de \_ \_ destino PNP de consulta \_ SiO                             | <Not used>                         | TOMACORRIENTE                                      | Obtiene el descriptor de socket del siguiente proveedor de la cadena de la que depende el socket actual en lo que respecta a PnP.                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ioctl de Winsock**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
