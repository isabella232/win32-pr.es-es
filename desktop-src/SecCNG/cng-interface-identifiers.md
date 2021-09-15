---
description: Los identificadores siguientes se usan para identificar una interfaz criptográfica CNG.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Identificadores de interfaz CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f75de82e198e0471b48175a080012b9b40eed9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271220"
---
# <a name="cng-interface-identifiers"></a>Identificadores de interfaz CNG

Los identificadores siguientes se usan para identificar una interfaz criptográfica CNG. En CNG, una interfaz identifica el tipo de comportamiento criptográfico que admite un proveedor. Por ejemplo, un proveedor puede ser un generador de números aleatorios o puede ser un proveedor de hash.



| Constante o valor                                                                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ INTERFAZ \_ DE CIFRADO**</dt> <dt>0x00000001</dt> </dl>                                               | Interfaz de cifrado simétrica.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ Interfaz \_ hash**</dt> <dt>0x00000002</dt> </dl>                                                     | Interfaz hash.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ INTERFAZ \_ DE \_ CIFRADO ASIMÉTRICO**</dt> <dt>0x00000003</dt> </dl> | Interfaz de cifrado asimétrica.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ INTERFAZ \_ DEL \_ CONTRATO**</dt> SECRETO <dt>0x00000004</dt> </dl>                | Interfaz del contrato secreto.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ INTERFAZ \_ DE FIRMA**</dt> <dt>0x00000005</dt> </dl>                                      | Interfaz de firma.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ Interfaz \_ de RNG**</dt> <dt>0x00000006</dt> </dl>                                                        | Interfaz del generador de números aleatorios.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ INTERFAZ \_ DE \_ ALMACENAMIENTO DE**</dt> CLAVES <dt>0x00010001</dt> </dl>                               | Interfaz de almacenamiento de claves.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ Interfaz \_ de SCHANNEL**</dt> <dt>0x00010002</dt> </dl>                                         | Interfaz de firma de Schannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ Interfaz de \_ firma \_ SCHANNEL**</dt> <dt>0x00010003</dt> </dl>          | Interfaz del conjunto de cifrado Schannel.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP y Windows 2000:** Este valor no se admite.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Bcrypt.h; </dt> <dt>Ncrypt.h</dt> </dl> |



 

 




