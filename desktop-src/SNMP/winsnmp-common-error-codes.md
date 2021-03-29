---
title: Códigos de error comunes de WinSNMP
description: La función SnmpGetLastError puede devolver un código de error general después de que se produzca un error en una función WinSNMP. En la tabla siguiente se enumeran los códigos de error comunes de WinSNMP.
ms.assetid: c286750f-a542-4f61-a22c-d77debd45775
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beee49aef651784b0b8dc05c0114b7bf906be113
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078086"
---
# <a name="winsnmp-common-error-codes"></a>Códigos de error comunes de WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

La función [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) puede devolver un código de error general después de que se produzca un error en una función WinSNMP. En la tabla siguiente se enumeran los códigos de error comunes de WinSNMP.



| Código de error                | Significado                                                                                                                                                                                                        | Acción recomendada                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ no se \_ inicializó | La función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) no se completó correctamente desde que comenzó la ejecución del programa o desde que se completó correctamente una llamada a la función [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . | La aplicación debe llamar a [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) antes de llamar a cualquier otra función de API WinSNMP cuando se produce un error de [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) . La función [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) devuelve información de error extendida sobre el error de [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup).                                                          |
| \_error de asignación de snmpapi \_     | La aplicación especificó un puntero no válido o se produjo un error durante la asignación de memoria. La implementación de Microsoft WinSNMP no pudo obtener suficientes recursos para ejecutar la solicitud.                | La aplicación debe proporcionar punteros de memoria válidos para todos los parámetros de salida. Debe liberar recursos, reducir los requisitos de recursos o facilitar un cierre estable. Un cierre estable incluye varias llamadas a la función [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , una por cada sesión WinSNMP abierta. También incluye una llamada a la función [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . |
| \_NOOP snmpapi             | La función no se completó correctamente porque todos los parámetros de salida son **null**.                                                                                                                         | La aplicación debe especificar al menos un parámetro de salida que no sea **null** cuando se llame a una función que devuelva información a la aplicación.                                                                                                                                                                                                                                  |
| SNMPAPI \_ otro \_ error     | Se produjo un error desconocido o no definido.                                                                                                                                                                        | Normalmente, la aplicación debe responder con un cierre estable. Un cierre estable incluye varias llamadas a la función [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , una por cada sesión WinSNMP abierta. También incluye una llamada a la función [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) .                                                                                                           |



 

Los errores WinSNMP que transmiten información específica del contexto se indican en la página de referencia de cada función.

 

 