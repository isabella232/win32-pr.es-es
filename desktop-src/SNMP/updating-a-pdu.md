---
title: Actualización de una PDU
description: Una aplicación WinSNMP puede recuperar y actualizar los campos PDU seleccionados mediante las funciones SnmpGetPduData y SnmpSetPduData.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c876f22118841b2139086665aa2f39c4dd5395328a27e21cea35cf609698f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885695"
---
# <a name="updating-a-pdu"></a>Actualización de una PDU

Una aplicación WinSNMP puede recuperar y actualizar los campos PDU seleccionados mediante las funciones [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) y [**SnmpSetPduData.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)

La aplicación puede recuperar el tipo de PDU, el identificador de solicitud, el estado de error y los campos de índice de error de una PDU específica. También puede recuperar el identificador de la lista de enlaces de variables. La aplicación puede actualizar el tipo **de PDU \_ y** los **campos de identificador \_ de** solicitud.

Si el tipo PDU es igual a SNMP PDU GETBULK, la aplicación también puede actualizar los campos de repeticiones máximas y no repeticiones de \_ \_ la PDU. **\_** **\_**

 

 




