---
description: Se usa con las funciones CryptAcquireContext y CryptSetProvider.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Nombres de proveedor de servicios criptográficos (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c9b41aaeacb0b03df4b2fc0c608ae1f98e59ac0a581a395eb9904d0ec8e235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768691"
---
# <a name="cryptographic-provider-names"></a>Nombres de proveedor de servicios criptográficos

Los siguientes [*nombres de proveedor de servicios*](../secgloss/c-gly.md) criptográficos (CSP) se definen en Wincrypt.h. Estas constantes se usan con las [**funciones CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) y [**CryptSetProvider.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera)



| Constante o valor                                                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ DH \_ SCHANNEL \_ PROV**</dt> <dt>"Proveedor criptográfico Schannel de Microsoft DH"</dt> </dl>      | El [proveedor criptográfico DSS y Diffie-Hellman/Schannel de Microsoft](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ DH \_ PROV**</dt> <dt>"Microsoft Base DSS and Diffie-Hellman Cryptographic Provider"</dt> </dl>     | Microsoft [Base DSS y Diffie-Hellman criptográfico](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ PROV**</dt> <dt>"Proveedor criptográfico DSS base de Microsoft"</dt> </dl>                                  | Proveedor [criptográfico DSS de Microsoft](microsoft-dss-cryptographic-provider.md).<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_ DEF \_ PROV**</dt> <dt>"Proveedor criptográfico base de Microsoft v1.0"</dt> </dl>                                              | Proveedor [criptográfico base de Microsoft](microsoft-base-cryptographic-provider.md).<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SCHANNEL \_ PROV**</dt> <dt>"Proveedor criptográfico de Microsoft RSA Schannel"</dt> </dl>  | Proveedor [criptográfico RSA/Schannel de Microsoft](microsoft-rsa-schannel-cryptographic-provider.md).<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SIG \_ PROV**</dt> <dt>"Proveedor criptográfico de firma RSA de Microsoft"</dt> </dl>                | No [se admite el proveedor criptográfico](microsoft-rsa-signature-cryptographic-provider.md) de firma RSA de Microsoft.<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ ENH \_ DSS \_ DH \_ PROV**</dt> <dt>"Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider"</dt> </dl> | Microsoft [Enhanced DSS y Diffie-Hellman cryptographic provider](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ ENH \_ RSA \_ AES \_ PROV**</dt> <dt>"Microsoft Enhanced RSA and AES Cryptographic Provider"</dt> </dl>         | Proveedor [criptográfico AES de Microsoft](microsoft-aes-cryptographic-provider.md).<br/> **Windows XP: **"Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype)"<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_ PROV \_ MEJORADO**</dt> <dt>"Proveedor criptográfico mejorado de Microsoft v1.0"</dt> </dl>                           | Proveedor [de servicios criptográficos mejorado de Microsoft](microsoft-enhanced-cryptographic-provider.md).<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_ SCARD \_ PROV**</dt> <dt>"Proveedor de criptografía de tarjeta inteligente base de Microsoft"</dt> </dl>                                         | Proveedor [de servicios criptográficos de tarjeta inteligente base de Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider).<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_ STRONG \_ PROV**</dt> <dt>"Proveedor de servicios criptográficos fuerte de Microsoft"</dt> </dl>                                        | Proveedor [de servicios criptográficos fuerte de Microsoft](microsoft-strong-cryptographic-provider.md).<br/>                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
