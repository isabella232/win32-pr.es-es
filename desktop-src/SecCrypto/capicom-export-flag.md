---
description: El tipo de enumeración de la marca de exportación de CAPICOM \_ \_ define si se omiten los errores de exportación de clave privada.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Enumeración CAPICOM_EXPORT_FLAG (CAPICOM. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670783"
---
# <a name="capicom_export_flag-enumeration"></a>\_Enumeración de marcas de exportación de CAPICOM \_

El tipo de enumeración de la **\_ \_ marca de exportación de CAPICOM** define si se omiten los errores de exportación de clave privada.

## <a name="members"></a>Miembros



| Miembro                                                            | Descripción                                               | Value |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **\_ \_ configuración predeterminada de CAPICOM**                                      | Los errores de exportación de claves privadas no se pasan por alto.<br/> | 0     |
| **ERROR de exportación de CAPICOM \_ \_ omitir \_ \_ clave privada \_ no \_ exportable \_** | Se omiten los errores de exportación de claves privadas.<br/>     | 1     |



## <a name="remarks"></a>Observaciones

El tipo de enumeración de la marca de exportación de CAPICOM \_ \_ se usa en el método siguiente:

-   [**Certificados. guardar**](certificates-save.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




