---
description: Define qué certificados de una cadena se guardan.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: CAPICOM_CERTIFICATE_INCLUDE_OPTION enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 5b6bb2cd36d6ce8ca422d680a05a1e84318d745981a8ca15d9de0be3dfe45c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879395"
---
# <a name="capicom_certificate_include_option-enumeration"></a>CAPICOM \_ CERTIFICATE INCLUDE OPTION \_ \_ (enumeración)

El **tipo de enumeración CAPICOM \_ CERTIFICATE INCLUDE \_ \_ OPTION** define qué certificados de una cadena se guardan. Este tipo de enumeración se introdujo en CAPICOM 2.0.

## <a name="members"></a>Miembros



| Miembro                                                 | Descripción                                                                           | Value |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERTIFICATE \_ INCLUDE \_ CHAIN \_ EXCEPT \_ ROOT** | Guarda todos los certificados de la cadena con la excepción de la entidad raíz.<br/> | 0     |
| **EL CERTIFICADO CAPICOM \_ \_ INCLUYE CADENA \_ \_ COMPLETA**        | Guarda la cadena de certificados completa.<br/>                                      | 1     |
| **EL CERTIFICADO CAPICOM \_ \_ INCLUYE SOLO ENTIDAD \_ \_ \_ FINAL**   | Guarda solo el certificado de entidad final.<br/>                                     | 2     |



## <a name="remarks"></a>Comentarios

El método [**Certificate.Save**](certificate-save.md) usa el tipo de enumeración **CAPICOM \_ CERTIFICATE INCLUDE \_ \_ OPTION.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




