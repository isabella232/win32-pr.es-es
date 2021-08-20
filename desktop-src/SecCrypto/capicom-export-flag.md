---
description: El tipo de enumeración CAPICOM EXPORT FLAG define si se omiten los errores de exportación \_ \_ de claves privadas.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: CAPICOM_EXPORT_FLAG enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d6be9953640eeb2eb1d6c7fad812f5efe2d2da2f6888a01b4450c638ab68bfca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772470"
---
# <a name="capicom_export_flag-enumeration"></a>CAPICOM \_ EXPORT \_ FLAG (enumeración)

El **tipo de enumeración CAPICOM \_ EXPORT \_ FLAG** define si se omiten los errores de exportación de claves privadas.

## <a name="members"></a>Miembros



| Miembro                                                            | Descripción                                               | Value |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **CAPICOM \_ EXPORT \_ DEFAULT**                                      | Los errores de exportación de claves privadas no se omiten.<br/> | 0     |
| **ERROR NO EXPORTABLE DE LA EXPORTACIÓN DE CAPICOM \_ IGNORE PRIVATE KEY NOT \_ \_ \_ \_ \_ \_ EXPORTABLE** | Se omiten los errores de exportación de claves privadas.<br/>     | 1     |



## <a name="remarks"></a>Comentarios

El siguiente método usa el tipo de \_ enumeración CAPICOM EXPORT \_ FLAG:

-   [**Certificates.Save**](certificates-save.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




