---
title: Cancelación de la retransmisión
description: Si no hay ninguna respuesta a una solicitud de comunicación dentro del período de tiempo de espera especificado para una entidad de destino y si se especifican retransmisiones para la entidad, la implementación de Microsoft WinSNMP retransmite la solicitud.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80770fc741357255adaa8b6bd15ab0e03b9148c37abf5fc631155d74b6d1f3a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009763"
---
# <a name="canceling-retransmission"></a>Cancelación de la retransmisión

Si no hay ninguna respuesta a una solicitud de comunicación dentro del período de tiempo de espera especificado para una entidad de destino y si se especifican retransmisiones para la entidad, la implementación de Microsoft WinSNMP retransmite la solicitud. Una llamada a la [**función SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) puede cancelar este ciclo de retransmisión y liberar estructuras de datos internas asociadas a la solicitud de mensaje.

Tenga en cuenta que es posible que una entidad de destino reciba un mensaje SNMP cancelado por una llamada a la [**función SnmpCancelMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) También es posible que una entidad de destino pueda responder a un mensaje SNMP cancelado. Esto se debe a que la cola de transacciones se produce en varios niveles. Sin embargo, una vez que una llamada a [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)canceló un mensaje, la implementación de Microsoft WinSNMP no retransmitirá el mensaje, enviará una PDU de respuesta ni enviará una notificación de tiempo de espera a la aplicación para ese mensaje.

 

 




