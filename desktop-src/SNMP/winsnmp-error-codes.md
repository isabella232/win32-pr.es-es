---
title: Códigos de error de WinSNMP
description: Códigos de error de WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Códigos de error de WinSNMP SNMP
- Códigos de error SNMP , WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2a9f9dda792008a0e69e6c23e692b4aa4c4e78316eeca015f7b056e2a275df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142868"
---
# <a name="winsnmp-error-codes"></a>Códigos de error de WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

> [!Note]  
> Los errores descritos en este tema son distintos de los códigos de error SNMP definidos por las RFC pertinentes.

 

Todas las funciones WinSNMP devuelven el valor **SNMPAPI \_ FAILURE** si se produce un error en la función. La aplicación WinSNMP debe llamar inmediatamente a la [**función SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) para recuperar información de error extendida cuando se produce un error en una función WinSNMP. En la tabla siguiente se enumeran los temas que tratan los códigos de error extendidos devueltos por las funciones winSNMP.



| Tema                                                        | Descripción                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Códigos de error comunes de WinSNMP](winsnmp-common-error-codes.md) | Describe códigos de error comunes para la API winSNMP.       |
| [Errores de transporte de red](network-transport-errors.md)     | Describe los errores de transporte de red para la API de WinSNMP. |



 

Los errores de WinSNMP que transmiten información específica del contexto se incluyen en la página de referencia de función.

 

 