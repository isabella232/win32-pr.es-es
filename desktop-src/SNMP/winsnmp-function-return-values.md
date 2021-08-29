---
title: Valores devueltos de la función WinSNMP
description: El valor devuelto de una llamada de función WinSNMP puede ser un identificador de un recurso que la implementación de WinSNMP de Microsoft asigna para la aplicación WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee75d85bf2e9b48f0b3172332f4340b21271ec37a9bc1027d63750927710f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142818"
---
# <a name="winsnmp-function-return-values"></a>Valores devueltos de la función WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

El valor devuelto de una llamada de función WinSNMP puede ser un identificador de un recurso que la implementación de WinSNMP de Microsoft asigna para la aplicación WinSNMP.

En la tabla siguiente se enumeran los cinco tipos de identificadores de recursos que asigna la implementación.



| Tipo de identificador    | Descripción                       |
|----------------|-----------------------------------|
| SESIÓN DE \_ HSNMP | Identificador de una sesión de WinSNMP       |
| ENTIDAD \_ HSNMP  | Identificador de una entidad SNMP          |
| CONTEXTO DE \_ HSNMP | Identificador de un contexto SNMP         |
| PDU de HSNMP \_     | Identificador de una unidad de datos de protocolo    |
| VBL de HSNMP \_     | Identificador de una lista de enlaces de variables |



 

Para obtener más información, vea [Objetos de identificador de recursos.](resource-handle-objects.md)

El valor devuelto también puede ser un valor entero largo sin signo del tipo **smiUINT32** que representa un valor DE ESTADO \_ DE SNMPAPI.

En la tabla siguiente se enumeran los valores de estado de WinSNMP y su significado.



| Estado           | Descripción                                                                      |
|------------------|----------------------------------------------------------------------------------|
| ERROR DE \_ SNMPAPI | Indica un error. Equivale a 0 o **NULL.**                                    |
| SNMPAPI \_ CORRECTO | Indica que la función se completó correctamente. Equivale a 1 o un recuento positivo. |



 

 

 