---
title: Confirmación para Close-Session
description: Use la confirmación de Close-Session paquete para confirmar la solicitud de Close-Session del cliente. El servidor envía la confirmación después de liberar todos los recursos asociados a la sesión de carga.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Confirmación de Close-Session BITS
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7142bfd8d1d5d65d1f669a328c75a2c8cdfb036
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104149720"
---
# <a name="ack-for-close-session"></a>Confirmación para Close-Session

Use el paquete **ACK for Close-Session** para confirmar la solicitud de [**cierre de sesión**](close-session.md) del cliente. El servidor envía la confirmación después de liberar todos los recursos asociados a la sesión de carga.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo
</dt> <dd>

Reemplace Reason-Code por el código de motivo HTTP. Por ejemplo, establezca Reason-Code en 200 si se realiza correctamente. Para obtener una lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>razón: Descripción
</dt> <dd>

Reemplace Reason-Description por la descripción de HTTP asociada al código de motivo. Por ejemplo, establezca Reason-Description en OK si Reason-Code es 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo
</dt> <dd>

Identifica este paquete de respuesta como un paquete de confirmación.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS
</dt> <dd>

GUID de cadena que identifica la sesión en el cliente. Reemplace {GUID} por el identificador de sesión que el cliente envió en el paquete de solicitud de [**sesión cerrada**](close-session.md) . Si no reconoce el identificador de sesión, establezca el encabezado BITS-error-código en la sesión de \_ BG \_ E \_ no \_ encontrada.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido
</dt> <dd>

Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta. La longitud del contenido es obligatoria, incluso si el cuerpo de la respuesta no incluye contenido.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BIT-error-código
</dt> <dd>

Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del servidor. Incluya solo este encabezado si Reason-Code no es 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-error-contexto
</dt> <dd>

Reemplace error-context por un número hexadecimal que representa el contexto en el que se produjo el error. Especifique el número hexadecimal del [**\_ \_ \_ \_ archivo remoto de contexto de error de BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0X5) si el servidor ha generado el error. En caso contrario, especifique el número hexadecimal de la **\_ \_ \_ \_ aplicación remota de contexto de error de BG** (0X7) si el error fue generado por la aplicación a la que se pasa el archivo de carga. Incluya este encabezado solo si el código de motivo no es 200 o 201.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El cliente de BITS reenvía el paquete de [**sesión de cierre**](close-session.md) si el código de motivo está en el intervalo de 500 a 599, a menos que el encabezado bits-error-Code esté presente con un valor de la \_ sesión BG E \_ \_ no \_ se encuentre. El cliente no volverá a intentarlo por los códigos de motivo 100 a 499.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Confirmación para cancelar sesión**](ack-for-cancel-session.md)
</dt> <dt>

[**Sesión de cierre**](close-session.md)
</dt> </dl>

 

 




