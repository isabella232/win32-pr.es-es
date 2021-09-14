---
description: El tipo de enumeración CAPICOM EXPORT FLAG define si se omiten los \_ errores de exportación de claves \_ privadas.
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
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171161"
---
# <a name="capicom_export_flag-enumeration"></a>ENUMERACIÓN CAPICOM \_ EXPORT \_ FLAG

El **tipo de enumeración CAPICOM \_ EXPORT \_ FLAG** define si se omiten los errores de exportación de claves privadas.

## <a name="members"></a>Members



| Miembro                                                            | Descripción                                               | Value |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **CAPICOM \_ EXPORT \_ DEFAULT**                                      | Los errores de exportación de claves privadas no se omiten.<br/> | 0     |
| **ERROR NO EXPORTABLE DE LA CLAVE PRIVADA OMITIBLE \_ \_ DE LA \_ \_ \_ \_ EXPORTACIÓN DE \_ CAPICOM** | Se omiten los errores de exportación de claves privadas.<br/>     | 1     |



## <a name="remarks"></a>Observaciones

El siguiente método usa el tipo de \_ enumeración CAPICOM EXPORT \_ FLAG:

-   [**Certificates.Save**](certificates-save.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




