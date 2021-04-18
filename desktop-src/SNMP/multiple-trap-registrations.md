---
title: Registros de captura múltiple
description: Hay varias opciones disponibles cuando una aplicación WinSNMP registra una sesión WinSNMP para capturas o notificaciones.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81aebf94d60ca26f39bcd53b26cb1f794f43af0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357442"
---
# <a name="multiple-trap-registrations"></a>Registros de captura múltiple

Hay varias opciones disponibles cuando una aplicación WinSNMP registra una sesión WinSNMP para capturas o notificaciones. Por este motivo, una aplicación puede llamar varias veces a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) , con lo que se define un filtro personalizado para la recepción de capturas y notificaciones. Por ejemplo, puede registrarse para un tipo de captura o notificación, o para todas las capturas y notificaciones, en función del valor del parámetro de *notificación* . Además, la aplicación puede especificar valores en otros parámetros para la función **SnmpRegister** con el fin de definir con mayor precisión las capturas y notificaciones que deben llegar a una aplicación. Para obtener más información, consulte [Administración de capturas y notificaciones](managing-traps-and-notifications.md).

A continuación se indican las instancias en las que varias llamadas a **SnmpRegister** son redundantes. En estos casos, **SnmpRegister** devuelve snmpapi \_ Success si la función se completa correctamente, pero el registro redundante es ineficaz.

1.  Una llamada a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) que solicita la entrega filtrada de capturas y notificaciones a la sesión, después de una llamada anterior a **SnmpRegister** que solicita la entrega de todas las capturas y notificaciones (entrega sin filtrar). Esta llamada es redundante porque la sesión ya está recibiendo todas las capturas y notificaciones, incluido el tipo único definido por el filtro.
2.  Una llamada duplicada a **SnmpRegister** o una en la que la lista de parámetros es idéntica a la lista de parámetros de una llamada anterior a **SnmpRegister** para la sesión.
3.  Una llamada a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) que solicita la entrega filtrada de capturas y notificaciones basadas en un identificador de objeto (OID) cuyo prefijo es un OID especificado en una llamada anterior a **SnmpRegister**. Por ejemplo, puede especificar "1.3.6.1.4.1.311" en el parámetro *Notification* para recibir notificaciones procedentes de cualquier entidad del agente SNMP de Microsoft. Si llama de nuevo a **SnmpRegister** y especifica "1.3.6.1.4.1.311.1", la segunda llamada es redundante porque la sesión ya está recibiendo todas las capturas y notificaciones que contienen el prefijo OID "1.3.6.1.4.1.311".

Para anular el registro de la sesión, debe hacer coincidir cada llamada de registro única con la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) . Llame a **SnmpRegister** para anular el registro de la sesión y asegúrese de que los cinco primeros parámetros de **SnmpRegister** son idénticos a los de la llamada de registro inicial. La única diferencia entre la llamada inicial y la anulación del registro es que al registrarse debe especificar el valor SNMPAPI en \_ el parámetro *status* y, al llamar a la función para anular el registro, debe especificar snmpapi \_ OFF. No es necesario que coincidan las llamadas de registro redundantes a la función **SnmpRegister** . Solo es necesario que coincida con la primera llamada de registro única.

Para cambiar los criterios de filtrado, puede ser necesario que una aplicación elimine primero del registro y deshabilite la entrega de ciertas notificaciones o notificaciones. A continuación, la aplicación puede crear un filtro nuevo llamando a [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), pasando los valores adecuados.

 

 




