---
title: Confirmación para fragmento
description: Use la confirmación para que el paquete de fragmentos confirme la solicitud de fragmento del cliente.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- Confirmación para BITS de fragmento
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103995721"
---
# <a name="ack-for-fragment"></a>Confirmación para fragmento

Use la **confirmación para** que el paquete de fragmentos confirme la solicitud de [**fragmento**](fragment.md) del cliente.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo
</dt> <dd>

Reemplace Reason-Code por un código de motivo HTTP. En la tabla siguiente se muestran los códigos de motivo típicos para una respuesta a una solicitud de [**fragmento**](fragment.md) . Para obtener una lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Código del motivo    | Descripción                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | Aceptar. La solicitud fue correcta.<br/>                                                                             |
| 416<br/> | Range: no-se puede satisfacer. El cliente envió un fragmento cuyo intervalo no es contiguo con el fragmento anterior.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>razón: Descripción
</dt> <dd>

Reemplace Reason-Description por la descripción de HTTP asociada al código de motivo. Por ejemplo, establezca Reason-Description en OK si Reason-Code es 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo
</dt> <dd>

Identifica este paquete de respuesta como un paquete de confirmación.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-recibido-contenido-intervalo
</dt> <dd>

Desplazamiento de base cero al siguiente byte que el servidor espera que el cliente envíe. Por ejemplo, si el fragmento contenía el intervalo 128 212, debe establecer intervalo en 213.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS
</dt> <dd>

GUID de cadena que identifica la sesión en el cliente. Reemplace {GUID} por el identificador de sesión que el cliente envió en el paquete de solicitud de [**fragmento**](fragment.md) . Si no reconoce el identificador de sesión, establezca el encabezado BITS-error-código en la sesión de \_ BG \_ E \_ no \_ encontrada.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>Dirección URL de BITS-respuesta
</dt> <dd>

Contiene la dirección URL de los datos de respuesta de un trabajo de carga y respuesta. Incluya este encabezado en la respuesta de fragmento final una vez completada la carga y reciba una respuesta de la aplicación de servidor, si procede.

Use el encabezado Content-Range de la solicitud de fragmento para determinar si la carga se ha completado. La carga se completa si el desplazamiento final del valor del intervalo es igual al valor de longitud total menos uno.

El servidor BITS envía el archivo de carga a la aplicación de servidor una vez que determina que la carga se ha completado. La aplicación de servidor procesa el archivo y genera la respuesta. El servidor BITS establece el valor de BITS-reply-URL en la dirección URL del archivo de respuesta de la aplicación de servidor.

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

Si la sesión es para un trabajo de carga y respuesta, puede haber un retraso antes de que el cliente reciba la confirmación final de la respuesta **de fragmento** . La duración del retraso depende de la cantidad de tiempo que la aplicación de servidor (la aplicación a la que el servidor envía el archivo de carga) tarda en generar la respuesta.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Crear sesión**](create-session.md)
</dt> <dt>

[**Fragmento**](fragment.md)
</dt> </dl>

 

 





