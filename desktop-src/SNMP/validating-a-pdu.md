---
title: Validación de una PDU
description: Cuando la aplicación WinSNMP llama a la función SnmpSendMsg o a la función SnmpEncodeMsg, la implementación de Microsoft WinSNMP comprueba la validez de la PDU y los demás parámetros de función.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418980"
---
# <a name="validating-a-pdu"></a>Validación de una PDU

Cuando la aplicación WinSNMP llama a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o a la función [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , la implementación de Microsoft WinSNMP comprueba la validez de la PDU y los demás parámetros de función.

El valor de un componente de datos PDU (o campo) puede ser válido individualmente, pero puede no ser válido en combinación con los valores de otros campos. Por ejemplo, a menos que el campo de **\_ tipo de PDU** de la PDU sea \_ GetBulk e inform PDU de SNMP \_ o respuesta de PDU de SNMP \_ \_ , los campos de **\_ Estado de error** y de **\_ Índice de error** deben ser iguales a cero. Cualquier otra combinación de valores constituye una PDU no válida.

La implementación rechaza las PDU no válidas y devuelve el estado de error SNMPAPI \_ error. Establece un código de error extendido igual a SNMPAPI \_ PDU \_ no válido.

 

 




