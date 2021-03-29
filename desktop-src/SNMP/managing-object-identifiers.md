---
title: Administrar identificadores de objeto
description: La API WinSNMP proporciona varias funciones de utilidad WinSNMP que simplifican la manipulación de los identificadores de objeto para las aplicaciones WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486983"
---
# <a name="managing-object-identifiers"></a>Administrar identificadores de objeto

La API WinSNMP proporciona varias [funciones de utilidad WinSNMP](winsnmp-functions.md) que simplifican la manipulación de los identificadores de objeto para las aplicaciones WinSNMP.

La función [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) convierte la representación binaria interna de un identificador de objeto en su formato de cadena numérica con puntos. Cuando llame a [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), especifique un búfer de cadena de longitud MAXOBJIDSTRSIZE (1408 bytes) para asegurarse de que el búfer de salida es lo suficientemente grande como para contener la cadena convertida. Para convertir un identificador de objeto del formato de cadena numérica con puntos en su representación binaria interna, llame a la función [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .

Para copiar un identificador de objeto SNMP, llame a la función [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) . Esta función asigna cualquier memoria necesaria para el nuevo identificador de objeto.

Una aplicación WinSNMP debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar los recursos asignados para el miembro **ptr** de la estructura [**SmiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) especificada por las funciones [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) y [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .

La función [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) compara dos identificadores de objeto SNMP. La aplicación WinSNMP puede especificar el número de subidentificadors que se van a comparar. Llame a **SnmpOidCompare** para determinar si dos identificadores de objeto tienen prefijos comunes.

Para obtener información adicional sobre la administración de la memoria asignada para los identificadores de objeto, vea [asignar objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




