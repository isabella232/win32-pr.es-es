---
description: Define el formato de un archivo que contiene información de certificado.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: CAPICOM_CERTIFICATE_SAVE_AS_TYPE enumeración (Capicom.h)
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
ms.openlocfilehash: 2000bd582475a227fdb638649ee1a634e488a21a7c09d84dd6e21dafc5e9aa42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772646"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>CAPICOM \_ CERTIFICATE SAVE AS TYPE \_ \_ \_ (enumeración)

El **tipo de enumeración CAPICOM \_ CERTIFICATE SAVE AS \_ \_ \_ TYPE** define el formato de un archivo que contiene información de certificado. CAPICOM 2.0 introdujo este tipo de enumeración.

## <a name="members"></a>Miembros



| Miembro                                  | Descripción                                                                                                                                   | Value |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CERTIFICADO CAPICOM \_ \_ GUARDAR COMO \_ \_ PFX** | El archivo de salida se formateará como un archivo PFX (PKCS 12) y también se guardarán las claves privadas asociadas que sean exportables.<br/> | 0     |
| **CAPICOM \_ CERTIFICATE \_ SAVE \_ AS \_ CER** | El archivo de salida se formateará como un archivo CER sin claves privadas guardadas.<br/>                                                        | 1     |



## <a name="remarks"></a>Comentarios

El método [**Certificate.Save**](certificate-save.md) usa el tipo de enumeración **CAPICOM \_ CERTIFICATE SAVE AS \_ \_ \_ TYPE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




