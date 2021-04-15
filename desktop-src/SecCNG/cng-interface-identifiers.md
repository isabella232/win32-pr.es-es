---
description: Los identificadores siguientes se usan para identificar una interfaz criptográfica de CNG.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Identificadores de interfaz CNG (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f75de82e198e0471b48175a080012b9b40eed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666259"
---
# <a name="cng-interface-identifiers"></a>Identificadores de interfaz CNG

Los identificadores siguientes se usan para identificar una interfaz criptográfica de CNG. En CNG, una interfaz identifica el tipo de comportamiento criptográfico que admite un proveedor. Por ejemplo, un proveedor puede ser un generador de números aleatorios o puede ser un proveedor de hash.



| Constante o valor                                                                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ CIPHER \_ interface**</dt> <dt>0x00000001</dt> </dl>                                               | La interfaz de cifrado simétrico.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ \_Interfaz hash**</dt> <dt>0x00000002</dt> </dl>                                                     | La interfaz hash.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Interfaz de cifrado asimétrico**</dt> <dt>0x00000003</dt> </dl> | La interfaz de cifrado asimétrico.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Interfaz de acuerdo secreto**</dt> <dt>0x00000004</dt> </dl>                | La interfaz del acuerdo secreto.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ \_Interfaz de signatura**</dt> <dt>0x00000005</dt> </dl>                                      | Interfaz de firma.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ \_Interfaz RNG**</dt> <dt>0x00000006</dt> </dl>                                                        | La interfaz del generador de números aleatorios.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interfaz de almacenamiento de claves**</dt> <dt>0x00010001</dt> </dl>                               | La interfaz de almacenamiento de claves.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ SCHANNEL ( \_ interfaz**</dt> ) <dt>0x00010002</dt> </dl>                                         | Interfaz de firma Schannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interfaz de firma Schannel**</dt> <dt>0x00010003</dt> </dl>          | La interfaz del conjunto de cifrado Schannel.<br/> **Windows server 2008, Windows Vista, Windows server 2003, Windows XP y windows 2000:** Este valor no se admite.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Bcrypt. h; </dt> <dt>Ncrypt. h</dt> </dl> |



 

 




