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
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171158"
---
# <a name="capicom_hash_algorithm-enumeration"></a>CAPICOM \_ HASH \_ ALGORITHM (enumeración)

La **enumeración CAPICOM \_ HASH \_ ALGORITHM** define un algoritmo hash.

## <a name="members"></a>Members



| Miembro                                 | Descripción                                                                                                                                                                 | Value |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **ALGORITMO \_ HASH CAPICOM \_ \_ SHA1**     | [*Algoritmo hash seguro*](../secgloss/s-gly.md) (SHA) que genera un resumen de mensajes de 160 bits.<br/> | 0     |
| **ALGORITMO \_ HASH CAPICOM \_ \_ MD2**      | Algoritmo de hash MD2.<br/>                                                                                                                                           | 1     |
| **ALGORITMO \_ HASH CAPICOM \_ \_ MD4**      | Algoritmo de hash MD4.<br/>                                                                                                                                           | 2     |
| **ALGORITMO \_ HASH CAPICOM \_ \_ MD5**      | Algoritmo de hash MD5.<br/>                                                                                                                                           | 3     |
| **ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 256** | Algoritmo hash SHA-256.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 4     |
| **ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 384** | Algoritmo hash SHA-384.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 5     |
| **ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 512** | Algoritmo hash SHA-512.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 6     |



## <a name="remarks"></a>Observaciones

La propiedad [**HashedData.Algorithm**](hasheddata-algorithm.md) usa la enumeración **\_ CAPICOM HASH \_ ALGORITHM.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
