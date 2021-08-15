---
title: Ping
description: Use el paquete Ping para establecer una conexión y negociar la seguridad con el servidor.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Ping BITS
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479e03e6e18c0ec7421bd225744c5181029fc2b2e220f35c7bae7a3b02d42b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004895"
---
# <a name="ping"></a>Ping

Use el **paquete Ping** para establecer una conexión y negociar la seguridad con el servidor.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo específico de BITS que identifica este paquete al servidor BITS.

Reemplace remote-URL por el URI absoluto o relativo. Normalmente, reemplace remote-URL por el nombre de archivo remoto del trabajo.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica este paquete de solicitud como un paquete Ping.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **paquete Ping** es opcional. En lugar de enviar un **paquete Ping,** puede usar [**el paquete Create-Session**](create-session.md) para establecer una conexión y negociar la seguridad. Sin embargo, es más eficaz usar el paquete **Ping** para este propósito.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Ack for Ping**](ack-for-ping.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




