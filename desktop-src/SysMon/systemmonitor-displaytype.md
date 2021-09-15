---
title: Propiedad SystemMonitor.DisplayType
description: Recupera o establece el tipo de gráfico utilizado para representar los datos del contador de rendimiento.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Propiedad DisplayType SysMon
- Propiedad DisplayType SysMon , clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad DisplayType
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473425"
---
# <a name="systemmonitordisplaytype-property"></a>Propiedad SystemMonitor.DisplayType

Recupera o establece el tipo de gráfico utilizado para representar los datos del contador de rendimiento.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a>Valor de propiedad

Tipo de gráfico que se usa para representar los datos del contador de rendimiento. Para obtener los valores posibles, [**vea DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                                         |
|------------------------------|---------------------------------------------------|
| **System.ArgumentException** | El gráfico o el valor de informe especificados no son válidos. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





