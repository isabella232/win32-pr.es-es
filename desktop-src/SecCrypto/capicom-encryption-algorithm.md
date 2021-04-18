---
description: Define los algoritmos que se van a usar en el cifrado y el descifrado.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Enumeración CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670856"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>\_Enumeración del algoritmo de cifrado CAPICOM \_

El tipo de enumeración del **\_ \_ algoritmo de cifrado de CAPICOM** define los algoritmos que se van a utilizar en el cifrado y descifrado.

## <a name="members"></a>Miembros



| Miembro                                   | Descripción                                                                                                                                                                                              | Value     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **\_Algoritmo de cifrado de CAPICOM \_ \_ RC2**  | Use el cifrado RSA RC2.<br/>                                                                                                                                                                       | 0         |
| **\_Algoritmo de cifrado de CAPICOM \_ \_ RC4**  | Usar el cifrado RSA RC4.<br/>                                                                                                                                                                       | 1         |
| **\_ \_ algoritmo des de cifrado de CAPICOM \_**  | Use el cifrado DES.<br/>                                                                                                                                                                           | 2         |
| **\_Algoritmo de cifrado \_ \_ 3DES de CAPICOM** | Use el cifrado Triple DES.<br/>                                                                                                                                                                    | 3         |
| **\_algoritmo de cifrado de CAPICOM \_ \_ AES**  | Use el algoritmo [*estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES). Este valor solo es válido para el objeto [**EncryptedData**](encrypteddata.md) .<br/> | 4//v 2.0 |



## <a name="remarks"></a>Observaciones

La propiedad [**algorithm.Name**](algorithm-name.md) usa el tipo de enumeración del **\_ \_ algoritmo de cifrado CAPICOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
