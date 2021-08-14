---
description: Los identificadores siguientes se usan para identificar una interfaz criptográfica CNG.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Identificadores de interfaz CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ebadf561df916eedde1175a39911da55628b113022378cee9e74b61d021792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908276"
---
# <a name="cng-interface-identifiers"></a>Identificadores de interfaz CNG

Los identificadores siguientes se usan para identificar una interfaz criptográfica CNG. En CNG, una interfaz identifica el tipo de comportamiento criptográfico que admite un proveedor. Por ejemplo, un proveedor puede ser un generador de números aleatorios o puede ser un proveedor de hash.



| Constante o valor                                                                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ Cifrado \_ de la interfaz**</dt> <dt>0x00000001</dt> </dl>                                               | Interfaz de cifrado simétrica.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ Hash \_ INTERFACE**</dt> <dt>0x00000002</dt> </dl>                                                     | Interfaz hash.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ INTERFAZ \_ DE \_ CIFRADO ASIMÉTRICO**</dt> <dt>0x00000003</dt> </dl> | Interfaz de cifrado asimétrico.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ INTERFAZ \_ DEL \_ CONTRATO**</dt> SECRETO <dt>0x00000004</dt> </dl>                | Interfaz del contrato secreto.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ INTERFAZ \_ DE**</dt> <dt>FIRMA 0x00000005</dt> </dl>                                      | Interfaz de firma.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ Interfaz \_ de RNG**</dt> <dt>0x00000006</dt> </dl>                                                        | Interfaz del generador de números aleatorios.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ INTERFAZ \_ DE \_ ALMACENAMIENTO DE**</dt> CLAVES <dt>0x00010001</dt> </dl>                               | Interfaz de almacenamiento de claves.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ Interfaz \_ de SCHANNEL**</dt> <dt>0x00010002</dt> </dl>                                         | Interfaz de firma de Schannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ Interfaz de \_ firma \_ SCHANNEL**</dt> <dt>0x00010003</dt> </dl>          | Interfaz del conjunto de cifrado Schannel.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP y Windows 2000:** Este valor no se admite.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                |
| Header<br/>                   | <dl> <dt>Bcrypt.h; </dt> <dt>Ncrypt.h</dt> </dl> |



 

 




