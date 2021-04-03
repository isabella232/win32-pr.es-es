---
title: Cancelando retransmisión
description: Si no hay ninguna respuesta a una solicitud de comunicación en el período de tiempo de espera especificado para una entidad de destino, y si se especifican retransmisiones para la entidad, la implementación de Microsoft WinSNMP vuelve a transmitir la solicitud.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075716"
---
# <a name="canceling-retransmission"></a>Cancelando retransmisión

Si no hay ninguna respuesta a una solicitud de comunicación en el período de tiempo de espera especificado para una entidad de destino, y si se especifican retransmisiones para la entidad, la implementación de Microsoft WinSNMP vuelve a transmitir la solicitud. Una llamada a la función [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) puede cancelar este ciclo de retransmisión y liberar las estructuras de datos internas asociadas a la solicitud de mensaje.

Tenga en cuenta que es posible que una entidad de destino reciba un mensaje SNMP cancelado por una llamada a la función [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) . También es posible que una entidad de destino pueda responder a un mensaje SNMP cancelado. Esto se debe a que las colas de transacciones se producen en varios niveles. Sin embargo, una vez que se ha cancelado un mensaje mediante una llamada a [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), la implementación de Microsoft WinSNMP no volverá a transmitir el mensaje, enviará una PDU de respuesta o enviará una notificación de tiempo de espera a la aplicación para ese mensaje.

 

 




