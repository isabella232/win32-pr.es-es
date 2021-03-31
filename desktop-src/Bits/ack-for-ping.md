---
title: Confirmación del ping
description: Use el paquete de confirmación de ping para confirmar la solicitud de ping del cliente.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Confirmación de los BITS de ping
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103995720"
---
# <a name="ack-for-ping"></a>Confirmación del ping

Use el paquete **de confirmación de ping** para confirmar la solicitud de [**ping**](ping.md) del cliente.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
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

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido
</dt> <dd>

Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta. Obligatorio incluso si el cuerpo de la respuesta no incluye contenido.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BIT-error-código
</dt> <dd>

Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del servidor. Incluya este encabezado solo si Reason-Code no es 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-error-contexto
</dt> <dd>

Reemplace error-context por un número hexadecimal que representa el contexto en el que se produjo el error. Especifique el número hexadecimal del [**\_ \_ \_ \_ archivo remoto de contexto de error de BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0X5) si el servidor ha generado el error. En caso contrario, especifique el número hexadecimal de la **\_ \_ \_ \_ aplicación remota de contexto de error de BG** (0X7) si el error fue generado por la aplicación a la que se pasa el archivo de carga. Incluya este encabezado solo si el código de motivo no es 200 o 201.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 




