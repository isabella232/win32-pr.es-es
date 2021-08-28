---
description: La enumeración CAPICOM \_ HASH ALGORITHM define un algoritmo \_ hash.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: CAPICOM_HASH_ALGORITHM enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: df312c7e1ed578150069ff335527a20a2185c721b67a9e0e02cc1d57938b1cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879145"
---
# <a name="capicom_hash_algorithm-enumeration"></a>CAPICOM \_ HASH \_ ALGORITHM (enumeración)

La **enumeración CAPICOM \_ HASH \_ ALGORITHM** define un algoritmo hash.

## <a name="members"></a>Miembros



| Miembro                                 | Descripción                                                                                                                                                                 | Value |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **ALGORITMO \_ HASH CAPICOM \_ \_ SHA1**     | [*Algoritmo hash seguro*](../secgloss/s-gly.md) (SHA) que genera un resumen de mensajes de 160 bits.<br/> | 0     |
| **ALGORITMO \_ HASH CAPICOM \_ \_ MD2**      | Algoritmo de hash MD2.<br/>                                                                                                                                           | 1     |
| **ALGORITMO \_ HASH CAPICOM \_ \_ MD4**      | Algoritmo de hash MD4.<br/>                                                                                                                                           | 2     |
| **ALGORITMO \_ HASH CAPICOM \_ \_ MD5**      | Algoritmo de hash MD5.<br/>                                                                                                                                           | 3     |
| **ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 256** | Algoritmo hash SHA-256.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 4     |
| **ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 384** | Algoritmo hash SHA-384.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 5     |
| **ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 512** | Algoritmo hash SHA-512.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 6     |



## <a name="remarks"></a>Comentarios

La propiedad [**HashedData.Algorithm**](hasheddata-algorithm.md) usa la enumeración **\_ CAPICOM HASH \_ ALGORITHM.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
