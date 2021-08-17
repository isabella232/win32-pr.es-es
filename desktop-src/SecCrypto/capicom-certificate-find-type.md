---
description: El tipo de enumeración CAPICOM CERTIFICATE FIND TYPE define el tipo de criterios de \_ \_ búsqueda \_ usados para buscar certificados específicos. Este tipo de enumeración se introdujo en CAPICOM 2.0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: CAPICOM_CERTIFICATE_FIND_TYPE enumeración (Capicom.h)
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
ms.openlocfilehash: fb10b9289ae094f27fe29c3f2723d639eccc029aa7e5512833ac7e859c5c36ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772700"
---
# <a name="capicom_certificate_find_type-enumeration"></a>ENUMERACIÓN CAPICOM \_ CERTIFICATE \_ FIND \_ TYPE

El **tipo de enumeración CAPICOM \_ CERTIFICATE FIND \_ \_ TYPE** define el tipo de criterios de búsqueda usados para buscar certificados específicos. Este tipo de enumeración se introdujo en CAPICOM 2.0.

## <a name="members"></a>Miembros



| Miembro                                                | Descripción                                                                                                                                 | Value |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH**            | Devuelve certificados que coinciden con un hash SHA1 especificado.<br/>                                                                             | 0     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ SUBJECT \_ NAME**         | Devuelve certificados cuyo nombre de sujeto coincide exactamente o parcialmente con un nombre de sujeto especificado.<br/>                                   | 1     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ ISSUER \_ NAME**          | Devuelve certificados cuyo nombre de emisor coincide exactamente o parcialmente con un nombre de emisor especificado.<br/>                                     | 2     |
| **CAPICOM CERTIFICATE FIND ROOT NAME (BUSCAR \_ NOMBRE RAÍZ DEL CERTIFICADO \_ \_ \_ CAPICOM)**            | Devuelve certificados cuyo nombre de sujeto raíz coincide exactamente o parcialmente con un nombre de sujeto raíz especificado.<br/>                         | 3     |
| **NOMBRE DE LA PLANTILLA \_ DE BUSCAR \_ CERTIFICADO \_ CAPICOM \_**        | Devuelve certificados cuyo nombre de plantilla coincide con un nombre de plantilla especificado.<br/>                                                      | 4     |
| **EXTENSIÓN CAPICOM \_ CERTIFICATE \_ FIND \_**             | Devuelve certificados que tienen una extensión que coincide con una extensión especificada.<br/>                                                  | 5     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ EXTENDED \_ PROPERTY**    | Devuelve certificados que tienen una propiedad extendida cuyo identificador de propiedad coincide con un identificador de propiedad especificado.<br/>           | 6     |
| **DIRECTIVA DE APLICACIÓN \_ DE BÚSQUEDA DE CERTIFICADOS \_ \_ CAPICOM \_**   | Devuelve certificados del almacén que tienen una extensión de uso de clave mejorada o una propiedad combinada con un identificador de uso.<br/> | 7     |
| **DIRECTIVA DE BUSCAR CERTIFICADO DE CAPICOM \_ \_ \_ \_**   | Devuelve certificados que contienen un OID de directiva especificado.<br/>                                                                          | 8     |
| **TIEMPO DE ENCONTRAR EL CERTIFICADO CAPICOM \_ \_ \_ \_ VÁLIDO**           | Devuelve certificados cuya hora es válida.<br/>                                                                                        | 9     |
| **EL TIEMPO DE \_ DE IDENTIFICACIÓN DEL CERTIFICADO \_ \_ CAPICOM AÚN NO ES \_ \_ \_ VÁLIDO** | Devuelve certificados cuya hora aún no es válida.<br/>                                                                                | 10    |
| **TIEMPO DE ENCONTRAR CERTIFICADO CAPICOM \_ \_ \_ \_ EXPIRADO**         | Devuelve certificados cuya hora ha expirado.<br/>                                                                                     | 11    |
| **USO DE LA CLAVE \_ DE \_ BUSCAR CERTIFICADO \_ CAPICOM \_**            | Devuelve certificados que contienen una clave que se puede usar de la manera especificada.<br/>                                                  | 12    |



## <a name="remarks"></a>Comentarios

El método [**Certificates.Find**](certificates-find.md) usa el tipo de enumeración **CAPICOM \_ CERTIFICATE \_ FIND \_** TYPE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




