---
title: Asignación de objetos de memoria WinSNMP
description: Descriptores, identificadores de recursos y cadenas de estilo C son los tres tipos de objetos de memoria en el entorno de programación WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1188af74e150313cb24b01886d06df9e3ad065039cad9fa4a3e0b3b5ee6a9f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009794"
---
# <a name="allocating-winsnmp-memory-objects"></a>Asignación de objetos de memoria WinSNMP

Descriptores, identificadores de recursos y cadenas de estilo C son los tres tipos de objetos de memoria en el entorno de programación WinSNMP.

El tipo de objeto determina si la implementación de Microsoft WinSNMP o la aplicación WinSNMP asigna y desasigna la memoria para el objeto. Esto reduce la asignación innecesaria de espacio de búfer temporal y la copia innecesaria de búferes.

En la tabla siguiente se resume la asignación y desasignación de recursos para objetos de memoria WinSNMP.



| Tipo de objeto                                                                   | Descripción                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descriptor smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) [**o smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Si la aplicación WinSNMP asigna la memoria, debe desasignar la memoria con una llamada a una función adecuada. Si la implementación asigna la memoria, la aplicación debe llamar a la [**función SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desasignar la memoria. |
| [**smiVALUE (estructura)**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)                                    | Si el **miembro de** valor es [**un smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o un descriptor [**smiOCTETS,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) la aplicación debe continuar como se indicó anteriormente para los descriptores.                                                                                                     |
| Identificador de recursos                                                               | La implementación asigna, administra y libera la memoria.                                                                                                                                                                                                                         |
| Cadena de estilo C                                                                | La aplicación WinSNMP debe administrar y liberar la memoria que asigna.                                                                                                                                                                                                                |



 

Para obtener más información, [vea Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).

 

 




