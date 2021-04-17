---
description: Define qué certificados de una cadena se guardan.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Enumeración CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
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
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671133"
---
# <a name="capicom_certificate_include_option-enumeration"></a>\_ \_ Enumeración de opciones de inclusión de certificado de CAPICOM \_

El tipo de enumeración de la **\_ \_ \_ opción incluir certificado de CAPICOM** define qué certificados de una cadena se guardan. Este tipo de enumeración se presentó en CAPICOM 2,0.

## <a name="members"></a>Miembros



| Miembro                                                 | Descripción                                                                           | Value |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **el \_ certificado de CAPICOM \_ incluye una \_ cadena excepto la \_ \_ raíz** | Guarda todos los certificados de la cadena con la excepción de la entidad raíz.<br/> | 0     |
| **el \_ certificado de CAPICOM \_ incluye una \_ \_ cadena entera**        | Guarda la cadena de certificados completa.<br/>                                      | 1     |
| **el \_ certificado de CAPICOM \_ incluye \_ \_ solo la entidad final \_**   | Guarda solo el certificado de entidad final.<br/>                                     | 2     |



## <a name="remarks"></a>Observaciones

El método [**Certificate. Save**](certificate-save.md) usa el tipo de enumeración de la **\_ opción de \_ inclusión \_ de certificado CAPICOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




