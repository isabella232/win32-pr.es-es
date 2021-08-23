---
title: Close-Session
description: Use el Close-Session para decir al servidor BITS que la carga de archivos se ha completado y para finalizar la sesión.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ae1318a99e690b13f4f0cad03624fb351c359efbcb1be9e105076ce53ceba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021203"
---
# <a name="close-session"></a>Close-Session

Use el **paquete Cerrar sesión** para decir al servidor BITS que la carga de archivos se ha completado y finalizar la sesión.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo específico de BITS que identifica este paquete en el servidor BITS.

Reemplace remote-URL por el URI absoluto o relativo. Normalmente, reemplace remote-URL por el nombre de archivo remoto del trabajo. Para ver las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-Host-Id en el [**paquete Create-Session.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica este paquete de solicitud como un Close-Session paquete.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadena que identifica la sesión en el servidor. Reemplace {guid} por el identificador de sesión que devuelve el servidor en el paquete [**de respuesta Ack for Create-Session.**](ack-for-create-session.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

El servidor BITS libera todos los recursos y elimina todos los archivos temporales cuando recibe este paquete.

Para los trabajos de carga y respuesta, debe descargar la respuesta antes de enviar **Close-Session**. De lo contrario, se pierde la respuesta.

Si envía este paquete antes de cargar todos los fragmentos, se elimina el archivo de carga. no puede cargar un archivo parcial.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ack for Close-Session**](ack-for-close-session.md)
</dt> <dt>

[**Cancel-Session**](cancel-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




