---
title: Validación de una PDU
description: Cuando la aplicación WinSNMP llama a la función SnmpSendMsg o a la función SnmpEncodeMsg, la implementación de Microsoft WinSNMP comprueba la validez de la PDU y los demás parámetros de función.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420fe01fac150bbebf39e494844bf2797ce0edc73d9339e0148c54faceebe8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885645"
---
# <a name="validating-a-pdu"></a>Validación de una PDU

Cuando la aplicación WinSNMP llama a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o a la [**función SnmpEncodeMsg,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) la implementación de Microsoft WinSNMP comprueba la validez de la PDU y los demás parámetros de función.

El valor de un componente de datos PDU (o campo) puede ser válido individualmente, pero puede no ser válido en combinación con los valores de otros campos. Por ejemplo, a menos que el campo **tipo PDU \_** de la PDU sea SNMP \_ PDU GETBULK o SNMP \_ \_ PDU RESPONSE, \_ **\_** **\_** tanto el estado de error como los campos de índice de errores deben ser iguales a cero. Cualquier otra combinación de valores constituye una PDU no válida.

La implementación rechaza las PDU no válidas y devuelve el estado de error SNMPAPI \_ FAILURE. Establece un código de error extendido igual a SNMPAPI \_ PDU \_ INVALID.

 

 




