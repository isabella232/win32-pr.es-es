---
title: Estructuras de WinSNMP
description: Las funciones de API de WinSNMP usan las siguientes estructuras.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- SNMP de estructuras winSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b409b6d12063ebd3feb9c663f2d607bc5ceead0462b2945334f1e7e691c9be63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142758"
---
# <a name="winsnmp-structures"></a>Estructuras de WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Las funciones de API de WinSNMP usan las siguientes estructuras.



| Estructura                                  | Descripción                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contiene un valor entero de 64 bits sin signo que representa un contador.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contiene un puntero a una cadena de octeto SNMP de longitud variable.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contiene un puntero a una matriz de longitud variable de los subidentificadores asociados a un objeto con nombre especificado. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Representa el valor asociado a un nombre de variable en una entrada de enlace de variable.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contiene información sobre la implementación de Microsoft de WinSNMP.                                                    |



 

 

 