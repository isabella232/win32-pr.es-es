---
description: El \_ \_ \_ tipo de enumeración de tipos de codificación SMS de WPD describe el tipo de codificación de un mensaje de servicio de mensajes cortos (SMS).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Enumeración WPD_SMS_ENCODING_TYPES (PortableDevice. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650072"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>\_ \_ Enumeración de tipos de codificación SMS de WPD \_

El tipo de enumeración de **\_ \_ \_ tipos de codificación SMS de WPD** describe el tipo de codificación de un mensaje de servicio de mensajes cortos (SMS).

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

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**\_Codificación SMS de \_ 7 \_ bits**
</dt> <dd>

Codificación de siete bits.

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**CODIFICACIÓN de SMS de \_ \_ 8 \_ bits**
</dt> <dd>

Codificación de ocho bits.

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**\_Codificación de SMS \_ UTF \_ 16**
</dt> <dd>

Codificación de dieciséis bits (UTF).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la propiedad de [ \_ \_ codificación de SMS de WPD](sms-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




