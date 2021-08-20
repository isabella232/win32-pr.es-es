---
title: Create-Session
description: Use el paquete Create-Session para solicitar una sesión de carga con el servidor BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639db08c5a29b09f5c32d7b0243de66f2c4dced001a1ff2afa7e74837c8d67e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021193"
---
# <a name="create-session"></a>Create-Session

Use el **paquete Create-Session** para solicitar una sesión de carga con el servidor BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo específico de BITS que identifica este paquete al servidor BITS.

Reemplace remote-URL por el URI absoluto o relativo. Normalmente, reemplace remote-URL por el nombre de archivo remoto del trabajo. Para ver las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-Host-Id.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica este paquete de solicitud como Create-Session paquete.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>Protocolos compatibles con BITS
</dt> <dd>

Lista delimitada por espacios de los protocolos que admite el cliente. Use GUID de cadena para identificar los protocolos. Especifique la lista en orden de preferencia de más a menos preferida. En la tabla siguiente se muestra el protocolo que admite el cliente bits. Reemplace {guid1} ... {guidN} con uno o varios GUID de cadena de la lista.



| Protocolo                                          | Descripción                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | Protocolo de Upload BITS 1.5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe enviar un paquete [**Ping**](ping.md) para establecer una conexión HTTP antes de enviar el Create-Session paquete. El Create-Session paquete también puede establecer la conexión; sin embargo, el Create-Session paquete es menos eficaz.

El servidor selecciona el protocolo que quiere usar en la lista que proporciona el cliente en el encabezado BITS-Supported-Protocols. El servidor devuelve el protocolo seleccionado en el BITS-Protocol encabezado del paquete de respuesta [**Ack for Create-Session.**](ack-for-create-session.md)

El cliente espera que el servidor devuelva un [**paquete de respuesta Deck for Create-Session.**](ack-for-create-session.md) Si el servidor pudo establecer una sesión, el cliente usa el paquete de solicitud [**Fragment**](fragment.md) para enviar intervalos del archivo al servidor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ack for Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Fragmento**](fragment.md)
</dt> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 





