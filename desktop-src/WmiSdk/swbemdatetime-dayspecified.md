---
description: Valor booleano que indica si el componente de día del valor DATETIME de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. DaySpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715747"
---
# <a name="swbemdatetimedayspecified-property"></a>Propiedad SWbemDateTime. DaySpecified

La propiedad **DaySpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de día del valor [**DateTime**](datetime.md) de CIM contiene un intervalo o un valor de carácter comodín. Si **DaySpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false**, [**SWbemDateTime. Day**](swbemdatetime-day.md) contiene un valor DateTime. Un valor [**DateTime**](datetime.md) que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** . Si **DaySpecified** es **false** y **IsInterval** es **true**, **SWbemDateTime. Day** contiene un intervalo.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md). Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | \_ISWBEMDATETIME IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemDateTime. Day**](swbemdatetime-day.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

 




