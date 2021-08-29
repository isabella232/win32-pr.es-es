---
title: Códigos de error comunes de WinSNMP
description: La función SnmpGetLastError puede devolver un código de error general después de que se produce un error en una función WinSNMP. En la tabla siguiente se enumeran los códigos de error comunes de WinSNMP.
ms.assetid: c286750f-a542-4f61-a22c-d77debd45775
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37550478b37cdc75c2dea427e54b4d9d3d52dcc838273a09cf904cd4479baa4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142958"
---
# <a name="winsnmp-common-error-codes"></a>Códigos de error comunes de WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

La [**función SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) puede devolver un código de error general después de que se produce un error en una función WinSNMP. En la tabla siguiente se enumeran los códigos de error comunes de WinSNMP.



| Código de error                | Significado                                                                                                                                                                                                        | Acción recomendada                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ NO \_ INICIALIZADO | La [**función SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) no se completó correctamente desde que se inició la ejecución del programa o desde que una llamada a la [**función SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) se completó correctamente. | La aplicación debe llamar a [**SnmpGetLastError antes**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) de llamar a cualquier otra función de la API winSNMP cuando se produce un error [**en SnmpStartup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) La [**función SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) devuelve información de error extendida sobre el error [**de SnmpStartup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)                                                          |
| ERROR DE ALLOC DE SNMPAPI \_ \_     | La aplicación especificó un puntero no válido o se produjo un error durante la asignación de memoria. La implementación de Microsoft WinSNMP no pudo obtener recursos suficientes para ejecutar la solicitud.                | La aplicación debe proporcionar punteros de memoria válidos para todos los parámetros de salida. Debe liberar recursos, reducir los requisitos de recursos o facilitar un cierre estable. Un cierre estable incluye varias llamadas a la [**función SnmpClose,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una para cada sesión winSNMP abierta. También incluye una llamada a la [**función SnmpCleanup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) |
| SNMPAPI \_ NOOP             | La función no se ha completado correctamente porque todos los parámetros de salida son **NULL.**                                                                                                                         | La aplicación debe especificar al menos un parámetro de salida que no sea **NULL** al llamar a una función que devuelve información a la aplicación.                                                                                                                                                                                                                                  |
| SNMPAPI \_ OTHER \_ ERROR     | Se produjo un error desconocido o indefinido.                                                                                                                                                                        | La aplicación normalmente debe responder con un cierre correcto. Un cierre estable incluye varias llamadas a la [**función SnmpClose,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una para cada sesión winSNMP abierta. También incluye una llamada a la [**función SnmpCleanup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)                                                                                                           |



 

Los errores de WinSNMP que transmiten información específica del contexto se anotan en la página de referencia de cada función.

 

 