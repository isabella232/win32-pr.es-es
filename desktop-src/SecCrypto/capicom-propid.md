---
description: Define los identificadores de propiedad CAPICOM.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: CAPICOM_PROPID enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROPID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 6d99c823d5396d2b8ece4484fa8888dff19b7898fb7d3b6ebedc5841b85c7e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772271"
---
# <a name="capicom_propid-enumeration"></a>CAPICOM \_ PROPID (enumeración)

La **enumeración \_ CAPICOM PROPID** define los identificadores de propiedad CAPICOM.

## <a name="members"></a>Miembros



| Miembro                                                 | Descripción                                                                                                                                                                                                                                                                                | Valor      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ PROPID \_ UNKNOWN**                           | No se conoce el tipo de la propiedad.<br/>                                                                                                                                                                                                                                          | 0          |
| **CAPICOM \_ PROPID \_ KEY \_ PROV \_ HANDLE**                 | Identificador de un contenedor de claves dentro de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        | 1          |
| **CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO**                   | Información sobre un contenedor de claves dentro de un CSP.<br/>                                                                                                                                                                                                                                 | 2          |
| **CAPICOM \_ PROPID \_ SHA1 \_ HASH**                        | Objeto hash SHA1.<br/>                                                                                                                                                                                                                                                             | 3          |
| **CAPICOM \_ PROPID \_ HASH \_ PROP**                        | Propiedades de un objeto hash.<br/>                                                                                                                                                                                                                                                | 3          |
| **CAPICOM \_ PROPID \_ MD5 \_ HASH**                         | Objeto hash MD5.<br/>                                                                                                                                                                                                                                                             | 4          |
| **CONTEXTO CLAVE \_ DE CAPICOM PROPID \_ \_**                      | Contexto de [*clave*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                | 5          |
| **CAPICOM \_ PROPID \_ KEY \_ SPEC**                         | Especificaciones de una clave.<br/>                                                                                                                                                                                                                                                   | 6          |
| **CAPICOM \_ PROPID \_ IE30 \_ RESERVED**                    | Información sobre si el objeto está reservado en Internet Explorer 3.0.<br/>                                                                                                                                                                                                      | 7          |
| **CAPICOM \_ PROPID \_ PUBKEY \_ HASH \_ RESERVED**            | Información sobre si el hash de la clave pública está reservado.<br/>                                                                                                                                                                                                               | 8          |
| **CAPICOM \_ PROPID \_ ENHKEY \_ USAGE**                     | Un [*uso mejorado de clave*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              | 9          |
| **USO DE \_ CAPICOM PROPID \_ CTL \_**                        | Uso [*de una lista de confianza*](../secgloss/c-gly.md) de certificados (CTL).<br/>                                                                                                                                             | 9          |
| **CAPICOM \_ PROPID \_ NEXT \_ UPDATE \_ LOCATION**            | Ubicación de la siguiente actualización de la [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               | 10         |
| **NOMBRE DESCRIPTIVO \_ DE CAPICOM PROPID \_ \_**                    | Un nombre legible para el usuario.<br/>                                                                                                                                                                                                                                                          | 11         |
| **ARCHIVO CAPICOM \_ PROPID \_ \_ PVK**                         | Archivo que contiene una clave privada.<br/>                                                                                                                                                                                                                                             | 12         |
| **CAPICOM \_ PROPID \_ DESCRIPTION**                       | Una descripción legible para el ser humano.<br/>                                                                                                                                                                                                                                                   | 13         |
| **CAPICOM \_ PROPID \_ ACCESS \_ STATE**                     | Estado del acceso.<br/>                                                                                                                                                                                                                                                        | 14         |
| **CAPICOM \_ PROPID \_ SIGNATURE \_ HASH**                   | Hash de la firma.<br/>                                                                                                                                                                                                                                                        | 15         |
| **DATOS DE TARJETA \_ INTELIGENTE CAPICOM PROPID \_ \_ \_**                 | Datos de tarjeta inteligente.<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM \_ PROPID \_ EFS**                               | Un [*Sistema de cifrado de archivos*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **CAPICOM \_ PROPID \_ FORTEZZA \_ DATA**                    | Datos creados mediante los protocolos criptográficos y algoritmos propiedad del [*Instituto Nacional de Estándares y Tecnología*](../secgloss/n-gly.md) (NIST).<br/> | 18         |
| **CAPICOM \_ PROPID \_ ARCHIVADO**                          | Información sobre si el objeto está archivado.<br/>                                                                                                                                                                                                                               | 19         |
| **CAPICOM \_ PROPID \_ KEY \_ IDENTIFIER**                   | Identificador de clave.<br/>                                                                                                                                                                                                                                                               | 20         |
| **CAPICOM \_ PROPID \_ AUTO \_ ENROLL**                      | Información de inscripción automática para un certificado.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ PARA**                 | Parámetros para un algoritmo de clave pública.<br/>                                                                                                                                                                                                                                          | 22         |
| **PUNTOS DE DISTRIBUCIÓN \_ DE CERTIFICADOS \_ CRUZADOS DE \_ \_ CAPICOM PROPID \_**         | Información utilizada para actualizar certificados cruzados dinámicos.<br/>                                                                                                                                                                                                                          | 23         |
| **HASH \_ \_ \_ \_ \_ MD5 \_ DE CLAVE PÚBLICA DEL EMISOR DE CAPICOM PROPID**    | Hash MD5 de la clave pública del emisor.<br/>                                                                                                                                                                                                                                        | 24         |
| **CAPICOM \_ PROPID \_ SUBJECT \_ PUBLIC \_ KEY \_ MD5 \_ HASH**   | Hash MD5 de la clave pública del sujeto.<br/>                                                                                                                                                                                                                                       | 25         |
| **INSCRIPCIÓN DE CAPICOM \_ PROPID \_**                        | Información sobre la inscripción del certificado.<br/>                                                                                                                                                                                                                                 | 26         |
| **CAPICOM \_ PROPID \_ DATE \_ STAMP**                       | Una marca de fecha.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **CAPICOM \_ PROPID \_ ISSUER \_ SERIAL \_ NUMBER \_ MD5 \_ HASH** | Hash MD5 del número de serie del emisor.<br/>                                                                                                                                                                                                                                     | 28         |
| **CAPICOM \_ PROPID \_ SUBJECT \_ NAME \_ MD5 \_ HASH**          | Hash MD5 del nombre del sujeto.<br/>                                                                                                                                                                                                                                             | 29         |
| **CAPICOM \_ PROPID \_ EXTENDED \_ ERROR \_ INFO**             | Información ampliada sobre un error.<br/>                                                                                                                                                                                                                                            | 30         |
| **RENOVACIÓN DE CAPICOM \_ PROPID \_**                           | Información sobre la renovación de una [*entidad de certificación.*](../secgloss/c-gly.md)<br/>                                                                                                                     | 64         |
| **CAPICOM \_ PROPID \_ ARCHIVED \_ KEY \_ HASH**               | Hash archivado de una clave.<br/>                                                                                                                                                                                                                                                      | 65         |
| **CAPICOM \_ PROPID \_ FIRST \_ RESERVED**                   | Información sobre la primera reserva.<br/>                                                                                                                                                                                                                                        | 66         |
| **CAPICOM \_ PROPID \_ LAST \_ RESERVED**                    | Información sobre la reserva más reciente.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **CAPICOM \_ PROPID \_ FIRST \_ USER**                       | Información sobre el primer usuario.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **ÚLTIMO USUARIO DE CAPICOM \_ PROPID \_ \_**                        | Información sobre el usuario más reciente.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Comentarios

Esta enumeración se usa en las siguientes propiedades CAPICOM:

-   [**ExtendedProperty.PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties.Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
