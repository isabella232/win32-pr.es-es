---
title: Fragmento
description: Use el paquete Fragment para enviar un fragmento del archivo de carga al servidor.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- Bits de fragmento
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613acaabc017b9e673d2cba6a64f84db054a4cdc0d73a0639fcf8455edff8298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528835"
---
# <a name="fragment"></a>Fragmento

Use el **paquete Fragment** para enviar un fragmento del archivo de carga al servidor.

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

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo específico de BITS que identifica este paquete en el servidor BITS.

Reemplace remote-URL por el URI absoluto o relativo. Normalmente, reemplace remote-URL por el nombre de archivo remoto del trabajo. Para ver las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-Host-Id en el [**paquete Create-Session.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica este paquete de solicitud como un paquete de fragmentos.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadena que identifica la sesión en el servidor. Reemplace {guid} por el identificador de sesión que devuelve el servidor en el paquete [**de respuesta Ack for Create-Session.**](ack-for-create-session.md)

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name
</dt> <dd>

Especifique este encabezado solo con el fragmento inicial. Reemplace filename por el nombre del archivo local del trabajo. El nombre no incluye la ruta de acceso.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud del contenido
</dt> <dd>

Reemplace length por el número de bytes enviados en el cuerpo del fragmento.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Intervalo de contenido
</dt> <dd>

Indica al servidor dónde aplicar el intervalo en el archivo de destino. Reemplace range por los desplazamientos inicial y final del intervalo en el archivo de destino. Los desplazamientos son de base cero. Si el intervalo especificado se superpone a un intervalo existente, BITS solo escribe la parte no superpuesta del intervalo; BITS no sobrescribe el contenido existente. Por ejemplo, si el primer paquete contenía el intervalo de 0 a 100 y el segundo paquete contenía el intervalo de 50 a 150, BITS escribe solo bytes de 101 a 150 desde el segundo paquete. Reemplace la longitud total por el número total de bytes del archivo.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codificación de contenido
</dt> <dd>

Reemplace la codificación por el tipo de codificación que el cliente usa en el fragmento. El cliente debe usar la codificación que el servidor identifica en el Accept-Encoding encabezado del paquete de respuesta [**de Ack for Create-Session.**](ack-for-create-session.md) El servidor usa el tipo de codificación para descodificar el fragmento. Todos los fragmentos deben especificar la misma codificación.

No envíe este encabezado si el tipo de codificación es Identity. El servidor BITS solo admite la codificación de identidad.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El fragmento es un intervalo de bytes enviados en el cuerpo del paquete. El cliente envía los fragmentos en orden secuencial a partir del desplazamiento cero; el servidor no realiza un seguimiento de los intervalos no contiguos. Si el cliente envía intervalos no contiguos, el servidor devuelve un código de retorno HTTP 416 (intervalo no satisfiable) en la respuesta [**de Ack for Fragment.**](ack-for-fragment.md)

Los encabezados Content-*xxxx* son encabezados HTTP 1.1 estándar. Para más información sobre los encabezados Content-*xxxx,* consulte la [especificación RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ack for Fragment**](ack-for-fragment.md)
</dt> <dt>

[**Cerrar sesión**](close-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




