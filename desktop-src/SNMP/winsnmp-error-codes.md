---
title: Códigos de error WinSNMP
description: Códigos de error WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Códigos de error WinSNMP SNMP
- Códigos de error SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488146"
---
# <a name="winsnmp-error-codes"></a>Códigos de error WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

> [!Note]  
> Los errores descritos en este tema son distintos de los códigos de error SNMP definidos por las RFC pertinentes.

 

Todas las funciones WinSNMP devuelven el valor **snmpapi \_ error** si se produce un error en la función. La aplicación WinSNMP debe llamar inmediatamente a la función [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) para recuperar la información de error extendida cuando se produce un error en una función WinSNMP. En la tabla siguiente se enumeran los temas que describen los códigos de error extendidos devueltos por las funciones WinSNMP.



| Tema                                                        | Descripción                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Códigos de error comunes de WinSNMP](winsnmp-common-error-codes.md) | Describe los códigos de error comunes de la API WinSNMP.       |
| [Errores de transporte de red](network-transport-errors.md)     | Describe los errores de transporte de red para la API WinSNMP. |



 

Los errores WinSNMP que transmiten información específica del contexto se incluyen en la página de referencia de la función.

 

 