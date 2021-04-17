---
title: Cancel-Session
description: Use el paquete de Cancel-Session para finalizar la sesión de carga con el servidor BITS.
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
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105656297"
---
# <a name="cancel-session"></a>Cancel-Session

Use el paquete **de cancelación de sesión** para finalizar la sesión de carga con el servidor bits.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
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

Identifica este paquete de solicitud como un paquete de Cancel-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS
</dt> <dd>

GUID de cadena que identifica la sesión en el servidor. Reemplace {GUID} por el identificador de sesión que devuelve el servidor en el paquete de respuesta [**de confirmación para creación de sesión**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este paquete cancela un trabajo de carga si se envía antes de que se envíe el último fragmento. Cancel-Session no tiene ningún efecto en un archivo cuyo último fragmento ya se ha enviado. Cuando el servidor BITS recibe el último fragmento, escribe el archivo en su destino final y, en el caso de una respuesta de carga, envía el archivo a la aplicación de servidor. En el caso de la respuesta de carga, el paquete de Cancel-Session cancela la parte de respuesta de un trabajo de carga y respuesta.

El servidor BITS libera todos los recursos y elimina todos los archivos temporales cuando recibe este paquete.

El cliente de BITS envía este paquete cuando el usuario cancela el trabajo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Confirmación de creación: sesión**](ack-for-create-session.md)
</dt> <dt>

[**Sesión de cierre**](close-session.md)
</dt> </dl>

 

 




