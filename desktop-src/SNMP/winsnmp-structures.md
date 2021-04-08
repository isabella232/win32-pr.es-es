---
title: Estructuras WinSNMP
description: Las funciones de API WinSNMP usan las siguientes estructuras.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- Estructuras WinSNMP de SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904702"
---
# <a name="winsnmp-structures"></a>Estructuras WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Las funciones de API WinSNMP usan las siguientes estructuras.



| Estructura                                  | Descripción                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contiene un valor entero de 64 bits sin signo que representa un contador.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contiene un puntero a una cadena de octeto SNMP de longitud variable.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contiene un puntero a una matriz de longitud variable de los subidentificadores que están asociados a un objeto con nombre especificado. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Representa el valor que está asociado a un nombre de variable en una entrada de enlace de variable.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contiene información sobre la implementación de Microsoft de WinSNMP.                                                    |



 

 

 