---
description: Se usa con las funciones CryptAcquireContext y CryptSetProvider.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Nombres de proveedor de servicios criptográficos (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a5cbe497e56144a9948dab96be0c03dd5a99f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001056"
---
# <a name="cryptographic-provider-names"></a>Nombres de proveedor de servicios criptográficos

Los siguientes nombres de [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) se definen en Wincrypt. h. Estas constantes se utilizan con las funciones [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) y [**CryptSetProvider**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera) .



| Constante o valor                                                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ DH \_ Schannel \_ Prov**</dt> <dt>"Microsoft DH Schannel Cryptographic Provider"</dt> </dl>      | [Proveedor de servicios criptográficos Microsoft DSS y Diffie-Hellman/Schannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ DH \_ Prov**</dt> <dt>"Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos"</dt> </dl>     | [Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_**</dt> <dt>"proveedor de servicios criptográficos de Microsoft base DSS"</dt> </dl>                                  | [Proveedor de servicios criptográficos de Microsoft DSS](microsoft-dss-cryptographic-provider.md).<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_ DEF \_ Prov**</dt> <dt>"Microsoft base Cryptographic Provider v 1.0"</dt> </dl>                                              | [Proveedor de servicios criptográficos de base de Microsoft](microsoft-base-cryptographic-provider.md).<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ Schannel \_ Prov**</dt> <dt>"proveedor de servicios criptográficos de Microsoft RSA Schannel"</dt> </dl>  | [Proveedor de servicios criptográficos RSA/Schannel de Microsoft](microsoft-rsa-schannel-cryptographic-provider.md).<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SIG \_ Prov**</dt> <dt>"Microsoft RSA Signature Cryptographic Provider"</dt> </dl>                | No se admite el [proveedor de servicios criptográficos de firmas RSA de Microsoft](microsoft-rsa-signature-cryptographic-provider.md) .<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ ENH \_ DSS \_ DH \_ Prov**</dt> <dt>"Microsoft Enhanced DSS y Diffie-Hellman proveedor de servicios criptográficos"</dt> </dl> | [Microsoft Enhanced DSS y Diffie-Hellman proveedor de servicios criptográficos](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ ENH \_ RSA \_ AES \_ Prov**</dt> <dt>"proveedor de servicios criptográficos RSA y AES mejorado de Microsoft"</dt> </dl>         | [Proveedor de servicios criptográficos AES de Microsoft](microsoft-aes-cryptographic-provider.md).<br/> * * Windows XP: * * "proveedor de servicios criptográficos RSA y AES mejorado de Microsoft (prototipo)"<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_ \_**</dt> <dt>Proveedor de servicios criptográficos mejorados de Microsoft v 1.0</dt> mejorado </dl>                           | [Proveedor de servicios criptográficos mejorados de Microsoft](microsoft-enhanced-cryptographic-provider.md).<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_ \_**</dt> <dt>"Proveedor de cifrado de tarjeta inteligente básica de Microsoft"</dt> </dl>                                         | [Proveedor de servicios criptográficos de la tarjeta inteligente base de Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider).<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_ STRONG \_**</dt> <dt>"proveedor de servicios criptográficos seguros de Microsoft"</dt> </dl>                                        | [Proveedor de servicios criptográficos seguros de Microsoft](microsoft-strong-cryptographic-provider.md).<br/>                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
