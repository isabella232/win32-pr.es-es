---
description: La propiedad HoursSpecified del objeto SWbemDateTime es un valor booleano que indica si el componente de horas del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: 55211da6-cbd5-4e61-ab7d-ee20363e9d81
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. HoursSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.HoursSpecified
- ISWbemDateTime.HoursSpecified
- ISWbemDateTime.get_HoursSpecified
- ISWbemDateTime.put_HoursSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e092747768035b7948ddef66f4c4d542bfa2c38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706076"
---
# <a name="swbemdatetimehoursspecified-property"></a>Propiedad SWbemDateTime. HoursSpecified

La propiedad **HoursSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de horas del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín. Si **HoursSpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false**, [**SWbemDateTime. hours**](swbemdatetime-hours.md) contiene un valor DateTime. Un valor DateTime que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** . Si **HoursSpecified** es **false** y **IsInterval** es **true**, **SWbemDateTime. hours** contiene un intervalo.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemDateTime.HoursSpecified As Boolean
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

[**SWbemDateTime. horas**](swbemdatetime-hours.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




