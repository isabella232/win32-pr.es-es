---
description: El \_ \_ tipo de enumeración SMS Message Types describe el tipo de contenido de un mensaje de servicio de mensajes cortos (SMS).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Enumeración SMS_MESSAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718712"
---
# <a name="sms_message_types-enumeration"></a>\_Enumeración de tipos de mensajes SMS \_

El tipo de enumeración **SMS \_ Message \_** Types describe el tipo de contenido de un mensaje de servicio de mensajes cortos (SMS).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**\_mensaje de texto SMS \_**
</dt> <dd>

Un mensaje de texto.

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**\_mensaje binario de SMS \_**
</dt> <dd>

Un mensaje binario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa el comando de [**envío de SMS de comandos de WPD \_ \_ \_**](wpd-command-sms-send-command.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




