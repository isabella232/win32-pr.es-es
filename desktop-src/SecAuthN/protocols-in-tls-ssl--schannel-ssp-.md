---
description: SSP de schannel implementa versiones de los protocolos TLS, DTLS y SSL. Las distintas versiones de Windows admiten versiones de protocolo diferentes.
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: Protocolos de TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: 4717a128602d2ae52f90e6e201c6f6ff6aeb1de2
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332420"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>Protocolos de TLS/SSL (Schannel SSP)

SChannel SSP implementa versiones de los protocolos TLS, DTLS y SSL. Las distintas versiones de Windows admiten versiones de protocolo diferentes.

## <a name="tls-protocol-version-support"></a>Compatibilidad con versiones del protocolo TLS

En la tabla siguiente se muestra la compatibilidad del proveedor de Microsoft Schannel con las versiones del protocolo TLS.

*Sugerencia: es posible que tenga que desplazarse horizontalmente para ver todas las columnas de esta tabla:*

| SO Windows | Cliente TLS 1.0 | Servidor TLS 1.0 | Cliente TLS 1.1 | Servidor TLS 1.1 | Cliente TLS 1.2 | Servidor TLS 1.2 | Cliente TLS 1.3 | Servidor TLS 1.3 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Windows Vista/Windows Server 2008                     | habilitado        | habilitado        | No compatible  | No compatible  | No compatible  | No compatible  | No compatible  | No compatible  |
| Windows Server 2008 con Service Pack 2 (SP2)         | habilitado        | habilitado        | Disabled       | Disabled       | Disabled       | Disabled       | No compatible  | No compatible  |
| Windows 7/Windows Server 2008 R2                      | habilitado        | habilitado        | Disabled       | Disabled       | Disabled       | Disabled       | No compatible  | No compatible  |
| Windows 8/Windows Server 2012                         | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 8.1/Windows Server 2012 R2                    | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1507                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1511                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1607/Windows Server 2016 Standard | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1703                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1709                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1803                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1809//Windows Server 2019                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1903                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 1909                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  | 
| Windows 10, versión 2004                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows 10, versión 20H2                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | No compatible  | No compatible  |
| Windows Server 2022                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        |


## <a name="dtls-protocol-version-support"></a>Compatibilidad con versiones del protocolo DTLS

A continuación se muestra la compatibilidad del proveedor de Microsoft Schannel con las versiones del protocolo DTLS.

*Sugerencia: es posible que tenga que desplazarse horizontalmente para ver todas las columnas de esta tabla:*

| SO Windows                                            | Cliente DTLS 1.0 | Servidor DTLS 1.0 | Cliente de DTLS 1.2 | Servidor DTLS 1.2 |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| Windows Vista/Windows Server 2008                     | No compatible   | No compatible   | No compatible   | No compatible   |
| Windows Server 2008 con SP2                          | No compatible   | No compatible   | No compatible   | No compatible   |
| Windows 7/Windows Server 2008 R2                      | habilitado         | habilitado         | No compatible   | No compatible   |
| Windows 8/Windows Server 2012                         | habilitado         | habilitado         | No compatible   | No compatible   |
| Windows 8.1/Windows Server 2012 R2                    | habilitado         | habilitado         | No compatible   | No compatible   |
| Windows 10, versión 1507                              | habilitado         | habilitado         | No compatible   | No compatible   |
| Windows 10, versión 1511                              | habilitado         | habilitado         | No compatible   | No compatible   |
| Windows 10, versión 1607/Windows Server 2016 Standard | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 1703                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 1803                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 1809                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 1903                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 1909                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 2004                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 20H2                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versión 21H1                              | habilitado         | habilitado         | habilitado         | habilitado         |

## <a name="pre-tls-standard-protocols-support"></a>Compatibilidad con protocolos estándar previos a TLS

A continuación se muestra la compatibilidad del proveedor de Microsoft Schannel con protocolos estándar previos a TLS:

*Sugerencia: es posible que tenga que desplazarse horizontalmente para ver todas las columnas de esta tabla:*

| SO Windows                                            | PCT 1.0       | Cliente SSL2   | Servidor SSL2   | Cliente SSL3 | Servidor SSL3 |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| Windows Vista/Windows Server 2008                     | No compatible | Disabled      | habilitado       | habilitado     | habilitado     |
| Windows Server 2008 con SP2                          | No compatible | Disabled      | habilitado       | habilitado     | habilitado     |
| Windows 7/Windows Server 2008 R2                      | No compatible | Disabled      | habilitado       | habilitado     | habilitado     |
| Windows 8/Windows Server 2012                         | No compatible | Disabled      | Disabled      | habilitado     | habilitado     |
| Windows 8.1/Windows Server 2012 R2                    | No compatible | Disabled      | Disabled      | habilitado     | habilitado     |
| Windows 10, versión 1507                              | No compatible | Disabled      | Disabled      | habilitado     | habilitado     |
| Windows 10, versión 1511                              | No compatible | Disabled      | Disabled      | habilitado     | habilitado     |
| Windows 10, versión 1607/Windows Server 2016 Standard | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 1703                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 1803                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 1809                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 1903                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 1909                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 2004                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 20H2                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |
| Windows 10, versión 20H1                              | No compatible | No compatible | No compatible | Disabled    | Disabled    |


> [!IMPORTANT]
> A partir Windows 10 versión 1607 y Windows Server 2016, SSL 2.0 se ha quitado y ya no se admite.

> [!TIP]  
> Todas las versiones de Windows aceptarán un mensaje de formato unificado "ClientHello", incluso cuando ssl versión 2 esté deshabilitado o ya no se admite.
