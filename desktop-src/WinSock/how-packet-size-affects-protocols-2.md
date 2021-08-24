---
description: Los problemas de tamaño de paquetes multimedia que se deban tratar en el tema Acerca del tamaño del paquete multimedia afectan de manera diferente a los \_ distintos protocolos IPX PF.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Cómo afecta el tamaño del paquete a los protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa654e8884f56ae8079375fa32764ad240f0c870229d07e50623f6e18e42958b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051643"
---
# <a name="how-packet-size-affects-protocols"></a>Cómo afecta el tamaño del paquete a los protocolos

Los problemas de tamaño de paquetes multimedia que se deban tratar en el tema Acerca del tamaño de paquete [multimedia](about-media-packet-size-2.md)afectan a los \_ distintos protocolos IPX PF de forma diferente. Una estrategia común para controlar varias restricciones de tamaño de enrutador y multimedia es usar el tamaño de medio completo cuando el número de red de la estación remota coincida con la estación local y volver al tamaño mínimo del paquete en caso contrario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>IPX de NSPROTO \_
</dt> <dd>

Proporciona un servicio de datagramas; cada datagrama debe residir dentro del tamaño máximo del paquete. Winsock establece el tamaño máximo del paquete del datagrama en el tamaño del paquete multimedia local menos el encabezado IPX. Sin embargo, tenga en cuenta que si el paquete se enruta, puede alcanzar las restricciones del enrutador en ruta. Asegúrese de que la aplicación puede volver a los datagramas de 546 bytes.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX
</dt> <dd>

Proporciona servicios de secuencia y paquetes secuenciados. Winsock IPX/SPX permite que los flujos de datos y los mensajes [**abarquen**](/windows/desktop/api/Winsock2/nf-winsock2-send) varios paquetes, por lo que el tamaño del paquete no limita la cantidad de datos que administra send [**y recv.**](/windows/desktop/api/winsock/nf-winsock-recv) Sin embargo, el tamaño del medio subyacente debe establecerse correctamente o el primer paquete grande no se podrá entregar y se restablecerá la conexión. Si la estación de destino está en la red local, Winsock establece su tamaño de paquete en el tamaño del paquete multimedia. De lo contrario, el valor predeterminado es 512 bytes. Este tamaño se puede cambiar inmediatamente después de [**conectarse**](/windows/desktop/api/Winsock2/nf-winsock2-connect) [**o aceptar a**](/windows/desktop/api/Winsock2/nf-winsock2-accept) través de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII
</dt> <dd>

SPXII ofrece una negociación de paquetes de Internet de gran tamaño para mantener el tamaño más adecuado para los paquetes y no requiere la intervención del programador. Sin embargo, si la estación remota no admite SPXII y negocia hasta el SPX estándar, las reglas de SPX de NSPROTO están \_ en vigor.



| Protocolo     | Medios      | Tipo        | Tamaño del paquete de datos |
|--------------|------------|-------------|------------------|
| IPX de NSPROTO \_ | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | Snap        |                  |
|              | Token Ring | 4 megabits   |                  |
|              |            | 16 megabits  |                  |
| NSPROTO \_ SPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | Snap        |                  |
|              | Token Ring | 4 megabits   |                  |
|              |            | 16 megabits  |                  |



 

</dd> </dl>

 

 



