---
title: Estructuras IKE/AuthIP
description: Estructuras IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de46cd72ec382dd360e6311930e946da3bf4189855adeaa49915b15ce3a9865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069095"
---
# <a name="ikeauthip-structures"></a>Estructuras IKE/AuthIP

## <a name="in-this-section"></a>En esta sección

-   [**MÉTODO DE \_ AUTENTICACIÓN DE IXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**MÉTODO DE \_ AUTENTICACIÓN DE IXT1 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**MÉTODO DE \_ AUTENTICACIÓN \_ IXTXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IXT \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IXT \_ CERT \_ ROOT \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**AUTENTICACIÓN DE \_ CERTIFICADOS \_ IXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**AUTENTICACIÓN DE \_ CERTIFICADOS \_ IXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**AUTENTICACIÓN DE \_ CERTIFICADOS \_ IXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**IXT \_ CERTIFICATE \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**IXT \_ CERTIFICATE \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**CRITERIOS DE CERTIFICADO \_ \_ IXT0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**ALGORITMO DE CIFRADO \_ \_ IXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**ESTADÍSTICAS COMUNES \_ DE IXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**ESTADÍSTICAS COMUNES \_ DE IXT1 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**IXT \_ COOKIE \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**IXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**IXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**IXT \_ CREDENTIAL2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**CREDENCIALES DE \_ IXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**CREDENCIALES DE \_ IXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**CREDENCIALES DE \_ IXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**IXT \_ CREDENTIAL \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**IXT \_ CREDENTIAL \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**IXT \_ CREDENTIAL \_ PAIR2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**AUTENTICACIÓN \_ DE EAP DE IXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**IXTXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IXTXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**IXTXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**ALGORITMO DE INTEGRIDAD \_ DE IXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**ESTADÍSTICAS COMUNES \_ ESPECÍFICAS DE LA VERSIÓN DE IP DE \_ \_ \_ \_ IXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**ESTADÍSTICAS COMUNES \_ ESPECÍFICAS DE LA VERSIÓN DE IP DE \_ \_ \_ \_ IXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**IXT \_ IP \_ VERSION SPECIFIC \_ \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**IXT \_ IP \_ VERSION SPECIFIC \_ \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**IXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**AUTENTICACIÓN \_ KERBEROS DE \_ IXT0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**AUTENTICACIÓN \_ KERBEROS DE \_ IXT1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**IXT \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**IXT \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**IXT \_ NAME \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**AUTENTICACIÓN DE IXT \_ NTLM \_ \_ V20**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**IXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**IXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**IXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**AUTENTICACIÓN \_ DE CLAVE PREVIAMENTE COMPARTIDA \_ DE IXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**AUTENTICACIÓN DE CLAVE \_ PRECOMPARTIDA \_ DE \_ IXT1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**IXT \_ PROPOSAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**AUTENTICACIÓN RESERVADA \_ DE IXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**DETALLES DE \_ SA DE IXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**DETALLES DE \_ SA DE IXTXT1 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**DETALLES DE SA DE IXT \_ \_ 2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**IXTXT \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**IXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**IXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**IXT \_ TRAFFIC0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




