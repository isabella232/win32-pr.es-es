---
description: El tipo de enumeración WPD SMS ENCODING TYPES describe el tipo de codificación de un mensaje de servicio de \_ \_ mensajes cortos \_ (SMS).
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
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247028"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>Enumeración WPD \_ SMS \_ ENCODING \_ TYPES

El **tipo de enumeración \_ WPD SMS \_ ENCODING \_ TYPES** describe el tipo de codificación de un mensaje de servicio de mensajes cortos (SMS).

## <a name="syntax"></a>Sintaxis


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

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la [propiedad WPD \_ SMS \_ ENCODING.](sms-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




