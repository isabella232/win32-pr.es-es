---
description: Define los identificadores de las propiedades de CAPICOM.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: Enumeración CAPICOM_PROPID (CAPICOM. h)
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
ms.openlocfilehash: d817262b869ef694c2cf9ff5b1e577840c3168a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670709"
---
# <a name="capicom_propid-enumeration"></a>CAPICOM \_ PROPID (enumeración)

La enumeración de el **\_ PROPID de CAPICOM** define los identificadores de las propiedades de CAPICOM.

## <a name="members"></a>Miembros



| Miembro                                                 | Descripción                                                                                                                                                                                                                                                                                | Value      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **no se \_ conoce el PROPID de CAPICOM \_**                           | No se conoce el tipo de la propiedad.<br/>                                                                                                                                                                                                                                          | 0          |
| **\_identificador de \_ Prov de clave \_ \_ de CAPICOM PROPID**                 | Identificador de un contenedor de claves dentro de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        | 1          |
| **\_información de \_ Prov de clave \_ \_ de CAPICOM PROPID**                   | Información sobre un contenedor de claves dentro de un CSP.<br/>                                                                                                                                                                                                                                 | 2          |
| **HASH de SHA1 de CAPICOM \_ PROPID \_ \_**                        | Objeto hash SHA1.<br/>                                                                                                                                                                                                                                                             | 3          |
| **\_ \_ propiedades hash de el PROPID de CAPICOM \_**                        | Propiedades de un objeto hash.<br/>                                                                                                                                                                                                                                                | 3          |
| **\_ \_ Hash MD5 del PROPID de CAPICOM \_**                         | Objeto hash MD5.<br/>                                                                                                                                                                                                                                                             | 4          |
| **contexto de clave de CAPICOM \_ PROPID \_ \_**                      | [*Contexto*](../secgloss/c-gly.md)de la clave.<br/>                                                                                                                                                                                                | 5          |
| **Especificación de clave de CAPICOM \_ PROPID \_ \_**                         | Especificaciones de una clave.<br/>                                                                                                                                                                                                                                                   | 6          |
| **CAPICOM \_ PROPID \_ IE30 \_ Reserved**                    | Información acerca de si el objeto está reservado en Internet Explorer 3,0.<br/>                                                                                                                                                                                                      | 7          |
| **se \_ ha \_ \_ reservado el hash de PUBKEY de CAPICOM PROPID \_**            | Información sobre si el hash de la clave pública está reservado.<br/>                                                                                                                                                                                                               | 8          |
| **\_uso de \_ ENHKEY del PROPID de CAPICOM \_**                     | Un [*uso mejorado de clave*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              | 9          |
| **\_uso de \_ CTL del PROPID de CAPICOM \_**                        | Un uso de la [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).<br/>                                                                                                                                             | 9          |
| **\_ \_ siguiente ubicación de \_ actualización \_ de CAPICOM PROPID**            | La ubicación de la siguiente actualización de la [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               | 10         |
| **\_ \_ nombre descriptivo de CAPICOM PROPID \_**                    | Un nombre legible.<br/>                                                                                                                                                                                                                                                          | 11         |
| **\_ \_ archivo PVK del PROPID de CAPICOM \_**                         | Un archivo que contiene una clave privada.<br/>                                                                                                                                                                                                                                             | 12         |
| **Descripción de la PROPID de CAPICOM \_ \_**                       | Una descripción legible.<br/>                                                                                                                                                                                                                                                   | 13         |
| **Estado de acceso de CAPICOM \_ PROPID \_ \_**                     | Estado del acceso.<br/>                                                                                                                                                                                                                                                        | 14         |
| **HASH de firma de CAPICOM \_ PROPID \_ \_**                   | Un hash de la firma.<br/>                                                                                                                                                                                                                                                        | 15         |
| **\_datos de \_ \_ tarjeta inteligente \_ de CAPICOM PROPID**                 | Datos de la tarjeta inteligente.<br/>                                                                                                                                                                                                                                                                | 16         |
| **\_EFS PROPID de CAPICOM \_**                               | [*Sistema de cifrado de archivos*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **datos de la \_ \_ información Fortezza del PROPID de CAPICOM \_**                    | Los datos creados mediante los protocolos criptográficos y los algoritmos que pertenecen al [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> | 18         |
| **CAPICOM \_ PROPID \_ archived**                          | Información sobre si el objeto se ha archivado.<br/>                                                                                                                                                                                                                               | 19         |
| **identificador de clave de CAPICOM \_ PROPID \_ \_**                   | Identificador de clave.<br/>                                                                                                                                                                                                                                                               | 20         |
| **\_ \_ inscripción automática de CAPICOM PROPID \_**                      | Información de inscripción automática de un certificado.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ PROPID \_ PUBKEY \_ alg \_ para**                 | Parámetros de un algoritmo de clave pública.<br/>                                                                                                                                                                                                                                          | 22         |
| **\_puntos de \_ distribución de certificados cruzados del PROPID de \_ \_ CAPICOM \_**         | Información utilizada para actualizar los certificados cruzados dinámicos.<br/>                                                                                                                                                                                                                          | 23         |
| **\_ \_ \_ \_ Hash MD5 de clave pública \_ del emisor \_ de CAPICOM PROPID**    | El hash MD5 de la clave pública del emisor.<br/>                                                                                                                                                                                                                                        | 24         |
| **\_Hash MD5 del asunto de la \_ \_ clave pública del sujeto \_ \_ de \_ CAPICOM**   | El hash MD5 de la clave pública del sujeto.<br/>                                                                                                                                                                                                                                       | 25         |
| **inscripción de CAPICOM \_ PROPID \_**                        | Información sobre la inscripción del certificado.<br/>                                                                                                                                                                                                                                 | 26         |
| **marca de fecha de CAPICOM \_ PROPID \_ \_**                       | Una marca de fecha.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **Número de serie del emisor de CAPICOM del \_ \_ \_ \_ \_ \_ algoritmo hash MD5** | El hash MD5 del número de serie del emisor.<br/>                                                                                                                                                                                                                                     | 28         |
| **Nombre del firmante de CAPICOM \_ PROPID \_ \_ \_ \_ hash MD5**          | El hash MD5 del nombre del sujeto.<br/>                                                                                                                                                                                                                                             | 29         |
| **\_información de \_ \_ error extendido \_ de CAPICOM PROPID**             | Información ampliada sobre un error.<br/>                                                                                                                                                                                                                                            | 30         |
| **\_renovación del PROPID de CAPICOM \_**                           | Información sobre la renovación de una [*entidad de certificación*](../secgloss/c-gly.md).<br/>                                                                                                                     | 64         |
| **\_hash de \_ clave archivada de CAPICOM PROPID \_ \_**               | Un hash archivado de una clave.<br/>                                                                                                                                                                                                                                                      | 65         |
| **se \_ ha \_ reservado primero el PROPID de CAPICOM \_**                   | Información sobre la primera reserva.<br/>                                                                                                                                                                                                                                        | 66         |
| **se \_ ha \_ reservado por última vez CAPICOM PROPID \_**                    | Información sobre la reserva más reciente.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **\_ \_ primer \_ usuario de CAPICOM PROPID**                       | Información sobre el primer usuario.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **\_ \_ último \_ usuario de CAPICOM PROPID**                        | Información sobre el usuario más reciente.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Observaciones

Esta enumeración se usa en las siguientes propiedades de CAPICOM:

-   [**ExtendedProperty. PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties. Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
