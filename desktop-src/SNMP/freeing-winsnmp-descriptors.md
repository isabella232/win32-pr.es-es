---
title: Liberación de descriptores WinSNMP
description: El entorno de programación WinSNMP asigna la desasignación de los recursos del descriptor a la implementación de WinSNMP o a la aplicación WinSNMP, dependiendo del componente que asigna la memoria para el descriptor.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97828c55d59932b7f4bdb75cbcf98964edd4a7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149592"
---
# <a name="freeing-winsnmp-descriptors"></a>Liberación de descriptores WinSNMP

El entorno de programación WinSNMP asigna la desasignación de los recursos del descriptor a la implementación de WinSNMP o a la aplicación WinSNMP, dependiendo del componente que asigna la memoria para el descriptor.

Para liberar los recursos de un descriptor de [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , se aplican las siguientes reglas:

-   Para los parámetros de entrada

    Dado que la aplicación WinSNMP asigna la memoria para los objetos de entrada con longitudes variables, la aplicación debe liberar esa memoria usando una función adecuada. Por ejemplo, si la aplicación asignó los recursos con una llamada a la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) , debe usar la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) para desasignar los recursos. Si la aplicación asignó los recursos con una llamada a la función [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) , debe llamar a la función [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree) .

-   Para los parámetros de salida

    Una llamada a cualquiera de las siguientes funciones provoca la implementación de la asignación de memoria para un descriptor de [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) : [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb), [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg), [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy), [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)y [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Dado que la implementación asigna la memoria para estos objetos de salida, la aplicación debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desasignar los recursos. Esta función permite a la implementación liberar la memoria asignada para el miembro **ptr** de estas estructuras.

Para liberar los recursos de una estructura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) , una aplicación WinSNMP debe comprobar el miembro de **Sintaxis** de una estructura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) para evaluar correctamente el miembro de **valor** de la estructura. Si el miembro de **Sintaxis** indica que el miembro de **valor** es un descriptor de [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , y la implementación asignó los recursos para el descriptor, la aplicación debe llamar a [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor). Esto permite a la implementación liberar la memoria. Si la aplicación asignó los recursos, debe liberar la memoria mediante una función adecuada, como se indicó anteriormente.

Para obtener más información, consulte [asignar objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 