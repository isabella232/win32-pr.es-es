---
title: Objetos de identificador de recursos
description: La estructura de un objeto de recurso está restringida a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede tener acceso a un objeto de recurso con un identificador.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778595"
---
# <a name="resource-handle-objects"></a>Objetos de identificador de recursos

La estructura de un objeto de recurso está restringida a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede tener acceso a un objeto de recurso con un identificador.

La implementación puede asignar uno de los siguientes tipos de identificadores de recursos para una aplicación WinSNMP.

| Tipo de identificador        | Descripción                       |
|--------------------|-----------------------------------|
| **sesión de HSNMP \_** | Identificador de una sesión WinSNMP       |
| **\_entidad HSNMP**  | Identificador de una entidad SNMP          |
| **contexto de HSNMP \_** | Identificador de un contexto WinSNMP       |
| **PDU de HSNMP \_**     | Identificador de una unidad de datos de protocolo    |
| **HSNMP \_ VBL**     | Identificador de una lista de enlaces de variables |



 

Una aplicación WinSNMP puede solicitar que la implementación cree o elimine identificadores de recursos, pero la implementación realiza la operación. Para obtener información adicional sobre cómo liberar recursos individuales, vea las funciones [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)y [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .

 

 




