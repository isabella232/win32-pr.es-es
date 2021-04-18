---
description: Indica el tipo de codificación utilizado.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Enumeración CAPICOM_ENCODING_TYPE (CAPICOM. h)
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
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671518"
---
# <a name="capicom_encoding_type-enumeration"></a>\_Enumeración de tipo de codificación de CAPICOM \_

El tipo de enumeración de **\_ \_ tipo de codificación de CAPICOM** indica el tipo de codificación utilizado.

## <a name="members"></a>Miembros



| Miembro                      | Descripción                                                                                                                                                                                 | Value      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ codificar \_ any**    | Los datos se guardan como una cadena codificada en base64 o en una secuencia binaria pura. Este tipo de codificación solo se usa para los datos de entrada que tienen un tipo de codificación desconocido. Introducido en CAPICOM 2,0.<br/> | 0xFFFFFFFF |
| **CAPICOM, codificación \_ \_ Base64** | Los datos se guardan como una cadena codificada en Base64.<br/>                                                                                                                                        | 0          |
| **\_código binario de codificación de CAPICOM \_** | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Observaciones

Este tipo de enumeración se usa en los siguientes métodos y propiedades de CAPICOM:

-   Método [**Certificate. Export**](certificate-export.md)
-   [**EncodedData. Value**](encodeddata-value.md) (propiedad)
-   [**EncryptedData. Encrypt**](encrypteddata-encrypt.md) (método)
-   [**EnvelopedData. Encrypt**](envelopeddata-encrypt.md) (método)
-   [**ExtendedProperty. Value**](extendedproperty-value.md) (propiedad)
-   [**SignedData. Sign**](signeddata-sign.md) (método)
-   [**SignedData. Cosign**](signeddata-cosign.md) (método)
-   [**Store. Export**](store-export.md) (método)
-   [**Utilities. GetRandom**](utilities-getrandom.md) (método)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




