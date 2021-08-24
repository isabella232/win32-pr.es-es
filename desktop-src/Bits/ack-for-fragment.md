---
title: Ack for Fragment
description: Use el paquete Ack for Fragment para confirmar la solicitud de fragmento del cliente.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- Ack for Fragment BITS
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd4b8bf5580a5724c689ced1886051006d34cd3c9ba0561d253f36428178c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702125"
---
# <a name="ack-for-fragment"></a>Ack for Fragment

Use el **paquete Ack for Fragment para** confirmar la solicitud de fragmento [**del**](fragment.md) cliente.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Reemplace reason-code por un código de motivo HTTP. En la tabla siguiente se muestran los códigos de motivo típicos para una respuesta a una [**solicitud de fragmento.**](fragment.md) Para obtener una lista de códigos de motivo HTTP, [vea RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Código del motivo    | Descripción                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | Aceptar. La solicitud fue correcta.<br/>                                                                             |
| 416<br/> | Range-Not-Satisfiable. El cliente envió un fragmento cuyo intervalo no es contiguo al fragmento anterior.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Reemplace reason-description por la descripción HTTP asociada al código de motivo. Por ejemplo, establezca reason-description en Ok si reason-code es 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica este paquete de respuesta como un paquete Deck.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range
</dt> <dd>

Desplazamiento de base cero al byte siguiente que el servidor espera que envíe el cliente. Por ejemplo, si el fragmento contiene el intervalo 128 212, establecería el intervalo en 213.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadena que identifica la sesión al cliente. Reemplace {guid} por el identificador de sesión que el cliente envió en el [**paquete de solicitud fragment.**](fragment.md) Si no reconoce el identificador de sesión, establezca el encabezado BITS-Error-Code en BG \_ E \_ SESSION NOT \_ \_ FOUND.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL
</dt> <dd>

Contiene la dirección URL de los datos de respuesta de un trabajo de carga y respuesta. Incluya este encabezado en la respuesta del fragmento final una vez completada la carga y reciba una respuesta de la aplicación de servidor, si procede.

Use el encabezado Content-Range de la solicitud Fragment para determinar si la carga se ha completado. La carga se completa si el desplazamiento final del valor de intervalo es igual al valor de longitud total menos uno.

El servidor BITS envía el archivo de carga a la aplicación de servidor después de determinar que la carga se ha completado. La aplicación de servidor procesa el archivo y genera la respuesta. El servidor BITS establece el valor de BITS-Reply-URL en la dirección URL del archivo de respuesta de la aplicación de servidor.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud del contenido
</dt> <dd>

Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta. Se requiere content-length, incluso si el cuerpo de la respuesta no incluye contenido.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del lado servidor. Incluya solo este encabezado si reason-code no es 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Reemplace error-context por un número hexadecimal que represente el contexto en el que se produjo el error. Especifique el número hexadecimal para [**BG ERROR CONTEXT REMOTE \_ \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si el servidor generó el error. De lo contrario, especifique el número hexadecimal de **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) si el error lo generó la aplicación a la que se pasa el archivo de carga. Incluya este encabezado solo si el código de motivo no es 200 o 201.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si la sesión es para un trabajo de carga y respuesta, puede haber un retraso antes de que el cliente reciba la respuesta final **de Ack for Fragment.** La duración del retraso depende de la cantidad de tiempo que tarda la aplicación de servidor (aplicación a la que el servidor publica el archivo de carga) para generar la respuesta.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> <dt>

[**Fragmento**](fragment.md)
</dt> </dl>

 

 





