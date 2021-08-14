---
title: EapHost Registry Configuración
description: Los valores del Registro de las siguientes claves del Registro controlan aspectos de la funcionalidad de EAPHost.
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec08a7428dac4c68044b0491e084574c6ff3d006fcf06f59912754c5a9f93833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482985"
---
# <a name="eaphost-registry-settings"></a>EapHost Registry Configuración

Los valores del Registro de las siguientes claves del Registro controlan aspectos de la funcionalidad de EAPHost.



| Subclave                                                                 | Descripción                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BypassNegotiation](bypassnegotiation.md)                             | Determina si se produce la negociación de funcionalidades entre el servidor RAS y el cliente.<br/>                                                                              |
| [AssumePhase2Fragmentation](assumephase2fragmentation.md)             | Determina si el servidor RAS y el cliente asumen la fragmentación de la fase 2.<br/>                                                                                         |
| [OverrideEAPCertificateSelection](overrideeapcertificateselection.md) | Determina si el cliente invalidará el comportamiento predeterminado de selección de certificados de tarjeta inteligente y proporcionará al usuario más certificados entre los que elegir.<br/> |
| [PeapServerUseAllPurposeCert](peapserveruseallpurposecert.md)         | Determina si se usan certificados de uso general para la autenticación PEAP.<br/>                                                                                      |
| [PeapServerAcceptAllPurposeCert](peapserveracceptallpurposecert.md)   | Determina si se aceptan certificados de uso general para la autenticación PEAP.<br/>                                                                                  |
| [TlsServerUseAllPurposeCert](tlsserveruseallpurposecert.md)           | Determina si se usan certificados de uso general para la autenticación EAP-TLS.<br/>                                                                                   |
| [TlsServerAcceptAllPurposeCert](tlsserveracceptallpurposecert.md)     | Determina si se aceptan certificados de uso general para la autenticación EAP-TLS.<br/>                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de API de EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 





