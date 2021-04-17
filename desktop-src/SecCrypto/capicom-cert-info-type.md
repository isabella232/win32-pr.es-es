---
description: Define la información que se va a consultar desde un certificado.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Enumeración CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670784"
---
# <a name="capicom_cert_info_type-enumeration"></a>\_ \_ Enumeración de tipo de información de certificado de CAPICOM \_

El tipo de enumeración de tipo de información de certificado de CAPICOM define qué información se va a consultar desde un certificado. **\_ \_ \_**

## <a name="members"></a>Miembros



| Miembro                                         | Descripción                                                                                  | Value |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **\_ \_ \_ nombre simple del asunto de información \_ de certificado de CAPICOM \_** | Devuelve el nombre para mostrar del asunto del certificado.<br/>                              | 0     |
| **\_ \_ \_ nombre simple del emisor de información de \_ certificado de \_ CAPICOM**  | Devuelve el nombre para mostrar del emisor del certificado.<br/>                        | 1     |
| **\_nombre de \_ \_ \_ correo electrónico del asunto de información de certificado de CAPICOM \_**  | Devuelve la dirección de correo electrónico del firmante del certificado.<br/>                             | 2     |
| **\_nombre de \_ \_ \_ correo electrónico del emisor de información \_ de certificado de CAPICOM**   | Devuelve la dirección de correo electrónico del emisor del certificado.<br/>                       | 3     |
| **\_UPN de \_ asunto de información de certificado de CAPICOM \_ \_**          | Devuelve el UPN del firmante del certificado. Introducido en CAPICOM 2,0.<br/>            | 4     |
| **\_UPN del \_ emisor de información de certificado de \_ CAPICOM \_**           | Devuelve el UPN del emisor del certificado. Introducido en CAPICOM 2,0.<br/>      | 5     |
| **\_ \_ \_ nombre DNS del asunto de información \_ de certificado de CAPICOM \_**    | Devuelve el nombre DNS del firmante del certificado. Introducido en CAPICOM 2,0.<br/>       | 6     |
| **\_ \_ \_ nombre DNS del emisor de información de \_ certificado de \_ CAPICOM**     | Devuelve el nombre DNS del emisor del certificado. Introducido en CAPICOM 2,0.<br/> | 7     |



## <a name="remarks"></a>Observaciones

El tipo de enumeración de tipo de información de certificado de CAPICOM lo usa el método [**Certificate. GetInfo**](certificate-getinfo.md) . **\_ \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




