---
title: Fragmento
description: Use el paquete de fragmento para enviar al servidor un fragmento del archivo de carga.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- BITS de fragmento
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149094"
---
# <a name="fragment"></a>Fragmento

Use el paquete de **fragmento** para enviar al servidor un fragmento del archivo de carga.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
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

Identifica este paquete de solicitud como un paquete de fragmento.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS
</dt> <dd>

GUID de cadena que identifica la sesión en el servidor. Reemplace {GUID} por el identificador de sesión que devuelve el servidor en el paquete de respuesta [**de confirmación para creación de sesión**](ack-for-create-session.md) .

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Nombre de contenido
</dt> <dd>

Especifique este encabezado solo con el fragmento inicial. Reemplace FILENAME por el nombre del archivo local del trabajo. El nombre no incluye la ruta de acceso.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido
</dt> <dd>

Reemplace length por el número de bytes enviados en el cuerpo del fragmento.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range
</dt> <dd>

Indica al servidor dónde aplicar el intervalo en el archivo de destino. Reemplace Range con los desplazamientos inicial y final del intervalo del archivo de destino. Los desplazamientos son de base cero. Si el intervalo especificado se superpone a un intervalo existente, BITS solo escribe la parte no superpuesta del intervalo. BITS no sobrescribe el contenido existente. Por ejemplo, si el primer paquete contenía el intervalo comprendido entre 0 y 100 y el segundo paquete contenía el intervalo de 50 a 150, BITS escribe solo los bytes 101 a 150 del segundo paquete. Reemplace total-length por el número total de bytes del archivo.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codificación de contenido
</dt> <dd>

Reemplace la codificación con el tipo de codificación que el cliente usa en el fragmento. El cliente debe usar la codificación que el servidor identifica en el encabezado Accept-Encoding del paquete de respuesta de [**confirmación de creación de sesión**](ack-for-create-session.md) . El servidor usa el tipo de codificación para descodificar el fragmento. Todos los fragmentos deben especificar la misma codificación.

No envíe este encabezado si el tipo de codificación es Identity. El servidor BITS solo admite la codificación de identidad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El fragmento es un intervalo de bytes enviados en el cuerpo del paquete. El cliente envía los fragmentos en orden secuencial a partir del desplazamiento cero; el servidor no realiza un seguimiento de los intervalos no contiguos. Si el cliente envía intervalos no contiguos, el servidor devuelve un código de retorno HTTP 416 (intervalo no se puede satisfacer) en la [**confirmación para la respuesta de fragmento**](ack-for-fragment.md) .

Los encabezados Content-*xxxx* son encabezados HTTP 1,1 estándar. Para obtener más información sobre los encabezados Content-*xxxx* , vea la especificación [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Confirmación para fragmento**](ack-for-fragment.md)
</dt> <dt>

[**Sesión de cierre**](close-session.md)
</dt> <dt>

[**Crear sesión**](create-session.md)
</dt> </dl>

 

 




