---
title: Create-Session
description: Use el paquete de Create-Session para solicitar una sesión de carga con el servidor BITS.
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
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487091"
---
# <a name="create-session"></a>Create-Session

Use el paquete **de creación de sesión** para solicitar una sesión de carga con el servidor bits.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_post bits
</dt> <dd>

Verbo específico de BITS que identifica este paquete en el servidor BITS.

Reemplace Remote-URL por el URI absoluto o relativo. Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo. Para conocer las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-host-ID.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo
</dt> <dd>

Identifica este paquete de solicitud como un paquete de Create-Session.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS: protocolos admitidos
</dt> <dd>

Lista delimitada por espacios de los protocolos que admite el cliente. Use GUID de cadena para identificar los protocolos. Especifique la lista en orden de preferencia de más a menos preferida. En la tabla siguiente se muestra el protocolo que admite el cliente BITS. Reemplace {guid1}... {guidn} con uno o más GUID de cadena de la lista.



| Protocolo                                          | Descripción                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | Protocolo de carga de BITS 1,5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe enviar un paquete [**ping**](ping.md) para establecer una conexión http antes de enviar el paquete de Create-Session. El paquete de Create-Session también puede establecer la conexión; sin embargo, el paquete de Create-Session es menos eficaz.

El servidor selecciona el protocolo que desea utilizar en la lista que el cliente proporciona en el encabezado BITS-compatible-protocolos. El servidor devuelve el protocolo seleccionado en el encabezado BITS-Protocol del paquete de respuesta de [**confirmación de creación de sesión**](ack-for-create-session.md) .

El cliente espera que el servidor devuelva una [**confirmación para el paquete de respuesta de la sesión de creación**](ack-for-create-session.md) . Si el servidor ha podido establecer una sesión, el cliente utiliza el paquete de solicitud de [**fragmento**](fragment.md) para enviar intervalos del archivo al servidor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Confirmación de creación: sesión**](ack-for-create-session.md)
</dt> <dt>

[**Fragmento**](fragment.md)
</dt> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 





