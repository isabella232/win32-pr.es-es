---
title: Asignación de objetos de memoria WinSNMP
description: Los descriptores, los identificadores de recursos y las cadenas de estilo C son tres tipos de objetos de memoria en el entorno de programación WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075048"
---
# <a name="allocating-winsnmp-memory-objects"></a>Asignación de objetos de memoria WinSNMP

Los descriptores, los identificadores de recursos y las cadenas de estilo C son tres tipos de objetos de memoria en el entorno de programación WinSNMP.

El tipo de objeto determina si la implementación de Microsoft WinSNMP o la aplicación WinSNMP asigna y desasigna la memoria para el objeto. Esto reduce la asignación innecesaria de espacio en búfer temporal y la copia innecesaria de búferes.

En la tabla siguiente se resume la asignación y desasignación de recursos para los objetos de memoria WinSNMP.



| Tipo de objeto                                                                   | Descripción                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| descriptor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Si la aplicación WinSNMP asigna la memoria, debe desasignar la memoria con una llamada a una función adecuada. Si la implementación asigna la memoria, la aplicación debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desasignar la memoria. |
| estructura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)                                    | Si el miembro de **valor** es un descriptor de [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , la aplicación debe continuar como se indicó anteriormente para los descriptores.                                                                                                     |
| Identificador de recursos                                                               | La implementación asigna, administra y libera la memoria.                                                                                                                                                                                                                         |
| Cadena de estilo C                                                                | La aplicación WinSNMP debe administrar y liberar la memoria que asigna.                                                                                                                                                                                                                |



 

Para obtener más información, consulte [liberación de descriptores WinSNMP](freeing-winsnmp-descriptors.md).

 

 




