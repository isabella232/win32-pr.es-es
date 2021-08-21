---
title: Administrar identificadores de objeto
description: La API de WinSNMP proporciona varias funciones de utilidad WinSNMP que simplifican la manipulación de identificadores de objeto para aplicaciones WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362adbf445901f25307452d67c313ef2a8d0ac5aea038ebfcf61863a72370cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009423"
---
# <a name="managing-object-identifiers"></a>Administrar identificadores de objeto

La API de WinSNMP proporciona varias funciones de utilidad [WinSNMP](winsnmp-functions.md) que simplifican la manipulación de identificadores de objetos para aplicaciones WinSNMP.

La [**función SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) convierte la representación binaria interna de un identificador de objeto a su formato de cadena numérica de puntos. Al llamar a [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), especifique un búfer de cadena de longitud MAXOBJIDSTRSIZE (1408 bytes) para asegurarse de que el búfer de salida es lo suficientemente grande como para contener la cadena convertida. Para convertir un identificador de objeto del formato de cadena numérica de puntos a su representación binaria interna, llame a [**la función SnmpStrToOid.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

Para copiar un identificador de objeto SNMP, llame [**a la función SnmpOidCopy.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) Esta función asigna la memoria necesaria para el nuevo identificador de objeto.

Una aplicación WinSNMP debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar los recursos asignados para el miembro **ptr** de la estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) especificada por las funciones [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) y [**SnmpOidCopy.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)

La [**función SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) compara dos identificadores de objeto SNMP. La aplicación WinSNMP puede especificar el número de subidentificadores que se deben comparar. Llame **a SnmpOidCompare** para determinar si dos identificadores de objeto tienen prefijos comunes.

Para obtener información adicional sobre cómo administrar la memoria asignada para los identificadores de objeto, vea [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).

 

 




