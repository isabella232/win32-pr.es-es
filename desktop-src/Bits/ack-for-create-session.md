---
title: Ack for Create-Session
description: Use la confirmación para Create-Session paquete para confirmar la solicitud de Create-Session cliente.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Ack for Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dbfcaeab897d55064fe11a506cefbc9d85dd6852a32d279133e6fe7a33a692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588805"
---
# <a name="ack-for-create-session"></a>Ack for Create-Session

Use el **paquete Ack for Create-Session** para confirmar la solicitud [**Create-Session del**](create-session.md) cliente.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Reemplace reason-code por el código de motivo HTTP. En la tabla siguiente se muestran los códigos de motivo típicos para una respuesta a una [**solicitud Create-Session.**](create-session.md) Para obtener una lista de códigos de motivo HTTP, [vea RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Código del motivo    | Descripción                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | Aceptar. La solicitud fue correcta.<br/>                                          |
| 201<br/> | Creado. Se creó la sesión.<br/>                                        |
| 403<br/> | Prohibido. El usuario no puede cargar archivos en la dirección URL especificada.<br/> |
| 404<br/> | Not Found. La dirección URL especificada no existe.<br/>                             |
| 409<br/> | Conflicto. El archivo existe en el servidor y no se puede sobrescribir.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Reemplace reason-description por la descripción HTTP asociada al código de motivo. Por ejemplo, establezca reason-description en Ok si reason-code es 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica este paquete de respuesta como un paquete Deck.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>Protocolo BITS
</dt> <dd>

GUID de cadena que identifica el protocolo que el servidor quiere usar para esta sesión. Reemplace {guid} por el identificador de protocolo de la lista de protocolos que el cliente incluye en la [**solicitud Create-Session;**](create-session.md) El encabezado BITS-Supported-Protocol contiene la lista. Incluya este encabezado solo si el código de motivo es 200 o 201.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadena que identifica esta sesión al cliente. Reemplace {guid} por el identificador de sesión que el cliente envía en todos los paquetes de solicitud posteriores.

BITS usa un GUID para identificar la sesión, pero puede usar cualquier cadena http legal de hasta 100 caracteres.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id
</dt> <dd>

Opcional. Incluya este encabezado solo si se establece la propiedad [de extensión IIS bits,](bits-iis-extension-properties.md)BITSHostId. Reemplace PublicHostName por el nombre del servidor o la dirección IP de la propiedad BITSHostId.

El cliente debe reemplazar la parte del servidor de la dirección URL remota en todos los paquetes posteriores. Si el cliente no especifica este nombre de host en paquetes posteriores, es posible que el trabajo se inicie de nuevo en otro servidor de la granja, dejando un archivo de carga parcial en el servidor anterior.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout
</dt> <dd>

Opcional. Incluya este encabezado solo si se especifica el encabezado BITS-Host-Id. Reemplace Timeout por el valor de tiempo de espera de la propiedad BITSHostIdFallbackTimeout. La propiedad BITSHostIdFallbackTimeout es una de las propiedades de [extensión de IIS de BITS](bits-iis-extension-properties.md).

El cliente usa el período de tiempo de espera para determinar cuánto tiempo intenta volver a conectarse al nombre de servidor especificado en el encabezado BITS-Host-Id antes de revertir al nombre de host especificado en el nombre de archivo remoto del trabajo. El temporizador comienza cuando BITS no puede conectarse al servidor BITS-Host-Id. El temporizador se restablece cuando se restaura una conexión al servidor. Si no se especifica un período de tiempo de espera, el cliente nunca vuelve al nombre de host especificado en el nombre de archivo remoto.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding
</dt> <dd>

Identifica el esquema de codificación que se usará en los fragmentos enviados al servidor. El paquete Fragment contiene el fragmento codificado en el cuerpo del paquete. El servidor BITS requiere codificación de identidad (texto no cifrado). Incluya este encabezado solo si reason-code es 200 o 201.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud del contenido
</dt> <dd>

Reemplace length por el número de bytes incluidos en el cuerpo de la respuesta. Obligatorio incluso si el cuerpo de la respuesta no incluye contenido.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Reemplace el código de error por un número hexadecimal que represente un valor HRESULT asociado a un error del lado servidor. Incluya este encabezado solo si reason-code no es 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Reemplace error-context por un número hexadecimal que represente el contexto en el que se produjo el error. Especifique el número hexadecimal para [**BG ERROR CONTEXT REMOTE \_ \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si el servidor generó el error. De lo contrario, especifique el número hexadecimal de **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) si el error lo generó la aplicación a la que se pasa el archivo de carga. Incluya este encabezado solo si el código de motivo no es 200 o 201.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 





