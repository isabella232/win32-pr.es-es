---
title: Ping
description: Use el paquete ping para establecer una conexión y negociar la seguridad con el servidor.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Hacer ping de BITS
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "105656301"
---
# <a name="ping"></a>Ping

Use el paquete **ping** para establecer una conexión y negociar la seguridad con el servidor.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Encabezados

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_post bits
</dt> <dd>

Verbo específico de BITS que identifica este paquete en el servidor BITS.

Reemplace Remote-URL por el URI absoluto o relativo. Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo
</dt> <dd>

Identifica este paquete de solicitud como un paquete de ping.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El paquete **ping** es opcional. En lugar de enviar un paquete **ping** , puede usar el paquete [**de creación de sesión**](create-session.md) para establecer una conexión y negociar la seguridad. Sin embargo, es más eficaz usar el paquete **ping** con este fin.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Confirmación del ping**](ack-for-ping.md)
</dt> <dt>

[**Crear sesión**](create-session.md)
</dt> </dl>

 

 




