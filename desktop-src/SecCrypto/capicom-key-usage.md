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
ms.openlocfilehash: bb477ee12b33c3d32fd2c48a56831dc2f56244b1e8a564cd2d0482e6e4a5d5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772430"
---
# <a name="capicom_key_usage-enumeration"></a>CAPICOM \_ KEY \_ USAGE (enumeración)

La **enumeración CAPICOM \_ KEY \_ USAGE** define las formas en que se puede usar una clave. Introducido en CAPICOM 2.0.

## <a name="members"></a>Miembros



| Miembro                                      | Descripción                                                                                                                      | Value      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **USO DE CLAVE \_ DE FIRMA DIGITAL \_ \_ CAPICOM \_** | La clave se puede usar para crear una firma digital.<br/>                                                                    | 0x00000080 |
| **USO DE LA \_ CLAVE CAPICOM SIN \_ \_ RECHAZO \_**   | La clave se puede usar para [*la norepudiation.*](../secgloss/n-gly.md)<br/> | 0x00000040 |
| **USO DE CLAVE DE CIFRADO DE CLAVE CAPICOM \_ \_ \_ \_**  | La clave se puede usar para cifrar una clave.<br/>                                                                                 | 0x00000020 |
| **USO DE CLAVE \_ DE CIFRADO DE DATOS \_ \_ \_ CAPICOM** | La clave se puede usar para cifrar los datos.<br/>                                                                                  | 0x00000010 |
| **USO DE CLAVE \_ DEL \_ CONTRATO DE CLAVE \_ CAPICOM \_**     | La clave se puede usar para el contrato de clave.<br/>                                                                                | 0x00000008 |
| **USO DE CLAVE \_ DE FIRMA DE CERTIFICADO DE \_ \_ \_ CLAVE \_ CAPICOM**    | La clave se puede usar para la firma de certificados de clave. Este valor es equivalente a CAPICOM \_ OFFLINE \_ CRL \_ SIGN KEY \_ \_ USAGE.<br/> | 0x00000004 |
| **USO DE CLAVE DE FIRMA \_ \_ DE CRL SIN CONEXIÓN \_ \_ DE \_ CAPICOM** | La clave se puede usar para la firma de certificados de clave. Este valor es equivalente a CAPICOM \_ KEY CERT SIGN KEY \_ \_ \_ \_ USAGE.<br/>    | 0x00000002 |
| **USO DE CLAVE \_ DE FIRMA DE CAPICOM CRL \_ \_ \_**          | La clave se puede usar para firmar.<br/>                                                                                      | 0x00000002 |
| **USO DE CLAVE \_ CAPICOM ENCIPHER \_ ONLY \_ \_**     | La clave solo se puede usar para cifrar.<br/>                                                                                  | 0x00000001 |
| **USO DE CLAVE \_ CAPICOM DECIPHER \_ ONLY \_ \_**     | La clave solo se puede usar para descifrar.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
