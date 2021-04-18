---
description: Los problemas de tamaño de los paquetes multimedia descritos en el tema sobre el tamaño de los paquetes multimedia afectan a los distintos protocolos de PF \_ IPX de manera diferente.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Cómo afecta el tamaño de paquete a los protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360300"
---
# <a name="how-packet-size-affects-protocols"></a>Cómo afecta el tamaño de paquete a los protocolos

Los problemas de tamaño de los paquetes multimedia descritos en el tema sobre el tamaño de los [paquetes multimedia](about-media-packet-size-2.md)afectan a los distintos protocolos de PF \_ IPX de manera diferente. Una estrategia común para controlar varias restricciones de tamaño de enrutador y de tamaño de los medios es usar el tamaño total del medio cuando el número de red de la estación remota coincide con la estación local y revertir al tamaño mínimo de los paquetes en caso contrario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX
</dt> <dd>

Proporciona un servicio de datagramas; cada datagrama debe residir en el tamaño máximo del paquete. Winsock establece el tamaño máximo del paquete de datagramas en el tamaño de paquete multimedia local menos el encabezado IPX. Sin embargo, tenga en cuenta que si se enruta el paquete, puede que se alcancen las restricciones de enrutador en la ruta. Asegúrese de que la aplicación puede revertir a datagramas de 546 bytes.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX
</dt> <dd>

Proporciona servicios de secuencia y de paquetes secuenciados. Winsock IPX/SPX permite que los flujos de datos y los mensajes abarquen varios paquetes, por lo que el tamaño de los paquetes no limita la cantidad de datos que se administran mediante el [**envío**](/windows/desktop/api/Winsock2/nf-winsock2-send) y la [**recepción**](/windows/desktop/api/winsock/nf-winsock-recv). Sin embargo, el tamaño del medio subyacente debe establecerse correctamente o el primer paquete de gran tamaño no se podrá enviar y se restablecerá la conexión. Si la estación de destino se encuentra en la red local, Winsock establece el tamaño de paquete en el tamaño de paquete multimedia. De lo contrario, el valor predeterminado es 512 bytes. Este tamaño se puede cambiar inmediatamente después de la [**conexión**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o de [**Aceptar**](/windows/desktop/api/Winsock2/nf-winsock2-accept) [**a la**](/windows/desktop/api/winsock/nf-winsock-setsockopt).

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII
</dt> <dd>

SPXII incluye una gran negociación de paquetes de Internet para mantener un tamaño mejor para los paquetes y no requiere la intervención del programador. Sin embargo, si la estación remota no es compatible con SPXII y se negocia a la SPX estándar, las \_ reglas de NSPROTO SPX estarán en vigor.



| Protocolo     | Medios      | Tipo        | Tamaño de paquete de datos |
|--------------|------------|-------------|------------------|
| NSPROTO \_ IPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | COMPLEMENTO        |                  |
|              | Token Ring | 4 megabits   |                  |
|              |            | 16 megabits  |                  |
| NSPROTO \_ SPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | COMPLEMENTO        |                  |
|              | Token Ring | 4 megabits   |                  |
|              |            | 16 megabits  |                  |



 

</dd> </dl>

 

 



