---
title: Descriptores de WinSNMP
description: En el entorno de programación WinSNMP, un descriptor es una de las dos estructuras siguientes.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356804"
---
# <a name="winsnmp-descriptors"></a>Descriptores de WinSNMP

En el entorno de programación WinSNMP, un *descriptor* es una de las dos estructuras siguientes:

-   Una estructura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) que describe una variable de cadena de octeto
-   Una estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) que describe una variable de identificador de objeto SNMP

Un descriptor WinSNMP es una estructura que tiene dos miembros: un miembro de longitud, **Len** y un miembro de puntero, **ptr**. El miembro **ptr** apunta a la cadena de octeto o al identificador de objeto de interés. El miembro **ptr** puede ser el tipo de datos **smiLPBYTE** o **smiLPUINT32** .

Un descriptor de [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o un descriptor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) puede ser el miembro de **valor** de una estructura **smiVALUE** . La estructura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) describe el valor asociado a un nombre de variable en una entrada de enlace de variables.

La implementación de Microsoft WinSNMP asigna y desasigna memoria para todas las estructuras **smiOCTETS** y **smiOID** de salida. Por lo tanto, la aplicación debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar la memoria para el miembro **ptr** de estas estructuras.

Los miembros de cadena en los descriptores no requieren un byte de terminación **null** . Para obtener información adicional sobre la administración de la memoria asignada para los descriptores, vea [asignar objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




