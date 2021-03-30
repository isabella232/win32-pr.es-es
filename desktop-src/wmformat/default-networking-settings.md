---
title: Configuración de red predeterminada
description: Configuración de red predeterminada
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- SDK de Windows Media Format, configuración de red predeterminada
- Advanced Systems Format (ASF), configuración de red predeterminada
- ASF (formato de sistemas avanzados), configuración de red predeterminada
- SDK de Windows Media Format, configuración de red
- Advanced Systems Format (ASF), configuración de red
- ASF (formato de sistemas avanzados), configuración de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903864"
---
# <a name="default-networking-settings"></a>Configuración de red predeterminada

En las tablas siguientes se describe la configuración predeterminada de los parámetros de red en el SDK de Windows Media Format, agrupados por interfaz.



| IWMReaderNetworkConfig                | Valor predeterminado              |
|---------------------------------------|------------------------------|
| Tiempo de almacenamiento en búfer                        | 5 segundos                    |
| UseFixedUDPPort                       | false                        |
| FixedUDPPort                          | 0 (no válido)                |
| ProxySetting: HTTP                    | \_Explorador de \_ configuración del proxy WMT \_ |
| ProxySetting: MMS                     | \_configuración del proxy WMT \_ \_ ninguno    |
| ProxySetting: RTSP                    | \_configuración del proxy WMT \_ \_ ninguno    |
| ProxyHostName (HTTP, MMS, RTSP)       | ""                           |
| ProxyPort: HTTP                       | 80                           |
| ProxyPort: MMS                        | 1755                         |
| ProxtPort: RTSP                       | 554                          |
| ProxyExceptionList (HTTP, MMS, RTSP)  | ""                           |
| ProxyBypassForLocal (HTTP, MMS, RTSP) | false                        |
| ForceRerunAutoDetection               | false                        |
| EnableMulticast                       | TRUE                         |
| EnableHTTP                            | TRUE                         |
| EnableTCP                             | TRUE                         |
| EnableUDP                             | TRUE                         |
| Ancho de banda de conexión                  | 0 (detección automática)              |



 



| IWMReaderNetworkConfig2        | Valor predeterminado        |
|--------------------------------|------------------------|
| Duración de transmisión por secuencias acelerada | 100 millones (10 segundos) |
| Habilitar almacenamiento en caché de contenido         | TRUE                   |
| Habilitar caché rápida              | TRUE                   |
| Habilitar reenvíos                 | TRUE                   |
| Habilitar el simplificado del contenido        | TRUE                   |
| Límite de reconexión                | 25                     |



 



| IWMWriterNetworkSink | Valor predeterminado         |
|----------------------|-------------------------|
| Número máximo de clientes      | 5                       |
| Protocolo de red.     | 0 ( \_ Protocolo WMT \_ http) |
| Dirección URL del host             | 0 (no válido)           |



 



| IWMWriterAdvanced2  | Valor predeterminado             |
|---------------------|-----------------------------|
| Tamaño máximo de paquete | 1400                        |
| ID. de cliente de registro       | false                       |
| Modo de reproducción           | \_ \_ selección activa del modo de reproducción WMT \_ |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> </dl>

 

 




