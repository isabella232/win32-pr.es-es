---
title: Confirmación para Create-Session
description: Use la confirmación de Create-Session paquete para confirmar la solicitud de Create-Session del cliente.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Confirmación de Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "105656435"
---
# <a name="ack-for-create-session"></a>Confirmación para Create-Session

Use el paquete **de confirmación para creación de sesión** para confirmar la solicitud de [**creación de sesión**](create-session.md) del cliente.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo
</dt> <dd>

Reemplace Reason-Code por el código de motivo HTTP. En la tabla siguiente se muestran los códigos de motivo típicos para una respuesta a una solicitud [**de creación de sesión**](create-session.md) . Para obtener una lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Código del motivo    | Descripción                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | Aceptar. La solicitud fue correcta.<br/>                                          |
| 201<br/> | Creado. Se creó la sesión.<br/>                                        |
| 403<br/> | Prohibido. No se permite al usuario cargar archivos en la dirección URL especificada.<br/> |
| 404<br/> | Not Found. La dirección URL especificada no existe.<br/>                             |
| 409<br/> | Conflicto. El archivo existe en el servidor y no se puede sobrescribir.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>razón: Descripción
</dt> <dd>

Reemplace Reason-Description por la descripción de HTTP asociada al código de motivo. Por ejemplo, establezca Reason-Description en OK si Reason-Code es 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo
</dt> <dd>

Identifica este paquete de respuesta como un paquete de confirmación.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>Protocolo BITS
</dt> <dd>

GUID de cadena que identifica el protocolo que el servidor desea usar para esta sesión. Reemplace {GUID} por el identificador de protocolo de la lista de protocolos que el cliente incluye en la solicitud de [**creación de sesión**](create-session.md) ; el encabezado BITS compatible-protocolo contiene la lista. Incluya este encabezado solo si el código de motivo es 200 o 201.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS
</dt> <dd>

GUID de cadena que identifica esta sesión en el cliente. Reemplace {GUID} por el identificador de sesión que el cliente envía en todos los paquetes de solicitud posteriores.

BITS usa un GUID para identificar la sesión, pero puede usar cualquier cadena HTTP-legal de hasta 100 caracteres.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-identificador de host
</dt> <dd>

Opcional. Incluya este encabezado solo si se ha establecido la [propiedad de extensión de IIS de bits](bits-iis-extension-properties.md), BITSHostId. Reemplace PublicHostName por el nombre del servidor o la dirección IP de la propiedad BITSHostId.

El cliente debe reemplazar la parte del servidor de la dirección URL remota en todos los paquetes posteriores. Si el cliente no especifica este nombre de host en los paquetes posteriores, es posible que el trabajo se inicie de nuevo en otro servidor de la granja, lo que deja un archivo de carga parcial en el servidor anterior.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-host-ID-reserva-timeout
</dt> <dd>

Opcional. Incluya este encabezado solo si se especifica el encabezado BITS-host-ID. Reemplace timeout por el valor de tiempo de espera de la propiedad BITSHostIdFallbackTimeout. La propiedad BITSHostIdFallbackTimeout es una de las [propiedades de extensión de IIS de bits](bits-iis-extension-properties.md).

El cliente utiliza el período de tiempo de espera para determinar cuánto tiempo intenta volver a conectarse al nombre de servidor especificado en el encabezado BITS-host-ID antes de revertir al nombre de host especificado en el nombre de archivo remoto del trabajo. El temporizador comienza cuando BITS no puede conectarse al servidor BITS-host-ID. El temporizador se restablece cuando se restaura una conexión al servidor. Si no se especifica un período de tiempo de espera, el cliente nunca revierte al nombre de host especificado en el nombre de archivo remoto.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Aceptar: codificación
</dt> <dd>

Identifica el esquema de codificación que se va a utilizar en los fragmentos enviados al servidor. El paquete de fragmento contiene el fragmento codificado en el cuerpo del paquete. El servidor BITS requiere codificación de identidad (texto sin formato). Incluya este encabezado solo si el código de motivo es 200 o 201.

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

[**Crear sesión**](create-session.md)
</dt> </dl>

 

 





