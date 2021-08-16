---
title: Cancel-Session
description: Use el Cancel-Session paquete para finalizar la sesión de carga con el servidor BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session BITS
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d570a49d1a5ba632fbbb453b6397338af70d29b0dc837db12193d2889c867eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835114"
---
# <a name="cancel-session"></a>Cancel-Session

Use el **paquete Cancel-Session** para finalizar la sesión de carga con el servidor BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
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

Identifica este paquete de solicitud como un Cancel-Session paquete.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadena que identifica la sesión en el servidor. Reemplace {guid} por el identificador de sesión que devuelve el servidor en el paquete [**de respuesta Ack for Create-Session.**](ack-for-create-session.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este paquete cancela un trabajo de carga si se envía antes de que se envíe el último fragmento. Cancel-Session no tiene ningún efecto en un archivo cuyo último fragmento ya se ha enviado. Cuando el servidor BITS recibe el último fragmento, escribe el archivo en su destino final y, en el caso de una respuesta de carga, envía el archivo a la aplicación de servidor. En el caso de upload-reply, el paquete Cancel-Session cancela la parte de respuesta de un trabajo upload-reply.

El servidor BITS libera todos los recursos y elimina todos los archivos temporales cuando recibe este paquete.

El cliente bits envía este paquete cuando el usuario cancela el trabajo.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Ack for Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Cerrar sesión**](close-session.md)
</dt> </dl>

 

 




