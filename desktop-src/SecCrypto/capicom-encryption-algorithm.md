---
description: Define los algoritmos que se usarán en el cifrado y descifrado.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: CAPICOM_ENCRYPTION_ALGORITHM enumeración (Capicom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171178"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>CAPICOM \_ ENCRYPTION \_ ALGORITHM (enumeración)

El **tipo de enumeración \_ CAPICOM ENCRYPTION \_ ALGORITHM** define los algoritmos que se usarán en el cifrado y descifrado.

## <a name="members"></a>Members



| Miembro                                   | Descripción                                                                                                                                                                                              | Value     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **ALGORITMO DE CIFRADO CAPICOM \_ \_ \_ RC2**  | Use el cifrado RSA RC2.<br/>                                                                                                                                                                       | 0         |
| **ALGORITMO DE CIFRADO CAPICOM \_ \_ \_ RC4**  | Use el cifrado RSA RC4.<br/>                                                                                                                                                                       | 1         |
| **CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ DES**  | Use el cifrado DES.<br/>                                                                                                                                                                           | 2         |
| **ALGORITMO DE CIFRADO CAPICOM \_ \_ \_ 3DES** | Use el cifrado DES triple.<br/>                                                                                                                                                                    | 3         |
| **ALGORITMO DE CIFRADO \_ \_ CAPICOM \_ AES**  | Use el [*algoritmo Estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES). Este valor solo es válido para [**el objeto EncryptedData.**](encrypteddata.md)<br/> | 4 // v2.0 |



## <a name="remarks"></a>Observaciones

El **tipo de enumeración \_ CAPICOM ENCRYPTION \_ ALGORITHM** se usa en [**la Algorithm.Name**](algorithm-name.md) propiedad .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
