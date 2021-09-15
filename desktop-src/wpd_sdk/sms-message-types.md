---
description: El tipo \_ de enumeración SMS MESSAGE \_ TYPES describe el tipo de contenido de un mensaje de servicio de mensajes cortos (SMS).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: SMS_MESSAGE_TYPES enumeración (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574261"
---
# <a name="sms_message_types-enumeration"></a>Enumeración \_ SMS MESSAGE \_ TYPES

El **tipo \_ de \_ enumeración SMS MESSAGE TYPES** describe el tipo de contenido de un mensaje de servicio de mensajes cortos (SMS).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**MENSAJE \_ DE TEXTO \_ SMS**
</dt> <dd>

Mensaje de texto.

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**MENSAJE \_ BINARIO \_ DE SMS**
</dt> <dd>

Mensaje binario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El comando SMS SEND de [**WPD \_ usa esta \_ \_ enumeración.**](wpd-command-sms-send-command.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




