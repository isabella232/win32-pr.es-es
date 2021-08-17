---
title: Descriptores de WinSNMP
description: En el entorno de programación WinSNMP, un descriptor es una de las dos estructuras siguientes.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875112d8519f93f4b5ae6729401f2689294a84c55dc729f0ffa24d05076e300b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142918"
---
# <a name="winsnmp-descriptors"></a>Descriptores de WinSNMP

En el entorno de programación WinSNMP, un *descriptor* es una de las dos estructuras siguientes:

-   Estructura [**smiOCTETS que**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) describe una variable de cadena de octeto
-   Estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) que describe una variable de identificador de objeto SNMP

Un descriptor WinSNMP es una estructura que tiene dos miembros: un miembro de longitud, **len** y un miembro de puntero, **ptr**. El **miembro ptr** apunta a la cadena de octeto o al identificador de objeto de interés. El **miembro ptr** puede ser el tipo de datos **smiLPBYTE** o **smiLPUINT32.**

Un [**descriptor smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o un descriptor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) puede ser el miembro **de** valor de una **estructura smiVALUE.** La [**estructura smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) describe el valor asociado a un nombre de variable en una entrada de enlace de variable.

La implementación de Microsoft WinSNMP asigna y desasigna memoria para todas las estructuras **smiOCTETS** y **smiOID de** salida. Por lo tanto, la aplicación debe llamar a [**la función SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar la memoria del **miembro ptr** de estas estructuras.

Los miembros de cadena en descriptores no requieren **un** byte de terminación NULL. Para obtener información adicional sobre cómo administrar la memoria asignada para los descriptores, vea [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).

 

 




