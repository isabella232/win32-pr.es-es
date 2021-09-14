---
description: Define la longitud de clave que se va a usar en el cifrado.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: CAPICOM_ENCRYPTION_KEY_LENGTH enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171177"
---
# <a name="capicom_encryption_key_length-enumeration"></a>CAPICOM \_ ENCRYPTION KEY LENGTH \_ \_ (enumeración)

El **tipo de enumeración CAPICOM \_ ENCRYPTION KEY \_ \_ LENGTH** define la [*longitud de clave*](../secgloss/k-gly.md) que se usará en el cifrado.

## <a name="members"></a>Members



| Miembro                                          | Descripción                                                                               | Value     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **LONGITUD MÁXIMA DE LA \_ \_ CLAVE DE CIFRADO \_ CAPICOM \_**   | Usa la longitud máxima de clave disponible con el algoritmo de cifrado indicado.<br/> | 0         |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ DE \_ \_ 40 \_ BITS**  | Usa claves de 40 bits.<br/>                                                              | 1         |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ DE \_ \_ 56 \_ BITS**  | Usa claves de 56 bits si están disponibles.<br/>                                                 | 2         |
| **LONGITUD DE CLAVE \_ DE CIFRADO CAPICOM DE \_ \_ \_ 128 \_ BITS** | Usa claves de 128 bits si están disponibles.<br/>                                                | 3         |
| **LONGITUD DE CLAVE \_ DE CIFRADO CAPICOM DE \_ \_ \_ 192 \_ BITS** | Usa claves de 192 bits. Esta longitud de clave solo está disponible para AES.<br/>                  | 4 // v2.0 |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ DE \_ \_ 256 \_ BITS** | Usa claves de 256 bits. Esta longitud de clave solo está disponible para AES.<br/>                  | 5 // v2.0 |



## <a name="remarks"></a>Observaciones

La propiedad [**Algorithm.KeyLength**](algorithm-keylength.md) usa el tipo de enumeración **CAPICOM \_ ENCRYPTION KEY \_ \_ LENGTH.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
