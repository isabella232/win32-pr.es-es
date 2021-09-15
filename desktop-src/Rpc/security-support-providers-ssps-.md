---
title: Proveedores de soporte técnico de seguridad (SSP)
description: A partir de Windows 2000, RPC admite una variedad de proveedores y paquetes de seguridad.
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cc5417dd6142c693005a1aab9d39738d108ae2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473547"
---
# <a name="security-support-providers-ssps"></a>Proveedores de soporte técnico de seguridad (SSP)

A partir de Windows 2000, RPC admite una variedad de proveedores y paquetes de seguridad. Entre ellas se incluyen las siguientes:

-   **Paquete de seguridad del protocolo Kerberos.** El protocolo Kerberos v5 es un paquete de seguridad estándar del sector. Usa nombres de entidad de seguridad completos.
-   **SCHANNEL SSP.** Este SSP implementa el paquete de seguridad del proveedor de protocolo unificado de Microsoft, que unifica SSL, la tecnología de comunicación privada (PCT) y la seguridad de nivel de transporte (TLS) en un paquete de seguridad. Reconoce los nombres principales msstd y fullsic.
-   **Paquete de seguridad NTLM.** Este era el paquete de seguridad principal para las redes NTLM antes Windows 2000.

Además, RPC de Microsoft proporciona *un pseudoSP* que permite a las aplicaciones negociar entre el uso de SSP reales. Este pseudoSP, denominado SSP simple del mecanismo de negociación de GSS-API (Snego), no proporciona ninguna función de autenticación real. Su único uso es ayudar a las aplicaciones a seleccionar un SSP real. Actualmente, los programas de cliente y servidor pueden usar Snego SSP para negociar entre el uso del paquete de seguridad NTLM y el paquete de seguridad del protocolo Kerberos. Para obtener más información sobre cómo seleccionar SSP, vea [Authentication-Service Constants](authentication-service-constants.md).

Todos los SSP que proporciona Microsoft, excepto SCHANNEL, reconocen las credenciales de autenticación en el formulario proporcionado por la estructura [**SEC \_ WINNT \_ AUTH \_ IDENTITY.**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) Para más información, consulte Credenciales [de autenticación de cliente.](client-authentication-credentials.md) Para obtener información sobre cómo usar SSP específicos, vea Funciones de [SSPI](/windows/desktop/SecMgmt/management-functions) y Uso del proveedor de seguridad [de Schannel](/windows/desktop/SecAuthN/secure-channel) en la documentación de seguridad del Kit de desarrollo de software de plataforma (SDK).

 

 