---
description: El tipo de enumeración \_ WPD SMS \_ ENCODING TYPES describe el tipo de codificación de un mensaje corto del servicio de mensajes \_ (SMS).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: WPD_SMS_ENCODING_TYPES enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 648815f8a82248151b19f5c753bf3e42643d61eb507501d907c5ac54a2b226b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927685"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>Enumeración WPD \_ SMS \_ ENCODING \_ TYPES

El **tipo de enumeración \_ WPD SMS \_ ENCODING \_ TYPES** describe el tipo de codificación de un mensaje corto del servicio de mensajes (SMS).

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**CODIFICACIÓN DE SMS \_ \_ DE 7 \_ BITS**
</dt> <dd>

Codificación de siete bits.

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**CODIFICACIÓN DE SMS \_ \_ DE 8 \_ BITS**
</dt> <dd>

Codificación de ocho bits.

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**CODIFICACIÓN DE SMS \_ \_ UTF \_ 16**
</dt> <dd>

Codificación de 16 bits (UTF).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración la usa la [propiedad WPD \_ SMS \_ ENCODING.](sms-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




