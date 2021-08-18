---
title: Varios registros de captura
description: Hay varias opciones disponibles cuando una aplicación WinSNMP registra una sesión de WinSNMP para capturas o notificaciones.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2149e4ac1e9880601ae64718cd78991718d54a6228488a03e593376d9a7937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009333"
---
# <a name="multiple-trap-registrations"></a>Varios registros de captura

Hay varias opciones disponibles cuando una aplicación WinSNMP registra una sesión de WinSNMP para capturas o notificaciones. Por este problema, una aplicación puede llamar a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) varias veces, definiendo de hecho un filtro personalizado para la recepción de capturas y notificaciones. Por ejemplo, puede registrarse para un tipo de captura o notificación, o para todas las capturas y notificaciones, dependiendo del valor del parámetro *de* notificación. Además, la aplicación puede especificar valores en otros parámetros para la función **SnmpRegister** para definir aún más las capturas y las notificaciones que deben llegar a una aplicación. Para obtener más información, vea [Administración de capturas y notificaciones.](managing-traps-and-notifications.md)

A continuación se encuentran instancias en las que varias llamadas **a SnmpRegister** son redundantes. En estos **casos, SnmpRegister** devuelve SNMPAPI SUCCESS si la función se completa correctamente, pero \_ el registro redundante no es eficaz.

1.  Una llamada a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) que solicita la entrega filtrada de capturas y notificaciones a la sesión, después de una llamada anterior a **SnmpRegister** que solicita la entrega de todas las capturas y notificaciones (entrega sin filtrar). Esta llamada es redundante porque la sesión ya recibe todas las capturas y notificaciones, incluido el tipo único definido por el filtro.
2.  Una llamada duplicada a **SnmpRegister** o una en la que la lista de parámetros es idéntica a la lista de parámetros de una llamada anterior a **SnmpRegister** para la sesión.
3.  Una llamada a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) que solicita la entrega filtrada de capturas y notificaciones basadas en un identificador de objeto (OID) cuyo prefijo es un OID especificado en una llamada anterior a **SnmpRegister**. Por ejemplo, puede especificar "1.3.6.1.4.1.311" en el parámetro de notificación para recibir notificaciones procedentes de cualquier entidad de agente SNMP de Microsoft.  Si vuelve a llamar a **SnmpRegister** y especifica "1.3.6.1.4.1.311.1", la segunda llamada es redundante porque la sesión ya recibe todas las capturas y notificaciones que contienen el prefijo OID "1.3.6.1.4.1.311".

Para anular el registro de la sesión, debe hacer coincidir cada llamada de registro única a la [**función SnmpRegister.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) Llame **a SnmpRegister** para anular el registro de la sesión y asegúrese de que los cinco primeros parámetros de **SnmpRegister** son idénticos a los de la llamada de registro inicial. La única diferencia entre la llamada inicial y la llamada de anulación del registro es que, al registrarse, debe especificar el valor SNMPAPI ON en el parámetro status y, al llamar a la función para anular el registro, debe especificar \_ SNMPAPI  \_ OFF. No es necesario hacer coincidir las llamadas de registro redundantes a **la función SnmpRegister.** Solo necesita coincidir con la primera llamada de registro única.

Para cambiar los criterios de filtrado, puede ser necesario que una aplicación anule primero el registro y deshabilite la entrega de determinadas capturas o notificaciones. A continuación, la aplicación puede crear un nuevo filtro llamando a [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), pasando los valores adecuados.

 

 




