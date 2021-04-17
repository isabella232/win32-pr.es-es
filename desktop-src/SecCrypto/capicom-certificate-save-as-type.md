---
description: Define el formato de un archivo que contiene información del certificado.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Enumeración CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670855"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_ \_ \_ Enumeración de tipo guardar certificado de CAPICOM \_

El tipo de enumeración de **certificado de CAPICOM de \_ \_ tipo "Save \_ as \_** " define el formato de un archivo que contiene información del certificado. CAPICOM 2,0 presentó este tipo de enumeración.

## <a name="members"></a>Miembros



| Miembro                                  | Descripción                                                                                                                                   | Value |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **el \_ certificado \_ de CAPICOM se guarda \_ como \_ pfx** | El archivo de salida se formateará como archivo PFX (PKCS 12) y también se guardarán las claves privadas asociadas que se puedan exportar.<br/> | 0     |
| **\_certificado \_ de CAPICOM guardar \_ como \_ cer** | El archivo de salida se formateará como un archivo CER sin ninguna clave privada guardada.<br/>                                                        | 1     |



## <a name="remarks"></a>Observaciones

El método [**Certificate. Save**](certificate-save.md) usa el tipo de enumeración de **\_ \_ \_ \_ tipo guardar certificado de CAPICOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




