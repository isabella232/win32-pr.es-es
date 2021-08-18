---
title: Liberar descriptores winSNMP
description: El entorno de programación WinSNMP asigna la desasignación de recursos de descriptor a la implementación de WinSNMP o a la aplicación WinSNMP, en función del componente que asigne la memoria para el descriptor.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86081a69cd5455bc3c58ca2bcea50154d75920a17655a1feef30ac2d29675d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009533"
---
# <a name="freeing-winsnmp-descriptors"></a>Liberar descriptores winSNMP

El entorno de programación WinSNMP asigna la desasignación de recursos de descriptor a la implementación de WinSNMP o a la aplicación WinSNMP, en función del componente que asigne la memoria para el descriptor.

Para liberar los recursos de [**un smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o un descriptor [**smiOCTETS,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) se aplican las siguientes reglas:

-   Para los parámetros de entrada

    Dado que la aplicación WinSNMP asigna la memoria para los objetos de entrada con longitudes variables, la aplicación debe liberar esa memoria mediante una función adecuada. Por ejemplo, si la aplicación asignó los recursos con una llamada a la función [**GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) debe usar la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) para desasignar los recursos. Si la aplicación asignó los recursos con una llamada a la función [**HeapAlloc,**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) debe llamar a [**la función HeapFree.**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)

-   Para los parámetros de salida

    Una llamada a cualquiera de las funciones siguientes da como resultado que la implementación asigne memoria para un [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o un descriptor [**smiOCTETS:**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb), [**SnmpEncodeMsg,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy), [**SnmpContextToStr y**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Dado que la implementación asigna la memoria para estos objetos de salida, la aplicación debe llamar a la [**función SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desasignar los recursos. Esta función permite a la implementación liberar la memoria asignada para el **miembro ptr** de estas estructuras.

Para liberar los recursos de una estructura [**smiVALUE,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) una  aplicación WinSNMP debe comprobar el  miembro de sintaxis de una estructura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) para evaluar correctamente el miembro de valor de la estructura. Si  el miembro de  sintaxis indica que el miembro de valor es [**un descriptor smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o [**smiOID,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) y la implementación asignó los recursos para el descriptor, la aplicación debe llamar a [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor). Esto permite a la implementación liberar la memoria. Si la aplicación asignó los recursos, debe liberar la memoria mediante una función adecuada, como se indicó anteriormente.

Para obtener más información, [vea Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).

 

 