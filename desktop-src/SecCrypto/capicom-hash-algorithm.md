---
description: La \_ \_ enumeración del algoritmo hash CAPICOM define un algoritmo hash.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Enumeración CAPICOM_HASH_ALGORITHM (CAPICOM. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670781"
---
# <a name="capicom_hash_algorithm-enumeration"></a>\_ \_ Enumeración de algoritmos hash CAPICOM

La enumeración del **\_ \_ algoritmo hash CAPICOM** define un algoritmo hash.

## <a name="members"></a>Miembros



| Miembro                                 | Descripción                                                                                                                                                                 | Value |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_Algoritmo hash de CAPICOM \_ \_ SHA1**     | [*Algoritmo hash seguro*](../secgloss/s-gly.md) (SHA) que genera una síntesis del mensaje de 160 bits.<br/> | 0     |
| **\_Algoritmo hash de CAPICOM \_ \_ MD2**      | Algoritmo de hash MD2.<br/>                                                                                                                                           | 1     |
| **\_Algoritmo hash \_ CAPICOM \_ MD4**      | Algoritmo de hash MD4.<br/>                                                                                                                                           | 2     |
| **\_Algoritmo hash de CAPICOM \_ \_ MD5**      | Algoritmo de hash MD5.<br/>                                                                                                                                           | 3     |
| **\_Algoritmo hash de CAPICOM \_ \_ Sha \_ 256** | Algoritmo hash SHA-256.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 4     |
| **\_Algoritmo hash de CAPICOM \_ \_ Sha \_ 384** | Algoritmo hash SHA-384.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 5     |
| **\_Algoritmo hash de CAPICOM \_ \_ Sha \_ 512** | Algoritmo hash SHA-512.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/>                                                                 | 6     |



## <a name="remarks"></a>Observaciones

La propiedad [**HashedData. algorithm**](hasheddata-algorithm.md) utiliza la enumeración del **\_ \_ algoritmo hash CAPICOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
