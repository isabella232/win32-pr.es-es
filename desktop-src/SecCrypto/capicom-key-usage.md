---
description: La enumeración CAPICOM \_ KEY USAGE define las formas en que se puede usar una \_ clave. Introducido en CAPICOM 2.0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: CAPICOM_KEY_USAGE enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171141"
---
# <a name="capicom_key_usage-enumeration"></a>CAPICOM \_ KEY \_ USAGE (enumeración)

La **enumeración CAPICOM \_ KEY \_ USAGE** define las formas en que se puede usar una clave. Introducido en CAPICOM 2.0.

## <a name="members"></a>Members



| Miembro                                      | Descripción                                                                                                                      | Value      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **USO DE CLAVE \_ DE FIRMA DIGITAL \_ \_ CAPICOM \_** | La clave se puede usar para crear una firma digital.<br/>                                                                    | 0x00000080 |
| **USO DE CLAVE \_ DE \_ NO RECHAZO DE \_ CAPICOM \_**   | La clave se puede usar para [*la no reesudiación.*](../secgloss/n-gly.md)<br/> | 0x00000040 |
| **USO DE CLAVE \_ \_ CAPICOM KEY ENCIPHERMENT \_ \_**  | La clave se puede usar para cifrar una clave.<br/>                                                                                 | 0x00000020 |
| **USO DE CLAVE \_ DE CIFRADO DE DATOS \_ \_ \_ CAPICOM** | La clave se puede usar para cifrar los datos.<br/>                                                                                  | 0x00000010 |
| **USO DE CLAVE \_ DE CONTRATO \_ DE \_ CAPICOM \_**     | La clave se puede usar para el contrato de clave.<br/>                                                                                | 0x00000008 |
| **USO DE CLAVE \_ CAPICOM KEY CERT SIGN \_ \_ \_ \_ KEY**    | La clave se puede usar para la firma de certificados de clave. Este valor es equivalente a CAPICOM \_ OFFLINE \_ CRL \_ SIGN KEY \_ \_ USAGE.<br/> | 0x00000004 |
| **USO DE CLAVE DE FIRMA \_ \_ DE CRL SIN CONEXIÓN DE \_ \_ CAPICOM \_** | La clave se puede usar para la firma de certificados de clave. Este valor es equivalente a CAPICOM \_ KEY CERT SIGN KEY \_ \_ \_ \_ USAGE.<br/>    | 0x00000002 |
| **USO DE CLAVE \_ DE FIRMA DE CAPICOM CRL \_ \_ \_**          | La clave se puede usar para firmar.<br/>                                                                                      | 0x00000002 |
| **USO DE CLAVE \_ CAPICOM ENCIPHER \_ ONLY \_ \_**     | La clave solo se puede usar para cifrar.<br/>                                                                                  | 0x00000001 |
| **USO DE CLAVE \_ CAPICOM DECIPHER \_ ONLY \_ \_**     | La clave solo se puede usar para descifrar.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
