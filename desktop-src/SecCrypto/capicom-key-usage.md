---
description: La \_ \_ enumeración de uso de claves de CAPICOM define las maneras en las que se puede usar una clave. Introducido en CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Enumeración CAPICOM_KEY_USAGE (CAPICOM. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649779"
---
# <a name="capicom_key_usage-enumeration"></a>\_Enumeración de uso de clave de CAPICOM \_

La enumeración de **\_ \_ uso de claves de CAPICOM** define las maneras en las que se puede usar una clave. Introducido en CAPICOM 2,0.

## <a name="members"></a>Miembros



| Miembro                                      | Descripción                                                                                                                      | Value      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **uso de la \_ \_ clave de firma digital \_ de CAPICOM \_** | La clave se puede utilizar para crear una firma digital.<br/>                                                                    | 0x00000080 |
| **uso de la clave de CAPICOM \_ sin \_ repudio \_ \_**   | La clave se puede utilizar para el no [*rechazo*](../secgloss/n-gly.md).<br/> | 0x00000040 |
| **uso de la \_ \_ clave de cifrado de clave de \_ CAPICOM \_**  | La clave se puede usar para cifrar una clave.<br/>                                                                                 | 0x00000020 |
| **uso de la \_ \_ clave de cifrado de datos de \_ CAPICOM \_** | La clave se puede usar para cifrar los datos.<br/>                                                                                  | 0x00000010 |
| **uso de la clave del acuerdo de \_ tecla CAPICOM \_ \_ \_**     | La clave se puede usar para el acuerdo de claves.<br/>                                                                                | 0x00000008 |
| **uso de la \_ \_ clave de firma de certificado \_ \_ \_ de CAPICOM**    | La clave se puede usar para la firma de certificados de clave. Este valor es equivalente al uso de la \_ clave de signo de CRL sin conexión de CAPICOM \_ \_ \_ \_ .<br/> | 0x00000004 |
| **uso de la \_ clave de signo de CRL sin conexión de CAPICOM \_ \_ \_ \_** | La clave se puede usar para la firma de certificados de clave. Este valor es equivalente al uso de la clave de firma de certificado de CAPICOM \_ \_ \_ \_ \_ .<br/>    | 0x00000002 |
| **uso de la clave de signo de \_ CRL de CAPICOM \_ \_ \_**          | La clave se puede utilizar para firmar.<br/>                                                                                      | 0x00000002 |
| **CAPICOM \_ \_ solo cifrado \_ uso de claves \_**     | La clave solo se puede usar para cifrar.<br/>                                                                                  | 0x00000001 |
| **CAPICOM \_ descifrar \_ solo el \_ uso de claves \_**     | La clave solo se puede usar para descifrar.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
