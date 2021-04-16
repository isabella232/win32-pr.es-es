---
description: Define la longitud de la clave que se va a utilizar en el cifrado.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Enumeración CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671788"
---
# <a name="capicom_encryption_key_length-enumeration"></a>\_ \_ Enumeración de longitud de clave de cifrado de CAPICOM \_

El tipo de enumeración longitud de la **\_ \_ clave \_ de cifrado de CAPICOM** define la [*longitud de clave*](../secgloss/k-gly.md) que se va a utilizar en el cifrado.

## <a name="members"></a>Miembros



| Miembro                                          | Descripción                                                                               | Value     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **\_ \_ \_ longitud máxima de la clave de CIFRAdo de CAPICOM \_**   | Utiliza la longitud de clave máxima disponible con el algoritmo de cifrado indicado.<br/> | 0         |
| **La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 40 \_ bits**  | Utiliza claves de 40 bits.<br/>                                                              | 1         |
| **La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 56 \_ bits**  | Utiliza claves de 56 bits si están disponibles.<br/>                                                 | 2         |
| **La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 128 \_ bits** | Utiliza claves de 128 bits si están disponibles.<br/>                                                | 3         |
| **La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 192 \_ bits** | Utiliza claves de 192 bits. Esta longitud de clave solo está disponible para AES.<br/>                  | 4//v 2.0 |
| **La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 256 \_ bits** | Utiliza claves de 256 bits. Esta longitud de clave solo está disponible para AES.<br/>                  | 5//v 2.0 |



## <a name="remarks"></a>Observaciones

La propiedad [**algorithm. KeyLength**](algorithm-keylength.md) usa el tipo de enumeración longitud de la **\_ \_ clave \_ de cifrado CAPICOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
