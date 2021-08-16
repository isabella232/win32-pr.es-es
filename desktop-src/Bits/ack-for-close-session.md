---
title: Ack for Close-Session
description: Use la confirmación para Close-Session paquete para confirmar la solicitud de Close-Session cliente. El servidor envía la confirmación después de liberar todos los recursos asociados a la sesión de carga.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Ack for Close-Session BITS
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289f2cfc2ca9f1e879e0aa592af28d86ae433f6e06d007aa71e00581baba2af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835418"
---
# <a name="ack-for-close-session"></a>Ack for Close-Session

Use el **paquete Ack for Close-Session** para confirmar la solicitud [**cerrar sesión del**](close-session.md) cliente. El servidor envía la confirmación después de liberar todos los recursos asociados a la sesión de carga.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Reemplace reason-code por el código de motivo HTTP. Por ejemplo, establezca reason-code en 200 si se ha hecho correctamente. Para obtener una lista de códigos de motivo HTTP, [vea RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Reemplace reason-description por la descripción HTTP asociada al código de motivo. Por ejemplo, establezca reason-description en Ok si reason-code es 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica este paquete de respuesta como un paquete Ack.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadena que identifica la sesión al cliente. Reemplace {guid} por el identificador de sesión que el cliente envió en el [**paquete de solicitud Cerrar**](close-session.md) sesión. Si no reconoce el identificador de sesión, establezca el encabezado BITS-Error-Code en BG \_ E \_ SESSION NOT \_ \_ FOUND.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud del contenido
</dt> <dd>

Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta. Se requiere content-length, incluso si el cuerpo de la respuesta no incluye contenido.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del lado servidor. Incluya solo este encabezado si el código de motivo no es 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Reemplace error-context por un número hexadecimal que represente el contexto en el que se produjo el error. Especifique el número hexadecimal para [**BG ERROR CONTEXT REMOTE \_ \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si el servidor generó el error. De lo contrario, especifique el número hexadecimal para **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) si la aplicación a la que se pasa el archivo de carga generó el error. Incluya este encabezado solo si el código de motivo no es 200 o 201.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El cliente bits vuelve a enviar el paquete [**Close-Session**](close-session.md) si el código de motivo está en el intervalo de 500 a 599, a menos que el encabezado BITS-Error-Code esté presente con un valor de BG \_ E SESSION NOT \_ \_ \_ FOUND. El cliente no volverá a intentarlo por los códigos de motivo del 100 al 499.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Ack for Cancel-Session**](ack-for-cancel-session.md)
</dt> <dt>

[**Cerrar sesión**](close-session.md)
</dt> </dl>

 

 




