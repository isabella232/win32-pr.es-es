---
title: Proveedores de compatibilidad para seguridad (SSP)
description: A partir de Windows 2000, RPC admite diversos proveedores y paquetes de seguridad.
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cc5417dd6142c693005a1aab9d39738d108ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149568"
---
# <a name="security-support-providers-ssps"></a>Proveedores de compatibilidad para seguridad (SSP)

A partir de Windows 2000, RPC admite diversos proveedores y paquetes de seguridad. Entre ellas se incluyen las siguientes:

-   **Paquete de seguridad del protocolo Kerberos.** El protocolo Kerberos V5 es un paquete de seguridad estándar del sector. Usa nombres de entidad de seguridad de fullsic.
-   **SSP DE SCHANNEL.** Este SSP implementa el paquete de seguridad del proveedor de protocolos unificados de Microsoft, que unifica SSL, la tecnología de comunicaciones privadas (PCT) y la seguridad de nivel de transporte (TLS) en un paquete de seguridad. Reconoce los nombres de entidad de seguridad msstd y fullsic.
-   **Paquete de seguridad de NTLM.** Este era el paquete de seguridad principal para las redes NTLM anteriores a Windows 2000.

Además, Microsoft RPC proporciona un *pseudo-SSP* que permite a las aplicaciones negociar entre el uso de SSP reales. Este pseudo-SSP, denominado "mecanismo de negociación simple GSS-API (Snego) SSP", no proporciona ninguna característica de autenticación real. Su único uso es ayudar a las aplicaciones a seleccionar un SSP real. Actualmente, los programas de cliente y servidor pueden usar el SSP Snego para negociar entre el uso del paquete de seguridad NTLM y el paquete de seguridad del protocolo Kerberos. Para obtener más información sobre la selección de SSP, vea [Authentication-Service constantes](authentication-service-constants.md).

Todos los SSP que proporciona Microsoft, excepto SCHANNEL, reconocen las credenciales de autenticación en el formato que proporciona la estructura de identidad de autenticación de [**\_ WinNT \_ \_**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) de la SEC. Para obtener más información, consulte [credenciales de autenticación del cliente](client-authentication-credentials.md). Para obtener información sobre cómo usar SSP específicos, consulte [funciones SSPI](/windows/desktop/SecMgmt/management-functions) y [uso del proveedor de seguridad Schannel](/windows/desktop/SecAuthN/secure-channel) en la documentación de seguridad del kit de desarrollo de software (SDK) de la plataforma.

 

 