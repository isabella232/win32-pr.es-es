---
description: Define qué información se va a consultar desde un certificado.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: CAPICOM_CERT_INFO_TYPE enumeración (Capicom.h)
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
ms.openlocfilehash: 480238556fce0470c51f00c394dd8566160686561342ec91da2e136c44a43cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879425"
---
# <a name="capicom_cert_info_type-enumeration"></a>CAPICOM \_ CERT INFO TYPE \_ \_ (enumeración)

El **tipo de enumeración \_ CAPICOM CERT INFO \_ \_ TYPE** define qué información se va a consultar desde un certificado.

## <a name="members"></a>Miembros



| Miembro                                         | Descripción                                                                                  | Value |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **NOMBRE SIMPLE DEL ASUNTO \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM \_** | Devuelve el nombre para mostrar del sujeto del certificado.<br/>                              | 0     |
| **NOMBRE SIMPLE DEL EMISOR \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM \_**  | Devuelve el nombre para mostrar del emisor del certificado.<br/>                        | 1     |
| **NOMBRE DE CORREO ELECTRÓNICO DEL ASUNTO \_ DE LA INFORMACIÓN DEL \_ \_ \_ CERTIFICADO \_ CAPICOM**  | Devuelve la dirección de correo electrónico del sujeto del certificado.<br/>                             | 2     |
| **NOMBRE DE CORREO ELECTRÓNICO DEL EMISOR \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ \_ CAPICOM**   | Devuelve la dirección de correo electrónico del emisor del certificado.<br/>                       | 3     |
| **UPN DEL ASUNTO \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM**          | Devuelve el UPN del firmante del certificado. Introducido en CAPICOM 2.0.<br/>            | 4     |
| **UPN DEL EMISOR \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM**           | Devuelve el UPN del emisor del certificado. Introducido en CAPICOM 2.0.<br/>      | 5     |
| **NOMBRE DNS DEL ASUNTO \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM \_**    | Devuelve el nombre DNS del sujeto del certificado. Introducido en CAPICOM 2.0.<br/>       | 6     |
| **NOMBRE DNS DEL EMISOR \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM \_**     | Devuelve el nombre DNS del emisor del certificado. Introducido en CAPICOM 2.0.<br/> | 7     |



## <a name="remarks"></a>Comentarios

El método [**Certificate.GetInfo**](certificate-getinfo.md) usa el tipo de enumeración **\_ CAPICOM CERT INFO \_ \_ TYPE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




