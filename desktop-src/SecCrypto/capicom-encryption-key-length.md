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
ms.openlocfilehash: 2957bd644fdf405fec7e82a487bf83af2cbae35ae305f10b9b168628a30b0749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772480"
---
# <a name="capicom_encryption_key_length-enumeration"></a>CAPICOM \_ ENCRYPTION KEY LENGTH \_ \_ (enumeración)

El **tipo de enumeración \_ CAPICOM ENCRYPTION KEY \_ \_ LENGTH** define la [*longitud de clave*](../secgloss/k-gly.md) que se usará en el cifrado.

## <a name="members"></a>Miembros



| Miembro                                          | Descripción                                                                               | Value     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **LONGITUD MÁXIMA DE LA \_ CLAVE \_ DE CIFRADO \_ CAPICOM \_**   | Usa la longitud máxima de clave disponible con el algoritmo de cifrado indicado.<br/> | 0         |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ \_ \_ 40 \_ BITS**  | Usa claves de 40 bits.<br/>                                                              | 1         |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ DE \_ \_ 56 \_ BITS**  | Usa claves de 56 bits si están disponibles.<br/>                                                 | 2         |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ DE \_ \_ 128 \_ BITS** | Usa claves de 128 bits si están disponibles.<br/>                                                | 3         |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ DE \_ \_ 192 \_ BITS** | Usa claves de 192 bits. Esta longitud de clave solo está disponible para AES.<br/>                  | 4 // v2.0 |
| **LONGITUD DE CLAVE DE CIFRADO CAPICOM \_ \_ DE \_ \_ 256 \_ BITS** | Usa claves de 256 bits. Esta longitud de clave solo está disponible para AES.<br/>                  | 5 // v2.0 |



## <a name="remarks"></a>Comentarios

La propiedad [**Algorithm.KeyLength**](algorithm-keylength.md) usa el tipo de enumeración **CAPICOM \_ ENCRYPTION KEY \_ \_ LENGTH.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
