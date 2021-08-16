---
title: Ack for Ping
description: Use el paquete Ack for Ping para confirmar la solicitud Ping del cliente.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Ack for Ping BITS
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f31850599331027f3f8135a42dac8c8ea54519c04291d42fb06b5c7b8735fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835185"
---
# <a name="ack-for-ping"></a>Ack for Ping

Use el **paquete Ack for Ping** para confirmar la solicitud Ping [**del**](ping.md) cliente.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
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

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud del contenido
</dt> <dd>

Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta. Obligatorio incluso si el cuerpo de la respuesta no incluye contenido.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del lado servidor. Incluya este encabezado solo si el código de motivo no es 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Reemplace error-context por un número hexadecimal que represente el contexto en el que se produjo el error. Especifique el número hexadecimal para [**BG ERROR CONTEXT REMOTE \_ \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si el servidor generó el error. De lo contrario, especifique el número hexadecimal para **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) si la aplicación a la que se pasa el archivo de carga generó el error. Incluya este encabezado solo si el código de motivo no es 200 o 201.

</dd> </dl>

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 




