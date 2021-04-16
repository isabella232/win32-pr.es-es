---
description: Establece o recupera la longitud de la clave.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Algorithm. KeyLength (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689987"
---
# <a name="algorithmkeylength-property"></a>Algorithm. KeyLength (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **KeyLength** establece o recupera la longitud de la clave.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Valor de propiedad

Un valor de la enumeración de longitud de la [**\_ \_ clave \_ de cifrado CAPICOM**](capicom-encryption-key-length.md) que especifica la longitud de la clave. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                        | Significado                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**\_ \_ \_ longitud máxima de la clave de CIFRAdo de CAPICOM \_**</dt> </dl>     | Usar la longitud de clave máxima disponible con el algoritmo de cifrado indicado.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 40 \_ bits**</dt> </dl>    | Usar claves de 40 bits.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 56 \_ bits**</dt> </dl>    | Use claves de 56 bits si está disponible.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 128 \_ bits**</dt> </dl> | Use claves de 128 bits si está disponible.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 192 \_ bits**</dt> </dl> | Usar claves de 192 bits. Esta longitud de clave solo está disponible para AES.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 256 \_ bits**</dt> </dl> | Usar claves de 256 bits. Esta longitud de clave solo está disponible para AES.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Cuando se utilizan algoritmos de cifrado DES y 3DES, las longitudes de clave son estándar y se omite la propiedad **KeyLength** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Algoritmo**](algorithm.md)
</dt> </dl>

 

 
