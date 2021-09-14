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
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256340"
---
# <a name="default-networking-settings"></a>Configuración predeterminada de Configuración

En las tablas siguientes se describe la configuración predeterminada de los parámetros de red en Windows SDK de formato multimedia, agrupados por interfaz.



| IWMReaderNetworkConfig                | Valor predeterminado              |
|---------------------------------------|------------------------------|
| Tiempo de almacenamiento en búfer                        | 5 segundos                    |
| UseFixedUDPPort                       | false                        |
| FixedUDPPort                          | 0 (no válido)                |
| ProxySetting: HTTP                    | EXPLORADOR DE CONFIGURACIÓN DE PROXY WMT \_ \_ \_ |
| ProxySetting: MMS                     | CONFIGURACIÓN DE \_ PROXY WMT \_ \_ NONE    |
| ProxySetting: RTSP                    | CONFIGURACIÓN DE \_ PROXY WMT \_ \_ NONE    |
| ProxyHostName (HTTP, MMS, RTSP)       | ""                           |
| ProxyPort: HTTP                       | 80                           |
| ProxyPort: MMS                        | 1755                         |
| ProxtPort: RTSP                       | 554                          |
| ProxyExceptionList (HTTP, MMS, RTSP)  | ""                           |
| ProxyBypassForLocal (HTTP, MMS, RTSP) | false                        |
| ForceRerunAutoDetection               | false                        |
| EnableMulticast                       | true                         |
| EnableHTTP                            | true                         |
| EnableTCP                             | true                         |
| EnableUDP                             | true                         |
| Ancho de banda de conexión                  | 0 (detección automática)              |



 



| IWMReaderNetworkConfig2        | Valor predeterminado        |
|--------------------------------|------------------------|
| Duración del streaming acelerado | 100000000 (10 segundos) |
| Habilitación del almacenamiento en caché de contenido         | true                   |
| Habilitación de la caché rápida              | true                   |
| Habilitación de los reenends                 | true                   |
| Habilitación de la simplificación de contenido        | true                   |
| Límite de reconexión                | 25                     |



 



| IWMWriterNetworkSink | Valor predeterminado         |
|----------------------|-------------------------|
| Número máximo de clientes      | 5                       |
| Protocolo de red.     | 0 (PROTOCOLO WMT \_ \_ HTTP) |
| Host URL             | 0 (no válido)           |



 



| IWMWriterAdvanced2  | Valor predeterminado             |
|---------------------|-----------------------------|
| Tamaño máximo del paquete | 1400                        |
| Id. de cliente de registro       | false                       |
| Modo de reproducción           | SELECCIÓN AUTOMÁTICA \_ DEL MODO DE REPRODUCCIÓN \_ \_ WMT |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> </dl>

 

 




