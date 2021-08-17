---
title: Configuración predeterminada de Configuración
description: Configuración predeterminada de Configuración
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows SDK de formato multimedia, configuración de red predeterminada
- Formato de sistemas avanzados (ASF), configuración de red predeterminada
- ASF (formato de sistemas avanzados), configuración de red predeterminada
- Windows SDK de formato multimedia, configuración de redes
- Formato de sistemas avanzados (ASF), configuración de red
- ASF (formato de sistemas avanzados), configuración de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591bf4aa2154d5cc04a8a17b5fc75f290a8493a39d530d4246bc0338c2424e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931425"
---
# <a name="default-networking-settings"></a>Configuración predeterminada de Configuración

En las tablas siguientes se describe la configuración predeterminada de los parámetros de red en Windows SDK de formato multimedia, agrupados por interfaz.



| IWMReaderNetworkConfig                | Valor predeterminado              |
|---------------------------------------|------------------------------|
| Tiempo de almacenamiento en búfer                        | 5 segundos                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (no válido)                |
| ProxySetting: HTTP                    | EXPLORADOR DE CONFIGURACIÓN DE PROXY WMT \_ \_ \_ |
| ProxySetting: MMS                     | CONFIGURACIÓN DE \_ PROXY WMT \_ \_ NONE    |
| ProxySetting: RTSP                    | CONFIGURACIÓN DE \_ PROXY WMT \_ \_ NONE    |
| ProxyHostName (HTTP, MMS, RTSP)       | ""                           |
| ProxyPort: HTTP                       | 80                           |
| ProxyPort: MMS                        | 1755                         |
| ProxtPort: RTSP                       | 554                          |
| ProxyExceptionList (HTTP, MMS, RTSP)  | ""                           |
| ProxyBypassForLocal (HTTP, MMS, RTSP) | FALSE                        |
| ForceRerunAutoDetection               | FALSE                        |
| EnableMulticast                       | TRUE                         |
| EnableHTTP                            | TRUE                         |
| EnableTCP                             | TRUE                         |
| EnableUDP                             | TRUE                         |
| Ancho de banda de conexión                  | 0 (detección automática)              |



 



| IWMReaderNetworkConfig2        | Valor predeterminado        |
|--------------------------------|------------------------|
| Duración del streaming acelerado | 100000000 (10 segundos) |
| Habilitación del almacenamiento en caché de contenido         | TRUE                   |
| Habilitación de la caché rápida              | TRUE                   |
| Habilitación de los reenends                 | TRUE                   |
| Habilitación de la simplificación de contenido        | TRUE                   |
| Límite de reconexión                | 25                     |



 



| IWMWriterNetworkSink | Valor predeterminado         |
|----------------------|-------------------------|
| Número máximo de clientes      | 5                       |
| Protocolo de red.     | 0 (PROTOCOLO WMT \_ \_ HTTP) |
| Host URL             | 0 (no válido)           |



 



| IWMWriterAdvanced2  | Valor predeterminado             |
|---------------------|-----------------------------|
| Tamaño máximo del paquete | 1400                        |
| Id. de cliente de registro       | FALSE                       |
| Modo de reproducción           | SELECCIÓN AUTOMÁTICA \_ DEL MODO DE REPRODUCCIÓN \_ \_ WMT |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> </dl>

 

 




