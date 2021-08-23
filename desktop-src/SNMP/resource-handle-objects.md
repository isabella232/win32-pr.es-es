---
title: Objetos de identificador de recursos
description: La estructura de un objeto de recurso está restringida a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede acceder a un objeto de recurso con un identificador.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b05702f0ad43e5b4b80a9b1a3cada471212dec3bc377bddcc95fe9a109ec78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009123"
---
# <a name="resource-handle-objects"></a>Objetos de identificador de recursos

La estructura de un objeto de recurso está restringida a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede acceder a un objeto de recurso con un identificador.

La implementación puede asignar uno de los siguientes tipos de identificadores de recursos para una aplicación WinSNMP.

| Tipo de identificador        | Descripción                       |
|--------------------|-----------------------------------|
| **SESIÓN DE \_ HSNMP** | Identificador de una sesión de WinSNMP       |
| **ENTIDAD \_ HSNMP**  | Identificador de una entidad SNMP          |
| **CONTEXTO DE \_ HSNMP** | Identificador de un contexto winSNMP       |
| **PDU de HSNMP \_**     | Identificador de una unidad de datos de protocolo    |
| **HSNMP \_ VBL**     | Identificador de una lista de enlaces de variables |



 

Una aplicación WinSNMP puede solicitar que la implementación cree o elimine identificadores de recursos, pero la implementación realiza la operación. Para obtener información adicional sobre cómo liberar recursos individuales, vea las funciones [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)y [**SnmpFreeContext.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)

 

 




