---
title: Close-Session
description: Use el paquete de Close-Session para indicar al servidor BITS que la carga de archivos se ha completado y para finalizar la sesión.
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
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103903966"
---
# <a name="close-session"></a>Close-Session

Use el paquete **de sesión de cierre** para indicar al servidor bits que la carga de archivos se ha completado y para finalizar la sesión.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_post bits
</dt> <dd>

Verbo específico de BITS que identifica este paquete en el servidor BITS.

Reemplace Remote-URL por el URI absoluto o relativo. Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo. Para conocer las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-host-ID en el paquete de [**creación de sesión**](create-session.md) .

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo
</dt> <dd>

Identifica este paquete de solicitud como un paquete de Close-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS
</dt> <dd>

GUID de cadena que identifica la sesión en el servidor. Reemplace {GUID} por el identificador de sesión que devuelve el servidor en el paquete de respuesta [**de confirmación para creación de sesión**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El servidor BITS libera todos los recursos y elimina todos los archivos temporales cuando recibe este paquete.

En el caso de los trabajos de carga y respuesta, debe descargar la respuesta antes de enviar la **sesión de cierre**. De lo contrario, se pierde la respuesta.

Si envía este paquete antes de cargar todos los fragmentos, se elimina el archivo de carga; no se puede cargar un archivo parcial.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Confirmación de cierre de sesión**](ack-for-close-session.md)
</dt> <dt>

[**Cancelar sesión**](cancel-session.md)
</dt> <dt>

[**Crear sesión**](create-session.md)
</dt> </dl>

 

 




