---
title: Estructuras de IKE/AuthIP
description: Estructuras de IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "104420384"
---
# <a name="ikeauthip-structures"></a>Estructuras de IKE/AuthIP

## <a name="in-this-section"></a>En esta sección

-   [**\_METHOD0 de autenticación de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**Autenticación de IKEEXT \_ \_ METHOD1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**\_METHOD2 de autenticación de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ CONFIG0 raíz del certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**\_AUTHENTICATION0 de certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**\_AUTHENTICATION1 de certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**\_Cuadro de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CREDENTIAL0 de certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**\_CREDENTIAL1 de certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**\_CRITERIA0 de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_Cifrado de ALGORITHM0 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**\_STATISTICS0 común de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**\_STATISTICS1 común de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**COOKIE de IKEEXT \_ \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**CREDENTIAL0 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**CREDENTIAL1 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**CREDENTIAL2 de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**CREDENTIALS0 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**CREDENTIALS1 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**CREDENTIALS2 de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**\_PAIR0 de credenciales de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**\_PAIR1 de credenciales de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**\_PAIR2 de credenciales de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**\_AUTHENTICATION0 de EAP de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**\_POLICY0 de EM de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IKEEXT \_ em \_ directiva1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**\_POLICY2 de EM de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_ALGORITHM0 de integridad de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**\_ \_ \_ \_ STATISTICS0 comunes específicos de la versión IP de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**\_ \_ \_ \_ STATISTICS1 comunes específicos de la versión IP de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**\_KEYMODULE específico de la versión IP de IKEEXT \_ \_ \_ \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**\_KEYMODULE específico de la versión IP de IKEEXT \_ \_ \_ \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**\_AUTHENTICATION0 de IPv6 \_ CGA \_ de IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**\_AUTHENTICATION0 de Kerberos IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**\_AUTHENTICATION1 de Kerberos IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**KEYMODULE de IKEEXT \_ \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**KEYMODULE de IKEEXT \_ \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**Nombre de IKEEXT \_ \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**AUTHENTICATION0 de IKEEXT \_ NTLM \_ V2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**POLICY0 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**IKEEXT \_ directiva1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**POLICY2 de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_AUTHENTICATION0 de claves previamente COMpartidas de IKEEXT \_ \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**\_AUTHENTICATION1 de claves previamente COMpartidas de IKEEXT \_ \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**PROPOSAL0 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_AUTHENTICATION0 reservada de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**\_DETAILS0 de SA de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**\_Detalles de SA de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**\_DETAILS2 de SA de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**TEMPLATE0 de la \_ \_ enumeración SA de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**STATISTICS0 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**STATISTICS1 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**TRAFFIC0 de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




