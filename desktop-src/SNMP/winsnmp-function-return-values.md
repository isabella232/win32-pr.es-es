---
title: Valores devueltos de la función WinSNMP
description: El valor devuelto de una llamada de función WinSNMP puede ser un identificador de un recurso que la implementación de Microsoft WinSNMP asigna a la aplicación WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078246"
---
# <a name="winsnmp-function-return-values"></a>Valores devueltos de la función WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

El valor devuelto de una llamada de función WinSNMP puede ser un identificador de un recurso que la implementación de Microsoft WinSNMP asigna a la aplicación WinSNMP.

En la tabla siguiente se enumeran los cinco tipos de identificadores de recursos que asigna la implementación.



| Tipo de identificador    | Descripción                       |
|----------------|-----------------------------------|
| sesión de HSNMP \_ | Identificador de una sesión WinSNMP       |
| \_entidad HSNMP  | Identificador de una entidad SNMP          |
| contexto de HSNMP \_ | Identificador de un contexto SNMP         |
| PDU de HSNMP \_     | Identificador de una unidad de datos de protocolo    |
| HSNMP \_ VBL     | Identificador de una lista de enlaces de variables |



 

Para obtener más información, vea [objetos de identificador de recursos](resource-handle-objects.md).

El valor devuelto también puede ser un valor entero largo sin signo del tipo **smiUINT32** que representa un \_ valor de estado snmpapi.

En la tabla siguiente se enumeran los valores de estado de WinSNMP y su significado.



| Status           | Descripción                                                                      |
|------------------|----------------------------------------------------------------------------------|
| error de SNMPAPI \_ | Indica un error. Equivale a 0 o **null**.                                    |
| SNMPAPI \_ correcto | Indica que la función se ha completado correctamente. Equivale a 1 o a un recuento positivo. |



 

 

 