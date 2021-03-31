---
title: Configuración del registro de EAPHost
description: Los valores del registro en las claves del registro siguientes controlan aspectos de la funcionalidad de EAPHost.
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e4d258062ee2ae365924ecda22c2660ed5b742
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103904322"
---
# <a name="eaphost-registry-settings"></a>Configuración del registro de EAPHost

Los valores del registro en las claves del registro siguientes controlan aspectos de la funcionalidad de EAPHost.



| Subclave                                                                 | Descripción                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BypassNegotiation](bypassnegotiation.md)                             | Determina si se produce la negociación de capacidades entre el servidor y el cliente RAS.<br/>                                                                              |
| [AssumePhase2Fragmentation](assumephase2fragmentation.md)             | Determina si el cliente y el servidor RAS asumen la fragmentación de la fase 2.<br/>                                                                                         |
| [OverrideEAPCertificateSelection](overrideeapcertificateselection.md) | Determina si el cliente invalidará el comportamiento predeterminado de la selección de certificados de tarjeta inteligente y proporcionará al usuario más certificados entre los que elegir.<br/> |
| [PeapServerUseAllPurposeCert](peapserveruseallpurposecert.md)         | Determina si los certificados de propósito general se utilizan para la autenticación PEAP.<br/>                                                                                      |
| [PeapServerAcceptAllPurposeCert](peapserveracceptallpurposecert.md)   | Determina si los certificados de propósito único se aceptan para la autenticación PEAP.<br/>                                                                                  |
| [TlsServerUseAllPurposeCert](tlsserveruseallpurposecert.md)           | Determina si los certificados de propósito general se utilizan para la autenticación EAP-TLS.<br/>                                                                                   |
| [TlsServerAcceptAllPurposeCert](tlsserveracceptallpurposecert.md)     | Determina si los certificados de propósito único se aceptan para la autenticación EAP-TLS.<br/>                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de API de EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 





