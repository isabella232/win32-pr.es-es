---
description: El \_ \_ \_ tipo de enumeración buscar certificado de CAPICOM define el tipo de criterio de búsqueda usado para buscar certificados específicos. Este tipo de enumeración se presentó en CAPICOM 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Enumeración CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670505"
---
# <a name="capicom_certificate_find_type-enumeration"></a>\_ \_ Enumeración de tipo de búsqueda de certificado de CAPICOM \_

El tipo de enumeración **\_ \_ Buscar \_ certificado de CAPICOM** define el tipo de criterio de búsqueda usado para buscar certificados específicos. Este tipo de enumeración se presentó en CAPICOM 2,0.

## <a name="members"></a>Miembros



| Miembro                                                | Descripción                                                                                                                                 | Value |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **Certificado de CAPICOM, \_ \_ Buscar \_ \_ hash SHA1**            | Devuelve certificados que coinciden con un hash SHA1 especificado.<br/>                                                                             | 0     |
| **\_el certificado de CAPICOM \_ encuentra \_ \_ el nombre del firmante**         | Devuelve certificados cuyo nombre de sujeto coincide exactamente o parcialmente con un nombre de sujeto especificado.<br/>                                   | 1     |
| **\_nombre del \_ emisor de búsqueda de certificado de \_ CAPICOM \_**          | Devuelve certificados cuyo nombre de emisor coincide exactamente o parcialmente con un nombre de emisor especificado.<br/>                                     | 2     |
| **nombre de la raíz del certificado de CAPICOM \_ \_ \_ \_**            | Devuelve certificados cuyo nombre de sujeto raíz coincide exactamente o parcialmente con un nombre de sujeto raíz especificado.<br/>                         | 3     |
| **\_nombre de \_ plantilla de búsqueda de certificado de CAPICOM \_ \_**        | Devuelve certificados cuyo nombre de plantilla coincide con un nombre de plantilla especificado.<br/>                                                      | 4     |
| **\_extensión de \_ búsqueda de certificado de CAPICOM \_**             | Devuelve los certificados que tienen una extensión que coincide con una extensión especificada.<br/>                                                  | 5     |
| **\_ \_ \_ propiedad extendida de búsqueda de certificado de CAPICOM \_**    | Devuelve los certificados que tienen una propiedad extendida cuyo identificador de propiedad coincide con un identificador de propiedad especificado.<br/>           | 6     |
| **\_Directiva de \_ aplicación de búsqueda de certificado de CAPICOM \_ \_**   | Devuelve los certificados del almacén que tienen una extensión de uso mejorado de clave o una propiedad combinada con un identificador de uso.<br/> | 7     |
| **\_Directiva de \_ certificado de búsqueda \_ \_ de certificado de CAPICOM**   | Devuelve certificados que contienen un OID de directiva especificado.<br/>                                                                          | 8     |
| **tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ válido**           | Devuelve certificados cuya hora es válida.<br/>                                                                                        | 9     |
| **tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ no \_ \_ válido todavía** | Devuelve certificados cuya hora todavía no es válida.<br/>                                                                                | 10    |
| **tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ expirado**         | Devuelve los certificados cuya hora ha expirado.<br/>                                                                                     | 11    |
| **uso de la clave de certificado de CAPICOM \_ \_ \_ \_**            | Devuelve certificados que contienen una clave que se puede usar de la manera especificada.<br/>                                                  | 12    |



## <a name="remarks"></a>Observaciones

El método Certificates [**. Find**](certificates-find.md) usa el tipo de enumeración **\_ \_ Buscar \_ certificado de CAPICOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




