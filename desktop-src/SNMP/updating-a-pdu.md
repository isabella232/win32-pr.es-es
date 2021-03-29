---
title: Actualización de una PDU
description: Una aplicación WinSNMP puede recuperar y actualizar los campos de PDU seleccionados mediante las funciones SnmpGetPduData y SnmpSetPduData.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778871"
---
# <a name="updating-a-pdu"></a>Actualización de una PDU

Una aplicación WinSNMP puede recuperar y actualizar los campos de PDU seleccionados mediante las funciones [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) y [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

La aplicación puede recuperar el tipo de PDU, el identificador de la solicitud, el estado de error y los campos de índice de error de una PDU específica. También puede recuperar el identificador de la lista de enlaces de variables. La aplicación puede actualizar los **campos \_ tipo de PDU** y **\_ ID** . de solicitud.

Si el tipo de PDU es igual a la PDU de SNMP \_ \_ GetBulk e inform, la aplicación también puede actualizar los campos **que no son de \_ repetición** y **máximo de \_ repeticiones** de la PDU.

 

 




