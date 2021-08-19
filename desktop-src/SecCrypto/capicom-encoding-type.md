---
description: Indica el tipo de codificación utilizado.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: CAPICOM_ENCODING_TYPE enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1ec9a9ea1de4e3f501c94394ec9038d39c9b881c1e2bb1f41322d4f08c2db922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772490"
---
# <a name="capicom_encoding_type-enumeration"></a>CAPICOM \_ ENCODING \_ TYPE (enumeración)

El **tipo de enumeración \_ CAPICOM ENCODING \_ TYPE** indica el tipo de codificación utilizado.

## <a name="members"></a>Miembros



| Miembro                      | Descripción                                                                                                                                                                                 | Value      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ ENCODE \_ ANY**    | Los datos se guardan como una cadena codificada en base64 o una secuencia binaria pura. Este tipo de codificación solo se usa para los datos de entrada que tienen un tipo de codificación desconocido. Introducido en CAPICOM 2.0.<br/> | 0xffffffff |
| **CAPICOM \_ ENCODE \_ BASE64** | Los datos se guardan como una cadena codificada en base64.<br/>                                                                                                                                        | 0          |
| **CAPICOM \_ ENCODE \_ BINARY** | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Comentarios

Los siguientes métodos y propiedades CAPICOM usan este tipo de enumeración:

-   [**Método Certificate.Export**](certificate-export.md)
-   [**Propiedad EncodedData.Value**](encodeddata-value.md)
-   [**Método EncryptedData.Encrypt**](encrypteddata-encrypt.md)
-   [**Método EnvelopedData.Encrypt**](envelopeddata-encrypt.md)
-   [**Propiedad ExtendedProperty.Value**](extendedproperty-value.md)
-   [**Método SignedData.Sign**](signeddata-sign.md)
-   [**Método SignedData.CoSign**](signeddata-cosign.md)
-   [**Método Store.Export**](store-export.md)
-   [**Método Utilities.GetRandom**](utilities-getrandom.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




